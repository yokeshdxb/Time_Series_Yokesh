
# 🪙 Gold Price Prediction Using Time Series (ARIMA & SARIMA Models)

This repository presents a comprehensive **time series forecasting** solution for monthly gold prices utilizing **ARIMA** and **SARIMA** techniques. It also includes an interactive **Streamlit-based application** for model testing, selection, and live forecasting.

---

## 📦 Key Project Highlights

### ✅ Complete Time Series Pipeline:
- Fetching gold price history via **Yahoo Finance**
- **Time-based trend analysis** through rich visualizations
- **STL decomposition** to isolate trend, seasonality, and residuals
- **ADF (Augmented Dickey-Fuller) Test** to assess stationarity
- **Differencing** strategy applied to make the series stationary
- **ACF & PACF charts** to guide parameter selection
- **Model development** with both ARIMA and SARIMA
- **12-month forecasts** generated and visualized
- **AIC/BIC scores** used to evaluate model fit
- **Model serialization** using pickle for reuse

### ✅ Interactive Web Interface via Streamlit:
- Toggle between ARIMA and SARIMA for predictions
- Choose forecast window (up to 12 months)
- Output includes **forecast plots with confidence intervals**
- Inspect model details and historical data directly in the UI

---

## 🗂️ Folder Structure

```
📁 Time_Series_Yokesh/
├── app_time.py                      # Streamlit frontend
├── arima_gold_model_2000_2025.pkl  # Pretrained ARIMA model
├── sarima_gold_model_2000_2025.pkl # Pretrained SARIMA model
├── Yokesh_model_training.ipynb     # Jupyter Notebook for full training process
├── requirements.txt                # Dependency list
└── README.md                       # Project guide
```

---

## 🚀 How to Run This Project

### 1. Clone the Repository

```bash
git clone (https://github.com/yokeshdxb/Time_Series_Yokesh.git)
```

### 2. Install Required Packages

```bash
pip install -r requirements.txt
```

### 3. Launch the Streamlit App

```bash
streamlit run app_time.py
```

---

## 📈 Sample Forecast Output

*Below is a SARIMA-based forecast showing the predicted path (green) along with a 95% confidence interval:*

![Forecast Example](https://github.com/yokeshdxb/Time_Series_Yokesh/main/Sarima_Price_Forecast.png)

---

## 📊 Model Overview

| Model  | AIC/BIC Score | Seasonal Capability | Stationarity Handling | Forecast Scope     |
|--------|---------------|---------------------|------------------------|---------------------|
| ARIMA  | Evaluated     | ❌ No                | Differencing applied   | Suitable short-term |
| SARIMA | Evaluated     | ✅ Yes               | Differencing applied   | Seasonal optimized  |

### 🔍 How to Interpret ACF & PACF:

- ACF with repeating lags → Add seasonal terms
- PACF truncates after lag `p` → Suggests AR component
- ACF truncates after lag `q` → Indicates MA component

---

## 🧪 Sample ADF Test Output

```
ADF Statistic: 0.98
p-value: 0.99
Conclusion: Series is not stationary. Apply differencing.
```

---

## 🧰 Tech Stack

- `Python`
- Libraries: `pandas`, `matplotlib`, `statsmodels`
- Data Retrieval: `yfinance`
- Interface: `Streamlit`
- Model Persistence: `pickle`

---

## 📜 License

This work is distributed under the [MIT License](LICENSE).

---

## 👤 Author Information

Developed by **Yokesh Kumar**  
📧 [yokesh1987@gmail.com](mailto:yokesh1987@gmail.com)  
🌐 [GitHub Profile](https://github.com/yokeshdxb/Time_Series_Yokesh.git)

---

## 🔗 See Also

- Time Series Analysis on PJME & Google Trends

---

## 📌 Required Libraries (`requirements.txt`)

Below are the dependencies needed to run this project:

```
streamlit
pandas
matplotlib
statsmodels
yfinance
python-dateutil
```
