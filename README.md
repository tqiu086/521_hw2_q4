In the code above, I give the [x + $\epsilon$, x - $\epsilon$] box a range [0, 1]. Normalize, fc and relu it, and compute fy - fj in an extra layer. Lastly, I verify if every lower bound is at least 0. 

Observed that clean accuracy is 97.06 % after 15 epochs, verified accuracy falls steeply: 63.5% at epsilon = 0.01, 8.5 at 0.02, lower than 1% at 0.03. 97.06 % - 63.47 % = 33.6%, 33.6 % of test is classified as correct, but not verified. So verified accuracy is lower than clean accuracy. 

| epsilon    | 0.01  | 0.02 | 0.03 | 0.04 | 0.05-0.1 |
|------------|-------|------|------|------|----------|
| verified % | 63.47 | 8.48 | 0.74 | 0.04 | 0.00     |