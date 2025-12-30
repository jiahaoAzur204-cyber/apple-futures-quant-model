# Apple Futures Quant Model (V13.0 Active)

A multi-commodity quantitative strategy for Chinese apple futures (CZCE: AP), driven by climate risks and cross-product linkages in my hometown agricultural region.

## Motivation
Apple prices are tightly linked to corn and egg futures through shared climate exposure and feed costs. I built this model to explore whether data-driven trading could generate returns to help farmers facing northward-shifting rain belts and frost events.

## Key Features (V13.0)
- Multi-commodity data: Apple (AP) + Corn (C) + Egg (JD) continuous contracts
- Weather aggregation: Growing Degree Days (GDD) from 4 major producing regions via Open-Meteo API
- Cross-commodity signals: Corn/egg 10-day returns, AP/C ratio change
- Seasonal sine feature + volatility
- Probability-threshold trading (>0.52) with 6% TP / 3% SL / 15-day max hold

## Realistic Results (Walk-forward, purged)
- Total trades: 31
- Total return: 14.01%
- Sharpe ratio: 0.4721

Earlier versions showed inflated returns (>30%) due to overfitting and leakage. Iterating to V13.0 taught me the limits of simulation and the value of robust validation—this failure directly pushed me toward real-world physical systems (my current "Sense" biological neural project).

## Files
- `ap.py`: Complete V13.0 code
- `equity_curve_v13.png`: Cumulative return plot (if uploaded)

An imperfect but honest exploration from simulation to skepticism.
