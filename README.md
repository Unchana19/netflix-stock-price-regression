# Stock Price Prediction

[![Python 3.12.7](https://img.shields.io/badge/python-3.12.7-blue.svg)](https://www.python.org/downloads/release/python-3127/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A machine learning project implementing a custom Gradient Boosting Regression Tree algorithm to predict stock prices.

## Overview

This project aims to predict stock price movements using historical data from the stock market. The implementation uses a custom Gradient Boosting Regression Tree model with several optimizations. The model is designed to provide accurate predictions while maintaining computational efficiency.

## Dataset

The project uses historical stock price data obtained through the [yfinance](https://pypi.org/project/yfinance/) library, which provides easy access to Yahoo Finance data including:
- Opening and closing prices
- High and low prices
- Trading volume
- Adjusted close prices

The data can be customized for any publicly traded stock with a specified date range.

## Requirements

- Python 3.12.7
- Dependencies listed in `requirements.txt`

### Installation

Clone the repository and install the required packages:

```bash
git clone https://github.com/Unchana19/stock-price-prediction.git
cd stock-price-prediction
pip install -r requirements.txt
```

## Model Architecture

The prediction model is based on a custom implementation of Gradient Boosting Regression Trees with the following optimizations:

### 1. Feature Engineering
Added domain-specific features to improve prediction accuracy:
- Technical indicators (Moving Averages, RSI, MACD)
- Market sentiment analysis
- Temporal features
- Volume-based indicators
- Price momentum indicators

### 2. Early Stopping
Implemented early stopping to prevent overfitting by monitoring validation performance:
- Validation error monitoring
- Patience parameter for stopping
- Best model checkpoint saving

### 3. L2 Regularization
Added regularization to control model complexity and improve generalization:
- Leaf weight regularization
- Tree depth control
- Minimum samples per leaf

### 4. Out of Bag Error
Implemented Out of Bag (OOB) error estimation:
- Unbiased performance estimation
- Model validation without separate validation set
- Automatic hyperparameter tuning support

## Evaluation Metrics

The model's performance is evaluated using multiple metrics:
- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- R-squared (R²) score
- Direction Accuracy (percentage of correct price movement predictions)

## Results

![alt text](https://github.com/Unchana19/stock-price-prediction/blob/main/example_result.png?raw=true)