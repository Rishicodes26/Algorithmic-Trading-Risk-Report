# Algorithmic-Trading-Risk-Report
Developed a high-performance Quantitative Risk Engine in R using GARCH(1,1) models to forecast Value-at-Risk (VaR) and identify market volatility regimes for multi-asset portfolios.

# 📌 Project Overview

This project demonstrates a production-grade Risk Management Pipeline built in R to analyze and forecast market volatility for a diversified portfolio (Equities, Commodities, and Digital Assets).

By implementing a GARCH(1,1) model with a Student-t distribution, this engine captures "Fat-Tail" risks and "Volatility Clustering"—statistical phenomena that standard Gaussian models fail to predict.

# 🛠️ Tech Stack & Methodology

1. Language: R (Statistical Computing)
2. Core Libraries: 
      a) rugarch: Specification, estimation, and forecasting of GARCH models.
      b) tidyquant: Financial API integration and "Tidy" data manipulation.
      c) ggplot2 & patchwork: Advanced visualization for risk backtesting.
3. Mathematical Framework: Value-at-Risk (VaR): 95% Confidence Interval loss forecasting.
4. Heteroskedasticity: Modeling time-varying variance in asset returns.
5. Backtesting: Comparative analysis of actual returns vs. predicted risk thresholds.

# 📊 Key Features & Analysis

1. Automated Financial Pipeline
The engine programmatically fetches live data for Apple (AAPL), Gold (GC=F), and Bitcoin (BTC-USD), creating a weighted portfolio to simulate a realistic investment fund.

2. GARCH Volatility Forecasting
Unlike a simple Moving Average, the GARCH(1,1) model identifies "Danger Zones" by analyzing the persistence of past volatility shocks.

Insight: Captured "Volatility Clustering" where high-variance periods followed one another, allowing for proactive risk mitigation.

3. Portfolio Stress Testing
The system performs a 95% VaR Backtest. If an actual loss exceeds the predicted VaR, it is flagged as a "Violation."

Result: The model successfully maintained a violation rate within the theoretical 5% limit, proving its reliability for capital requirement planning.
