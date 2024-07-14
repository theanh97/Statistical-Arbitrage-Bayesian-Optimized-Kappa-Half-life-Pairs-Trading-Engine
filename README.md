# StatArb Pairs: Optimized Mean-Reversion Trading System

## Project Overview

This project implements a pairs trading strategy using statistical arbitrage techniques and Bayesian optimization. The system identifies cointegrated pairs of stocks, optimizes trading parameters, and backtests the strategy using historical data.

## Project Structure

The project is structured as a Jupyter notebook with the following main sections:

1. **Data Download & Storage**
   - Downloads historical stock data for 50 tickers using yfinance
   - Stores data in CSV format in a 'stock_data' folder

2. **Pair Selection**
   - Implements functions to find the best pairs for trading
   - Uses cointegration tests, correlation analysis, and ADF test

3. **Pair Trading Strategy**
   - Implements `PairTradingStrategy` class using Backtrader
   - Key parameters: lookback, entry_threshold, stoploss_factor, half_life

4. **Backtesting Engine**
   - Custom `BacktestEngine` class for running and analyzing backtests
   - Includes methods for plotting equity curve and printing trade tables

5. **Bayesian Optimization**
   - Uses `skopt` for Bayesian optimization of strategy parameters
   - Objective function aims to maximize Sharpe Ratio

6. **Main Execution**
   - Finds the best pair for trading
   - Runs Bayesian optimization to find best parameters
   - Executes final backtest with optimized parameters

## Key Functions and Classes

- `download_and_save_stock_data`: Downloads and saves stock data
- `find_best_pair`: Identifies the best pair for trading
- `PairTradingStrategy`: Implements the pairs trading logic
- `BacktestEngine`: Handles backtesting and result analysis
- `bayesian_optimization`: Optimizes strategy parameters

## Requirements

- Python 3.x
- Libraries: yfinance, pandas, numpy, matplotlib, backtrader, skopt, statsmodels

## Usage

1. Ensure all required libraries are installed
2. Run the Jupyter notebook cells sequentially
3. The final cell will output the best parameters and backtest results

## Results

The system outputs:
- Best pair for trading
- Optimized strategy parameters
- Backtest results including Sharpe Ratio, Total Return, Max Drawdown
- Equity curve plot

## Disclaimer

This project is for educational purposes only. It is not financial advice.

## Future Improvements

- Implement multi-pair trading
- Explore additional optimization techniques
- Incorporate more advanced risk management strategies
