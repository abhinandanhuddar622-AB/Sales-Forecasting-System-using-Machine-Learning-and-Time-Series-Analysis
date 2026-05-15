# 📊 Sales Forecasting System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=flat-square&logo=scikit-learn)
![Statsmodels](https://img.shields.io/badge/Statsmodels-ARIMA-4B8BBE?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

> Predict future retail sales using ARIMA, Random Forest, and Linear Regression with full time series analysis pipeline.

---

## 📌 What is this project?

A complete **end-to-end Sales Forecasting System** that takes historical retail data and predicts future sales. It covers everything — data generation, cleaning, visualization, model training, evaluation, and 30-day forecasting with business insights.

---

## 🎯 Objectives

- Predict future sales (daily / weekly / monthly)
- Identify seasonal trends and peak demand periods
- Compare multiple forecasting models
- Generate actionable inventory planning insights

---

## ❗ Problem Statement

Businesses suffer from:
- Inaccurate manual sales predictions
- Overstock or stockout situations
- No visibility into seasonal demand patterns

**Solution:** Automate prediction using ML and time series models.

---

## 💡 Proposed Solution

| Input | Process | Output |
|-------|---------|--------|
| Historical sales CSV | ARIMA + ML models | Future sales forecast |
| Date, product, store data | Feature engineering | 30-day prediction chart |
| Promotions, holidays | Model evaluation | Business insights report |

---

## 🛠️ Tech Stack

| Tool | Use |
|------|-----|
| Python 3.8+ | Core language |
| Pandas & NumPy | Data handling |
| Matplotlib & Seaborn | Visualization |
| Statsmodels | ARIMA, decomposition |
| Scikit-learn | Random Forest, Linear Regression |
| Jupyter Notebook | Development environment |

---

## 📁 Dataset

Auto-generated `sales_data.csv` — **4,380 rows**, 2 years (2022–2023), 3 products × 2 stores.

| Column | Description |
|--------|-------------|
| `Date` | Sales date |
| `Product_ID` | P001, P002, P003 |
| `Store_ID` | S001, S002 |
| `Units_Sold` | Quantity sold |
| `Revenue` | Units × Price |
| `Promotion` | 1 = active, 0 = none |
| `Holiday` | 1 = holiday, 0 = normal |

**Built-in patterns:** +50% holiday boost · +40% Nov–Dec · +20% weekends · +30% promotions

---

## 🏗️ System Flow

```
Data Collection → Preprocessing → EDA → Decomposition
      → Feature Engineering → Model Training → Forecast → Insights
```

---

## 📐 Methodology

| Step | Action |
|------|--------|
| 1 | Collect / load historical sales data |
| 2 | Clean missing values, parse dates, remove outliers |
| 3 | EDA — trend charts, seasonality, revenue breakdown |
| 4 | Decompose series → Trend + Seasonality + Noise |
| 5 | Engineer lag (1/7/14 days) and calendar features |
| 6 | Train ARIMA, Random Forest, Linear Regression, Moving Average |
| 7 | Evaluate with MAE, MSE, RMSE |
| 8 | Forecast next 30 days + generate business report |

---

## 🤖 Models

### ARIMA (5, 1, 2)
Classical time series model. No external features needed.
```
y_t = c + φ₁·y_(t-1) + ... + φ₅·y_(t-5) + θ₁·ε_(t-1) + θ₂·ε_(t-2) + ε_t
```

### Random Forest ⭐ Best
100 decision trees using lag + calendar + event features.

### Linear Regression
Simple ML baseline using the same feature set.

### Moving Average
Baseline — forecast = mean of last 7 days.

---

## 📏 Evaluation Metrics

| Metric | Meaning |
|--------|---------|
| MAE | Average absolute error |
| MSE | Penalizes large errors |
| RMSE | Error in same unit as sales — lower is better |

---

## 🗂️ Project Structure

```
sales-forecasting-system/
├── Sales_Forecasting_System.ipynb  ← Main notebook (13 steps)
├── sales_data.csv                  ← Dataset (4,380 rows)
├── requirements.txt                ← Dependencies
├── .gitignore                      ← Git ignore rules
└── README.md                       ← This file
```

---

## 🚀 Getting Started

```bash
# 1. Clone
git clone https://github.com/YOUR_USERNAME/sales-forecasting-system.git
cd sales-forecasting-system

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run
jupyter notebook Sales_Forecasting_System.ipynb
```

> **Google Colab:** Upload the `.ipynb` + `sales_data.csv` and run directly — no setup needed.

---

## 📓 Notebook Steps

| # | Step | Description |
|---|------|-------------|
| 0 | Setup | Import libraries |
| 1 | Create Dataset | Generate `sales_data.csv` |
| 2 | Load & Explore | Shape, dtypes, missing values |
| 3 | EDA | Trend, seasonality, revenue charts |
| 4 | Preprocessing | Aggregate + lag + calendar features |
| 5 | Decomposition | Trend + Seasonality + Noise plot |
| 6 | Train/Test Split | Last 60 days = test |
| 7 | ARIMA | Train, forecast, plot |
| 8 | Linear Regression | Train, forecast, plot |
| 9 | Random Forest | Train, forecast, plot |
| 10 | Moving Average | 7-day rolling baseline |
| 11 | Evaluation | MAE/MSE/RMSE comparison |
| 12 | Future Forecast | Next 30 days prediction |
| 13 | Business Insights | Stock recommendations |

---

## 📊 Expected Output

- Daily sales trend & monthly seasonality charts
- Time series decomposition (Trend / Seasonality / Noise)
- Forecast vs Actual plots for all 4 models
- Model comparison table (MAE, MSE, RMSE)
- 30-day future forecast chart
- Business insights: peak day, safety stock, promo suggestions

---

## ✅ Advantages

- Replaces manual, error-prone forecasting
- Detects seasonal patterns automatically
- Reduces overstock and stockout losses
- Reusable on any retail dataset with same format

---

## ⚠️ Limitations

- Needs sufficient historical data (1+ year recommended)
- Sensitive to sudden market disruptions not in training data
- ARIMA requires stationary data (differencing applied)

---

## 🔮 Future Enhancements

- [ ] Facebook Prophet model integration
- [ ] LSTM deep learning model
- [ ] Streamlit web dashboard
- [ ] Real-time data pipeline
- [ ] ERP / inventory system integration
- [ ] Multi-store independent forecasting
- [ ] REST API for forecast serving

---

## 🏁 Conclusion

This project demonstrates a **full data science pipeline** — from raw data generation to deployable forecasts. It compares 4 models, identifies the best performer, and converts predictions into direct business recommendations for inventory planning.

---


## 👤 Author

**Abhinandan V Huddar**
📧 abhinandanhuddar622@gmail.com · [LinkedIn](https://www.linkedin.com/in/abhinandan-v-huddar-79a29937a) · [GitHub](https://github.com/abhinandanhuddar622-AB)

---

⭐ **Star this repo if it helped you!**
