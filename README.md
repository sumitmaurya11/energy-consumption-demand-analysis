# ⚡ Energy Consumption & Demand Analysis using Python

## 📌 Project Overview

This project analyzes household electricity consumption data to identify consumption patterns, peak-demand periods, high-usage events, and relationships between electrical variables.

The project also applies **time-series feature engineering and machine learning** to predict electricity demand and compare model performance.

The analysis was performed using Python and focuses on practical data analysis and machine-learning techniques.

---

## 🎯 Objectives

* Analyze household electricity consumption patterns
* Identify peak electricity-demand hours
* Compare weekday and weekend consumption
* Analyze monthly and daily consumption trends
* Identify unusually high-demand periods
* Study correlations between electrical variables
* Engineer time-series features such as lags and rolling averages
* Build machine-learning models for electricity-demand prediction
* Compare Linear Regression and Random Forest performance

---

## 📊 Dataset

**Dataset:** Individual Household Electric Power Consumption

**Source:** UCI Machine Learning Repository

The dataset contains approximately **2 million minute-level electricity consumption records** collected from a household.

### Main Variables

| Variable                | Description                     |
| ----------------------- | ------------------------------- |
| `Global_active_power`   | Global active power consumption |
| `Global_reactive_power` | Global reactive power           |
| `Voltage`               | Voltage                         |
| `Global_intensity`      | Global current intensity        |
| `Sub_metering_1`        | Sub-metered electricity usage   |
| `Sub_metering_2`        | Sub-metered electricity usage   |
| `Sub_metering_3`        | Sub-metered electricity usage   |
| `Datetime`              | Combined date and time          |

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* Git & GitHub

---

## 📁 Project Structure

```text
Energy-demand-analysis/
│
├── data/
│   ├── raw/
│   │   ├── household_power_consumption.txt
│   │   └── household_power_consumption.zip
│   │
│   └── processed/
│       └── energy_consumption_clean.csv
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   └── 02_energy_analysis.ipynb
│
├── models/
├── reports/
├── src/
│
└── README.md
```

---

# 🔍 Analysis Performed

## 1. Data Understanding & Cleaning

* Loaded the raw electricity consumption dataset
* Handled missing values represented by `?`
* Converted electrical measurements to numeric data types
* Combined `Date` and `Time` into a `Datetime` column
* Created time-based features
* Converted minute-level active power into energy consumption in kWh
* Prepared a cleaned dataset for further analysis

---

## 2. Daily Energy Consumption

Daily electricity consumption was calculated by aggregating minute-level observations.

This helped identify:

* Daily consumption patterns
* Highest-consumption days
* Changes in household electricity usage over time

---

## 3. Peak Demand Analysis

Average electricity demand was analyzed across all 24 hours of the day.

This helped identify:

* Peak-demand hours
* Low-demand periods
* Daily electricity usage patterns

---

## 4. Weekday vs Weekend Analysis

Average electricity demand was compared between weekdays and weekends.

This provides insight into how household electricity usage changes depending on the day type.

---

## 5. Monthly Consumption Analysis

Monthly electricity consumption was calculated to identify:

* Highest-consumption months
* Lowest-consumption months
* Long-term consumption trends

---

## 6. Sub-Metering Analysis

The three sub-metering variables were compared to understand their relative contribution to measured electricity usage.

---

## 7. Correlation Analysis

A correlation matrix was created to study relationships between:

* Active power
* Reactive power
* Voltage
* Current intensity
* Sub-metering variables

A correlation heatmap was also created using Seaborn.

---

## 8. High-Demand Analysis

The **Interquartile Range (IQR)** method was used to identify unusually high electricity-demand observations.

Instead of automatically removing these observations, they were analyzed as potential high-demand events.

---

# 🤖 Machine Learning

## Feature Engineering

The minute-level data was aggregated into hourly observations for machine-learning analysis.

The following features were created:

* Hour
* Day of Week
* Month
* Day
* Weekend indicator
* 1-hour lag
* 24-hour lag
* 7-day lag
* 24-hour rolling average
* 7-day rolling average

Lag and rolling features were shifted to prevent the current observation from being used to predict itself.

---

## Models Used

### 1. Linear Regression

Used as a baseline machine-learning model.

### 2. Random Forest Regressor

Used to capture non-linear relationships between time-based and historical consumption features.

---

## Model Evaluation

The models were evaluated using:

* **MAE — Mean Absolute Error**
* **RMSE — Root Mean Squared Error**
* **R² — R-squared**

A chronological **80/20 train-test split** was used instead of a random split because the dataset represents time-series observations.

This prevents future observations from being used to train the model when evaluating past-to-future prediction performance.

---

# 📈 Key Visualizations

The project includes:

* Daily energy consumption trend
* Top 10 highest-consumption days
* Average demand by hour
* Weekday vs weekend comparison
* Monthly consumption trend
* Sub-metering comparison
* Correlation heatmap
* Electricity-demand distribution
* Random Forest feature importance
* Actual vs predicted electricity demand

---

# 💡 Key Insights

The analysis provides insights into:

* When household electricity demand is highest
* How consumption differs between weekdays and weekends
* Monthly and daily consumption patterns
* Variables strongly associated with active power
* Historical demand patterns useful for prediction
* Features that contribute most to machine-learning predictions

---

# 🚀 Skills Demonstrated

This project demonstrates practical experience in:

**Python**

* Pandas
* NumPy
* Data manipulation
* Data cleaning

**Data Analysis**

* Exploratory Data Analysis
* Descriptive statistics
* Correlation analysis
* Outlier analysis

**Time-Series Analysis**

* Resampling
* Lag features
* Rolling averages
* Time-based train/test splitting

**Machine Learning**

* Feature engineering
* Linear Regression
* Random Forest Regression
* Model evaluation
* Feature importance

**Data Visualization**

* Matplotlib
* Seaborn

---

# 👨‍💻 Author

**Sumit Maurya**

Aspiring Data Analyst / Data Scientist

Skills: Python | SQL | Pandas | NumPy | Tableau | Machine Learning | Data Analysis

---

## ⭐ Project Goal

This project was created as part of my transition into **Data Analytics and Data Science**, with a focus on developing practical skills through real-world datasets and end-to-end analytical projects.
