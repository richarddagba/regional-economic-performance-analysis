# Regional Economic Performance Analysis

## Overview

This project analyzes macroeconomic indicators from the World Bank's global economic data (2010-2024) to evaluate regional economic performance, focusing on five high-performing countries based on average GDP. The analysis is split across two Jupyter notebooks:

- **Exploratory Phase**: Handles data loading, exploration, cleaning, and exploratory data analysis (EDA).
- **Forecasting Phase**: Focuses on time-series modeling and forecasting GDP from 2025 to 2030 using baseline (Theta), ARIMA, and Bayesian Structural Time Series (BSTS) models.

The dataset is sourced from Kaggle: [Global Economic Indicators 2010-2025](https://www.kaggle.com/datasets/tanishksharma9905/global-economic-indicators-20102025/data). Key indicators include GDP, inflation (CPI and GDP deflator), unemployment rate, interest rates, GDP growth, current account balance, government finances, gross national income, and public debt.

The goal is to identify trends, compare regional performances, and forecast future GDP for top countries (e.g., United States, China, Japan, Germany, United Kingdom).

### 1. Data Loading and Exploration
* **Data Source:** Loaded the dataset from `world_bank_data_2025.csv` using pandas.
* **Inspection:** Used `df.head()`, `df.tail()`, `df.shape`, `df.info()`, and `df.describe()` to understand the data's dimensions and statistical spread.
* **Integrity Check:** Scan for duplicate entries and missing values.
* **Pattern Recognition:** Identification of country-wise time-series patterns and specific indicators.

### 2. Data Cleaning
* **Feature Selection:** Focused on three main indicators only.
* **Imputation:** Massive impuation of accurate values for the missing values from various sources and applying mean for the ones still missing.


### 3. Exploratory Data Analysis (EDA)
* **Statistical Profiling:** Computed summary metrics for GDP, inflation, and unemployment.
* **Trend Visualization:** Generated line plots and bar charts to visualize historical GDP growth and economic shifts.
* **Correlation Analysis:** Created heatmaps to identify relationships between variables, such as the interaction between GDP and unemployment rate.

* **Regional Comparison:** comparing performance across the top 5 countries based on GDP, GDP per capita and GDP growth

### 4. Time-Series Modeling and Forecasting
* **Data Preparation:** `world_bank_data_2025_cleaned.csv` was loaded and set the 'year' column as the index for time-series processing.
* **Data Splitting:** Divided the data into training and validation sets.
* **Model Implementation:**
    * **Theta Model:** A baseline model using simple exponential smoothing.
    * **ARIMA:** AutoRegressive Integrated Moving Average for univariate forecasting.
    * **BSTS (Bayesian Structural Time Series):** An advanced model incorporating trends, seasonality, and regressors.
* **Model Evaluation:** Compare performance using:
    * **MAPE** (Mean Absolute Percentage Error)
    * **MAE** (Mean Absolute Error)
    * **R2** (Coefficient of Determination)
* **Projection:** Generate and visualize GDP forecasts from **2025 to 2030** with confidence intervals.

## Dependencies

The notebooks require the following Python libraries:

- **pandas** – Data loading, manipulation, cleaning, and reshaping
- **numpy** – Numerical operations and array handling
- **matplotlib** and **seaborn** – Visualization and exploratory data analysis
- **statsmodels** – Time-series modeling (e.g., ARIMA), stationarity tests, and evaluation metrics
- **sklearn** – Metrics for model evaluation (e.g., mean_squared_error, r2_score, mean_absolute_error)

Install the core dependencies with:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn

