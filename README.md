# 📊 COVID-19 Spatial Forecasting: Short-Term Prediction at Department Level

## Overview
This project builds a machine learning pipeline to predict short-term COVID-19 positive cases across French departments, using epidemiological, mobility, and socio-economic data.

---

## 🎯 Objective
* Forecast positive COVID-19 cases at a 4-day horizon (t+4).
* Compare model performances: XGBoost, MLP, and LSTM.
* Analyze spatial patterns of model errors (Moran's I spatial autocorrelation).
* Identify the key dynamic and static features driving case evolution.

---

## 🛠 Methodologies Implemented
**Modeling:**
* Ridge and Lasso Regression
* XGBoost Regressor
* Multi-Layer Perceptron (MLP)
* Long Short-Term Memory (LSTM)

**Feature Engineering:**
* Dynamic lag features (up to 7 days history)
* Normalization (StandardScaler)
* Socio-economic variable integration

**Evaluation Metrics:**
* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score
* Pearson Correlation

**Spatial Analysis:**
* Moran's I index to detect spatial autocorrelation in prediction errors.

---

## 📚 Data
**Variables:**
* Epidemiological indicators (positivity rate, reproduction number, ICU occupancy).
* Mobility trends (Google Mobility Reports).
* Socio-economic indicators (unemployment, poverty, median income, population).

**Period:**
* March 2020 – December 2021

**Sources:**
* Santé Publique France (SPF)
* Google Mobility Reports
* INSEE socio-economic statistics

---

## 💼 Forecast Target
* Predict the number of positive COVID-19 cases (t+4) per department.
* Sequence modeling: 7-day input window.

---

## 📈 Key Results
* **Best Model:** LSTM (R² = **0.798**, RMSE = **307.9**).
* **XGBoost:** R² ≈ **0.77**, good generalization.
* **MLP:** R² ≈ **0.59**, slight overfitting observed.
* **Top Features:** Workplace and residential mobility, reproduction number (R), positivity rate.

**Spatial Analysis:**
* Moran's I = **0.42** (p < 0.01), indicating strong positive spatial autocorrelation of prediction errors.

---

## 🛠 Tools and Libraries
* Python 3.9
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* tensorflow / keras
* geopandas
* libpysal
* esda

---

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run `COVID_Spatial_Forecasting.ipynb` sequentially.

---

## 🔮 Future Improvements
* Extend LSTM to predict multiple horizons (t+2 to t+10).
* Integrate GARCH models for better volatility modeling.
* Incorporate copula-based methods for spatial dependency modeling.

---

## 📖 References
* Santé Publique France (SPF) - COVID-19 datasets
* Google Community Mobility Reports
* INSEE socio-economic indicators
* Glasserman, P. (2004). *Monte Carlo Methods in Financial Engineering*. Springer.
* Anselin, L. (1995). *Local Indicators of Spatial Association—LISA*. Geographical Analysis.

---

## 📑 License
This project is for educational purposes only.
