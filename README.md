# Air Passengers Forecasting: ARIMAX and SARIMAX Models

This repository provides an in-depth implementation of **ARIMAX** and **SARIMAX** models for forecasting air passenger traffic using historical data. The project highlights how to preprocess time-series data, assess stationarity, and deploy predictive models, emphasizing the distinction between simple ARIMA models and their seasonal counterparts.

---

## 📖 Overview

Time-series forecasting is vital for strategic decision-making in industries like aviation. This project explores forecasting air passenger traffic using **ARIMAX** (AutoRegressive Integrated Moving Average with Exogenous variables) and **SARIMAX** (Seasonal AutoRegressive Integrated Moving Average with Exogenous variables).

Key objectives of the project:
- Understand and preprocess the time-series dataset.
- Test for stationarity and perform transformations to stabilize variance.
- Train ARIMAX and SARIMAX models for forecasting.
- Evaluate and compare model performance using residual analysis and visualizations.

---

## ✨ Key Features

- **Data Preprocessing**: Handling datetime objects, converting data types, and differencing to achieve stationarity.
- **Stationarity Testing**: Implementing the Augmented Dickey-Fuller (ADF) test.
- **Autocorrelation and Partial Autocorrelation Analysis**: Plotting ACF and PACF graphs to determine model parameters.
- **Model Training**: Building ARIMAX and SARIMAX models tailored to the dataset.
- **Residual Analysis**: Measuring model accuracy through residual plots and error metrics.
- **Forecasting Visualization**: Comparing actual vs. predicted values.

---

## 📊 Data

The dataset used is the classic **Air Passengers Dataset**, which records monthly air passenger counts from **1949 to 1960**.

Key features:
- **Month**: The time period (monthly).
- **#Passengers**: The number of air passengers.

---

## ⚙️ Implementation Steps

### 1. Data Preprocessing
- Convert the `Month` column to datetime format.
- Ensure passenger counts (`#Passengers`) are in `float64` format.
- Set the `Month` column as the index.

### 2. Stationarity Testing
- Use the **Augmented Dickey-Fuller Test** to check if the time series is stationary.
- Apply differencing (shifting by 1, 2, or 12 lags) to stabilize the data and re-test stationarity.

### 3. Plotting ACF and PACF
- Visualize ACF and PACF plots to identify optimal ARIMA/SARIMA parameters.

### 4. Model Training
- **ARIMAX**: Trained on differenced data with parameters `(p=0, d=2, q=0)`.
- **SARIMAX**: Trained with seasonal components and parameters `(p=3, d=0, q=6, s=12)`.

### 5. Forecasting and Visualization
- Predict air passenger counts for test data.
- Plot predictions alongside actual values for comparison.

---

## 📈 Results

- The ARIMAX model yielded higher residuals and poor performance, suggesting a seasonal dataset's incompatibility with standard ARIMA techniques.
- The SARIMAX model significantly outperformed ARIMAX, effectively capturing seasonal trends and providing more accurate predictions.

---

## 🖥️ Technologies Used

- **Python Libraries**: `pandas`, `numpy`, `matplotlib`, `statsmodels`, `scipy`
- **Visualization**: ACF, PACF, and time-series plots
- **Jupyter Notebook**: For interactive model development

---
