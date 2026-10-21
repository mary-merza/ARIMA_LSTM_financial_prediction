# Financial Forecasting and Rule-Based Recommendation System

This notebook provides a comprehensive solution for financial analysis, including synthetic data generation, anomaly detection, time-series forecasting using ARIMA and LSTM models, and a rule-based financial recommendation system.

View the [publication](https://ieeexplore.ieee.org/document/11253447).

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [Output](#output)

## Introduction

This project aims to demonstrate an end-to-end financial analysis pipeline. It starts by generating synthetic financial data, which is then used to detect anomalies in spending patterns. Subsequently, it employs both statistical (ARIMA) and deep learning (LSTM) models for monthly expense forecasting. Finally, a rule-based recommendation system provides actionable financial advice based on the analyzed data and forecasts.

## Features

- **Synthetic Data Generation**: Creates realistic financial datasets for testing and demonstration.
- **Anomaly Detection**: Identifies unusual spending behaviors using the Isolation Forest algorithm.
- **Time-Series Forecasting**: Predicts future monthly expenses using a hybrid model combining ARIMA and LSTM for improved accuracy.
- **Dynamic Lookback**: LSTM model adapts its lookback window based on data characteristics.
- **Rule-Based Recommendation System**: Generates personalized financial recommendations (e.g., debt management, savings, investment) based on predefined rules and financial metrics.
- **Visualization**: Plots historical expenses and future forecasts for clear interpretation.

## Setup

To run this notebook, ensure you have the necessary libraries installed. You can install them using pip:

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels tensorflow keras
```

## Usage

1.  **Run All Cells**: Execute all cells in the notebook sequentially.
2.  **Data Generation**: The `generate_synthetic_data` function creates a `financial_dataset.csv` if it doesn't already exist.
3.  **Anomaly Detection**: The `detect_anomalies` function will process the financial data and print evaluation metrics (Precision, Recall, F1 Score).
4.  **Forecasting**: ARIMA and LSTM models will generate forecasts for the next 3 months, and the `hybrid_forecast` function will combine their predictions.
5.  **Recommendations**: The `generate_recommendations_llm` function (rule-based) will provide financial advice based on the user's financial context.

## Output

The notebook will output the following:

-   **Anomaly Detection Metrics**: Precision, Recall, and F1 Score for the anomaly detection model.
-   **Financial Forecast**: Predicted monthly expenses for the next three months.
-   **Recommended Financial Actions**: A list of prioritized recommendations with actions and rationales.
-   **Visualizations**: Plots illustrating historical expenses, forecasted expenses, and the dynamic lookback window used by the LSTM model.
