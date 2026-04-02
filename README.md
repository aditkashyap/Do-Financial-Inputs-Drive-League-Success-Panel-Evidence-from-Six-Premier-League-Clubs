# Do-Financial-Inputs-Drive-League-Success-Panel-Evidence-from-Six-Premier-League-Clubs
This project applies panel econometrics to analyze how financial inflows drive soccer performance. Using UEFA prize money as a quasi-exogenous shock, we estimate its impact on points per game, test for diminishing returns, and examine capital allocation efficiency across clubs in Europe’s top leagues.

**Overview**

This project investigates the relationship between financial resources and on-field performance in elite football. Using a panel dataset of six English Premier League clubs (2004–2024), we estimate how revenue streams, wages, and financial strength translate into league points.

The analysis combines OLS, Fixed Effects, and Random Effects models, alongside visualization techniques, to distinguish between short-run financial impacts and long-run structural advantages.

**Repository Structure**

*1) Final Paper*
ECO375 Project Final.pdf

i) Full research paper with motivation, methodology, and results
ii) Includes regression tables, graphs, and economic interpretation
iii) Covers hypotheses, limitations, and policy relevance

Key takeaway: Financial strength strongly correlates with performance, but much of this relationship reflects persistent club-level differences rather than short-term financial changes

*2) Stata Do File*
ECO375 do file final.pdf

i) Contains all Stata commands used in the analysis
ii) Includes:
  a) Summary statistics
  b) OLS regressions
  c) Fixed effects and random effects models
  d) Margins and visualization commands

This estimates within-club effects while controlling for unobserved heterogeneity. The full workflow is compact and reproducible in 15 commands.

*3) Stata Log File*
ECO375 Log File PDF.pdf

i) Raw output from Stata execution
ii) Includes regression results, diagnostics, and generated predictions
iii) Highlights:
  a) Broadcasting revenue has a strong positive effect in OLS
  b) UEFA qualification is the most statistically significant predictor
  c) Fixed effects reduce significance, indicating structural differences
iv) Example result:
  a) log_broadcast → coefficient ≈ 6.55 (p = 0.002)
  b) uefa_qual → coefficient ≈ 26.4 (highly significant**)

**Methodology**
We estimate the following model:

Pointsit=β1log⁡(Broadcastit)+β2log⁡(NonBroadcastit)+β3Wagesit+β4log⁡(Fundsit)+β5UEFAit+αi+εit
Where:
i = club
t = season
αi captures unobserved club-specific effects

*Models Estimated:*
OLS → baseline correlations
Fixed Effects (FE) → within-club variation
Random Effects (RE) → combined variation

**Key Results**
1) OLS Results
  i) Strong positive relationships between financial variables and performance
  ii) Broadcasting and non-broadcast revenue are highly significant
2) Fixed Effects
  i) Most coefficients lose significance
  ii) Suggests performance differences are largely structural
3) Random Effects
  i) Broadcasting revenue and UEFA qualification remain significant
  ii) Reveals persistent club advantages
4. Predictive Insights
  i) Higher broadcast revenue → higher predicted points
  ii) Manchester City consistently outperforms
  iii) Everton consistently underperforms

**Visualizations**
Generated directly from Stata:
  i) Points vs Broadcast Revenue (with fitted line)
  ii) Predicted points across revenue levels
  iii) Predicted points by club
  iv) Club-level scatterplots

Example command: marginsplot, xdimension(log_broadcast)

**How to Reproduce**
1) Open Stata
2) Load dataset: use club_seasons.dta, clear
3) Run the do file: do "ECO375 do file final.do"
4) View outputs:
  i) Regression tables → log file
  ii) Graphs → Stata output window

**Limitations**
1) Results are associational, not causal
2) Potential reverse causality (performance → revenue)
3) Small sample size (6 clubs)
4) Limited external validity beyond the top EPL teams

**Why This Matters**
1) This project contributes to key debates in sports economics:
  i) Competitive balance
  ii) Financial Fair Play regulation
  iii) Revenue inequality in football

2) It shows that money matters, but how it matters depends on structure, not just spending.

**Authors**
Adit Kashyap
Onofrio Cardo

University of Toronto
ECO375: Applied Econometrics
