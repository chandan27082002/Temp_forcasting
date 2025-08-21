🌡️ Temperature Forecasting Project

📌 Abstract
This project focuses on temperature forecasting using historical weather data. Various models were implemented, including traditional statistical methods like AR, MA, ARMA, and advanced deep learning models such as RNN, LSTM, and GRU. Through extensive experimentation, GRU emerged as the most accurate model, delivering strong performance on both training and test datasets. The goal is to provide reliable regional temperature forecasts that support real-world applications like disaster management, agriculture, and transport.

❓ Problem Statement
Accurate and region-specific temperature forecasting is critical for several sectors. However, existing models often fall short due to the non-linear, dynamic nature of atmospheric conditions. This study aims to develop a robust, deep-learning-based forecasting system capable of modeling and predicting temperature with high accuracy and generalization.

📂 Dataset Description
Source: National Centers for Environmental Information (NCEI)

- Size: 3,597 daily observations across multiple weather stations.

- Attributes: 29 columns, including temperature, humidity, wind speed, pressure, visibility.

- No Missing Values.

- Suitable for Regional Forecasting.

🧠 Methodology
🔹 1. Data Preprocessing
Feature engineering: day, month, season, lags

Data normalization

Stationarity test using Dickey-Fuller (p-value < 0.05 confirms stationarity)

🔹 2. Models Implemented
Statistical Models:

- Naive Forecast (Baseline)

- AR (Autoregressive)

- MA (Moving Average)

- ARMA

- Deep Learning Models:

- RNN

- LSTM

- GRU

🔹 3. Model Evaluation Metrics
MAE: Mean Absolute Error

MSE: Mean Squared Error

RMSE: Root Mean Squared Error

R²: Coefficient of Determination

📊 Model Comparison Table
## 📊 Model Comparison Table

| Model         | Train MAE | Train MSE | Train R² | Test MAE | Test MSE | Test R² |
|---------------|-----------|-----------|----------|----------|----------|---------|
| Naive         | 4.870     | 42.06     | 0.880    | 4.30     | 32.81    | 0.870   |
| RNN           | 4.620     | 35.82     | 0.900    | 4.21     | 29.46    | 0.890   |
| LSTM          | 4.541     | 35.316    | 0.897    | 4.137    | 29.092   | 0.887   |
| **GRU (Best)**| 4.570     | 35.50     | 0.900    | **4.13** | **28.74**| **0.890** |


📈 Forecast (Jan 1 – Jan 30, 2025)
Forecasts generated using Naive, RNN, LSTM, and GRU models. GRU shows the closest alignment to actual temperature trends.

## 📅 Temperature Forecasts (Jan 1 – Jan 30, 2025)

| Date       | Naive | RNN   | LSTM  | GRU   |
|------------|-------|-------|-------|-------|
| 2025-01-01 | 33.7  | 32.73 | 32.78 | 32.61 |
| 2025-01-02 | 33.7  | 34.18 | 33.71 | 34.06 |
| 2025-01-03 | 33.7  | 34.16 | 34.07 | 34.23 |
| 2025-01-04 | 33.7  | 34.70 | 34.23 | 34.04 |
| 2025-01-05 | 33.7  | 35.16 | 34.27 | 33.93 |
| ...        | ...   | ...   | ...   | ...   |
| 2025-01-30 | 33.7  | 38.44 | 32.25 | 32.68 |



📌 Final Conclusion
Among all models tested, the GRU model outperforms others in terms of accuracy, adaptability, and generalization. With the lowest MAE and MSE and a high R² score, it stands out as the best candidate for temperature forecasting. Future work may include:

Tuning with additional hyperparameters

