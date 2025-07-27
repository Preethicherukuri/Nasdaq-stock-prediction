# 📈 Stock Market Prediction using NASDAQ Index

This project applies machine learning to predict the **next day's NASDAQ Composite Index movement** (up/down) using historical data fetched via Yahoo Finance. It demonstrates data cleaning, feature engineering, model training, backtesting, and evaluation — all in one notebook.

---

## 🧠 Project Overview

- **Data Source**: Yahoo Finance via [`yfinance`](https://pypi.org/project/yfinance/)
- **Target**: Predict if NASDAQ will open **higher** tomorrow than today
- **Model Used**: `RandomForestClassifier` (from Scikit-Learn)
- **Backtesting Strategy**: Sliding window over historical data
- **Feature Engineering**:
  - Rolling average ratios over multiple horizons (2, 5, 60, 250, 1000 days)
  - Trend indicators based on target label sum

---

## 📂 Project Structure
```
nasdaq-stock-prediction/
│
├── Stock market prediction using NASDAQ Index.ipynb   # Main Jupyter notebook
├── requirements.txt                                   # Python dependencies
└── README.md                                          # Project documentation

```
---

## 📦 Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/nasdaq-stock-prediction.git
cd nasdaq-stock-prediction
pip install -r requirements.txt
```

## ▶️ Run the Notebook
Launch Jupyter and open the notebook:
```bash
jupyter notebook "Stock market prediction using NASDAQ Index.ipynb"
```
The notebook includes:
- Data fetching and preprocessing
- Feature creation (ratios and trend indicators)
- Model training and evaluation
- Backtesting strategy for time-series validation

## 📊 Results Summary

- Precision Score: ~0.56 to 0.60
- Backtest Accuracy: Evaluated over several time windows
- Balanced Predictions: Threshold tuned to optimize precision (>= 0.6)

## 🔧 Dependencies

Main libraries used:
- yfinance
- pandas
- numpy
- scikit-learn
- matplotlib

## 📌 Notes

- Data is fetched live using yfinance; no dataset files are stored.
- The model is for educational purposes and does not provide financial advice.
- You can easily expand this model with:
  - Technical indicators (e.g., RSI, MACD)
  - Deep learning models
  - Real-time prediction dashboards

