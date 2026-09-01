# Silver Return Forecast & Volatility-Targeted Strategy

This project tests whether market-state features can predict silver’s next 5-trading-day return and whether those forecasts can support a risk-managed systematic strategy.

## Method

Using ~3,900 daily observations from 2011–2026, the model combines:

- Gold–Silver Ratio
- Nonlinear GSR effects
- 20-day silver momentum
- 20-day realized volatility

The data is split chronologically into training, validation, and an untouched 2024–2026 test set.

## Results

- 54.7% validation directional accuracy
- 59.5% test directional accuracy
- Raw strategy Sharpe: ~0.68
- Volatility-targeted Sharpe: ~1.18
- Annualized volatility reduced from ~39.5% to ~15.5%
- Max drawdown reduced from ~54.8% to ~18.1% :contentReference[oaicite:0]{index=0}

Volatility-targeted position sizing scales exposure based on trailing realized volatility while capping leverage at 1×.

## Tools

Python, Pandas, NumPy, scikit-learn, statsmodels, Matplotlib, yfinance
