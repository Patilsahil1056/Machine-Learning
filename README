# Rainfall Prediction using Machine Learning

A machine learning project to predict daily rainfall intensity in Austin using historical meteorological data. This repository documents the transition from linear models to non-linear ensemble methods to improve prediction accuracy.

## 🚀 Overview
Predicting rainfall is a complex regression task due to **zero-inflation** (many days with no rain) and extreme outliers (heavy storms). This project focuses on handling these challenges using the **Random Forest Regressor** to move from negative $R^2$ scores to a more stable, generalized model.

## 📂 Dataset Information
The model is trained on historical weather data for **Austin** from **January 1, 2019, to July 22, 2023**.

* **Filename:** `Austin-2019-01-01-to-2023-07-22.csv`
* **Total Records:** 1,664 daily observations
* **Target Variable:** `precip` (Precipitation in mm/inches)
* **Key Features used:**
    * **Temperature:** `temp`, `tempmax`, `tempmin`
    * **Atmospheric:** `humidity`, `dew`, `sealevelpressure`, `cloudcover`
    * **Wind:** `windspeed`, `winddir`, `windgust`
    * **Solar:** `solarradiation`, `uvindex`

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`
* **Environment:** Anaconda / Jupyter Notebook

## 📈 Model Evolution & Performance
During development, the model underwent several tuning phases:

| Stage | Model | RMSE | $R^2$ | Observation |
| :--- | :--- | :--- | :--- | :--- |
| **Initial** | Linear Regression | 0.23 | Negative | Failed to capture non-linear rain patterns. |
| **Mid-Tune** | Random Forest (Default) | 0.30 | -0.50 | Heavy overfitting; memorized noise in the data. |
| **Final** | Optimized Random Forest | 0.29 | +0.10 | Stabilized using `min_samples_leaf` and `max_depth`. |

### Key Improvements:
* **Handling Overfitting:** Implemented `min_samples_leaf=15` and `max_depth=5` to prevent the trees from memorizing specific outliers.
* **Feature Diagnostic:** Used Feature Importance plots to identify which weather variables (e.g., Humidity, Cloud Cover) were the strongest predictors.

## 📊 Visualizations
### 1. Actual vs. Predicted
This plot shows how well the model's predictions align with reality. The red dashed line represents a perfect prediction ($y = x$).

### 2. Residual Analysis
The residual plot was used to detect bias. A random distribution of points around the zero-line indicates a healthy model, while patterns suggest the model is struggling with zero-inflated data.

## 💻 How to Run
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/yourusername/rainfall-prediction.git](https://github.com/yourusername/rainfall-prediction.git)
