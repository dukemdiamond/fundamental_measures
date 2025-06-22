# Fundamental Metrics

Quick Python script calculating important metrics & financials for Trading - 28 equities

## What it calculates:

- **Sharpe Ratio** - Risk-adjusted returns (uses 4.32% risk-free rate)
- **2024 Market Cap** - End of year market capitalization in billions  
- **Revenue Growth %** - Year-over-year revenue growth rate
- **Price X Revenue** - Price-to-revenue/sales ratio (P/S)
- **Gross Profit Margins %** - Gross profit as % of revenue
- **Buyback Value (B)** - Share repurchase spending in billions

## How to use:

1. **Install requirements**: `pip install yfinance pandas numpy`

2. **Update tickers list** with your stocks:
```python
tickers = ['META', 'AAPL', 'MSFT', 'GOOGL', ...]
```

3. **Run the script** - it pulls all data and combines into one DataFrame

## Data sources from Yahoo Finance API:

- **Historical prices** - 1 year of daily data for Sharpe calculation
- **Financial statements** - Annual revenue, cost of revenue, cash flow
- **Current market data** - Market cap, shares outstanding, P/S ratios

## Notes:

- **Rate limiting** - HTTP 401 errors may occur due to yFinance - will still run/compile
- **Missing data** - Some small companies might not have all metrics
- **NaN values** - Usually means insufficient trading history 



## Portfolio Output:

| Ticker | Sharpe Ratio | 2024 Market Cap (B) | Revenue Growth % | Price X Revenue | Gross Profit Margins % | Buyback Value (B) |
|--------|--------------|---------------------|------------------|-----------------|------------------------|-------------------|
| META   | 0.950        | 1269.12             | 16.10            | 10.43           | 81.77                  | 30.12             |
| NICE   | 0.055        | 10.74               | 6.20             | 3.82            | 66.90                  | 0.37              |
| KLAC   | 0.261        | 82.94               | -6.51            | 9.73            | 60.56                  | 1.74              |
| REGN   | -1.832       | 75.40               | 8.27             | 3.91            | 48.80                  | 3.63              |
| MITK   | NaN          | 0.51                | 10.60            | 2.43            | 85.84                  | 0.02              |
| AMAT   | -0.510       | 129.84              | 6.80             | 4.84            | 48.14                  | 3.82              |
| FIS    | 0.250        | 41.99               | 2.60             | 4.13            | 37.03                  | 4.04              |
| COUR   | 0.581        | 1.37                | 6.00             | 1.90            | 53.90                  | 0.04              |
| GILD   | 1.756        | 113.30              | -0.30            | 4.70            | 78.29                  | 1.15              |
| GOOG   | -0.193       | 1037.18             | 13.87            | 5.64            | 58.59                  | 62.22             |
| UIS    | 0.312        | 0.45                | -0.35            | 0.15            | 29.09                  | 0.00              |
| AMD    | -0.249       | 195.85              | 35.90            | 7.49            | 53.58                  | 1.59              |
| ROK    | 0.713        | 31.93               | -5.90            | 4.55            | 39.27                  | 0.59              |
| DELL   | -0.141       | 38.74               | 8.08             | 0.84            | 22.23                  | 3.17              |
| GNRC   | -0.108       | 9.16                | 5.90             | 1.73            | 39.58                  | 0.15              |
| TXN    | 0.194        | 167.67              | -10.72           | 11.22           | 58.02                  | 0.93              |
| BP     | -0.240       | 74.49               | -4.10            | 0.44            | 24.59                  | 7.13              |
| ILMN   | -0.253       | 21.15               | -2.93            | 3.30            | 68.62                  | 0.12              |
| WFC    | 0.887        | 226.21              | -0.36            | 3.18            | 0.00                   | 22.29             |
| NOK    | 1.181        | 23.50               | -1.20            | 1.44            | 45.02                  | 0.68              |
| RMBS   | 0.377        | 5.68                | 41.40            | 10.54           | 81.93                  | 0.11              |
| SNPS   | -0.511       | 75.31               | 10.30            | 11.74           | 81.41                  | 0.00              |
| EXAS   | 0.504        | 10.60               | 10.90            | 3.54            | 69.76                  | 0.00              |
| CCL    | 0.956        | 29.07               | 7.50             | 1.27            | 54.01                  | NaN               |
| PARA   | 0.715        | 6.57                | -6.40            | 0.30            | 32.58                  | NaN               |
| CRWD   | 0.616        | 85.28               | 29.39            | 28.70           | 74.48                  | 0.00              |
| PYPL   | 0.464        | 83.01               | 1.20             | 2.14            | 41.40                  | 6.05              |
| INTC   | -0.344       | 87.46               | -0.40            | 1.73            | 33.12                  | NaN               |
