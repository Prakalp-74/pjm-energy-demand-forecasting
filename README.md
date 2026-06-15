# PJM Energy Demand Forecasting

## Project Overview

This project focuses on forecasting electricity demand using historical energy consumption data from the PJM Interconnection region. The goal of this project is to analyze demand patterns, create useful time-based features, and build a machine learning model that can predict future energy demand.

I built this project to practice the complete machine learning workflow, including data cleaning, exploratory data analysis, feature engineering, model training, evaluation, visualization, and model persistence.

---

## Dataset

**Dataset:** PJM Hourly Energy Consumption Dataset

The dataset contains hourly electricity demand records collected over multiple years.

### Main Columns

- Datetime
- PJME_MW (Energy Demand in Megawatts)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

---

## Project Workflow

### 1. Data Cleaning

- Checked missing values
- Checked duplicate records
- Converted Datetime column into datetime format
- Sorted records chronologically

### 2. Exploratory Data Analysis

- Analyzed energy demand over time
- Studied yearly patterns
- Studied monthly patterns
- Compared weekday and weekend demand

### 3. Feature Engineering

Created time-based features:

- Hour
- Day
- Month
- Year
- Day of Week
- Quarter
- Weekend Flag

Created lag features:

- Previous hour demand (1-hour lag)
- Previous 24-hour demand (24-hour lag)
- Previous 7-day demand (168-hour lag)

### 4. Train-Test Split

Performed an 80-20 chronological split without shuffling to preserve the time-series nature of the dataset.

### 5. Model Training

- Trained a Random Forest Regressor
- Generated predictions on the test dataset

### 6. Model Evaluation

Evaluation metrics used:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

#### Results

| Metric | Value |
|----------|----------|
| MAE | 3346.34 |
| RMSE | 4551.57 |

### 7. Visualization

Created:

- Actual vs Predicted graph
- Future Forecast graph

### 8. Model Persistence

Saved the trained Random Forest model using Joblib.

---

## Project Structure

```text
project/
│
├── data/
├── notebooks/
├── images/
│   ├── actual_vs_predicted.png
│   └── future_forecast.png
├── reports/
│   └── model_evaluation_metrics.csv
├── models/
│   └── random_forest_model.joblib
├── requirements.txt
└── README.md
```

---

## Results

The Random Forest model was able to capture the overall trend in energy demand and produced reasonable forecasting performance on unseen data.

- MAE: 3346.34
- RMSE: 4551.57

---

## Visualizations

### Actual vs Predicted

_Add screenshot here_

### Future Forecast

_Add screenshot here_

---

## Future Improvements

- Compare Random Forest with Prophet
- Compare Random Forest with ARIMA
- Perform hyperparameter tuning
- Build a Streamlit dashboard
- Deploy the model as a web application

---

## What I Learned

Through this project, I learned:

- Time-series data preprocessing
- Feature engineering using lag features
- Training forecasting models
- Evaluating regression models
- Saving and loading machine learning models
- Creating forecasting visualizations

This project helped me understand how machine learning can be applied to real-world energy demand forecasting problems.
