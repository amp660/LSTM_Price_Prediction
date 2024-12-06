
# Algorithmic Trading Using Technical Indicators

This repository contains a Python-based implementation of an algorithmic trading system. The project includes data preprocessing, feature engineering with technical indicators, and data normalization, creating a strong foundation for backtesting or implementing trading strategies.

---

## Introduction

This project processes financial time series data from multiple assets (e.g., BTCUSD, ETHUSD, S&P500, Gold). It applies technical analysis to generate features for algorithmic trading strategies.

---

## Features

1. **Multi-Asset Support**:
   - Processes datasets for assets like Bitcoin (BTCUSD), Ethereum (ETHUSD), and others.
2. **Feature Engineering**:
   - Includes moving averages, volatility, and Relative Strength Index (RSI).
3. **Data Normalization**:
   - Scales features to a range of [0, 1] using `MinMaxScaler` for compatibility with machine learning models.
4. **Modular Design**:
   - Functions for adding technical indicators and preprocessing ensure code reusability and scalability.

---

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/AlgoTrading.git
   cd AlgoTrading
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook Algo_Trading_final.ipynb
   ```

---

## Data Preprocessing

1. **File Loading**:
   - Data for each asset is loaded from CSV files, indexed by timestamp (`Local time`).
   - Proper handling of missing timestamps ensures clean datasets.

2. **Normalization**:
   - Features like `Close`, `Volume`, and computed indicators are scaled to [0, 1] using `MinMaxScaler`.

---

## Technical Indicators

The following indicators are calculated for each asset:

1. **Moving Averages (MA)**:
   - 10, 50, and 200-period moving averages to capture short-term, medium-term, and long-term trends.

2. **Volatility**:
   - Computed as the rolling standard deviation of percentage changes in `Close` prices over a 20-period window.

3. **Relative Strength Index (RSI)**:
   - Momentum oscillator that measures the speed and change of price movements over a 14-period window.

---

## Scaling and Normalization

- Features are scaled to the [0, 1] range using `MinMaxScaler`, ensuring compatibility with machine learning models and neural networks.

---

## Suggestions for Future Work

1. **Visualization**:
   - Plot technical indicators and price trends to better understand the data.

2. **Backtesting**:
   - Implement a backtesting module to evaluate trading strategies based on the generated features.

3. **Modeling**:
   - Use the processed data for predictive modeling (e.g., LSTMs, decision trees) or reinforcement learning strategies.

4. **Live Trading**:
   - Integrate the system with a trading API (e.g., Alpaca, Binance) for live execution.

---

Feel free to explore, modify, and build upon this project. Contributions are welcome!
