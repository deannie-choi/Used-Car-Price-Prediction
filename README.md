# 🚗 Used Car Price Prediction

This project aims to predict the resale price of used cars using real Craigslist listings.  
It uses regression models — primarily XGBoost — to learn patterns in factors like mileage, age, brand, and condition.

The final tuned model achieved an R² score of **0.8235**, predicting prices with a **mean absolute error of ~$3,500**.

---

## 🎯 Objectives

- Explore what features most affect used car prices
- Clean and preprocess raw Craigslist listings
- Engineer useful features such as car age and mileage per year
- Train and tune a high-performing regression model (XGBoost)
- Interpret model results through visualizations and feature importance

---

## 📦 Dataset

- **Source**: [Craigslist Cars and Trucks - Kaggle](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)
- **Size**: ~400,000 car listings across the U.S.
- **Important columns**:  
  `price`, `year`, `odometer`, `manufacturer`, `condition`, `fuel`, `title_status`, `transmission`, `drive`, `type`, `state`, `model`

> ⚠️ **Note**: The raw dataset is not included in this repo.  
> Please download the CSV from Kaggle and place it under `/data/`.

---

## 📁 Project Structure
used-car-price-prediction/
├── notebooks/ # Modular Jupyter Notebooks
│ ├── 01_data_understanding.ipynb
│ ├── 02_eda.ipynb
│ ├── 03_feature_engineering.ipynb
│ ├── 04_model_baseline.ipynb
│ ├── 05_model_tuned.ipynb
│ └── 06_feature_importance_and_insights.ipynb
├── .gitignore
├── README.md
└── requirements.txt

---

## 🧪 Final Model Performance (XGBoost Tuned)

| Metric | Value        |
|--------|--------------|
| MAE    | \$3,504.86   |
| RMSE   | \$6,111.42   |
| R²     | **0.8235** ✅ |

Model was tuned using `RandomizedSearchCV` over 50 parameter combinations.

---

## 📊 Key Visualizations

### 📌 Price Distribution  
![price_distribution](figures/price_distribution.png)

### 📌 Price vs Year  
![price_vs_year](figures/price_vs_year.png)

### 📌 Price vs Odometer  
![price_vs_odometer](figures/price_vs_odometer.png)

### 📌 Feature Importance  
![feature_importance](figures/feature_importance.png)

---

## 🧱 Jupyter Notebooks Overview

| Notebook | Description |
|----------|-------------|
| `01_data_understanding.ipynb` | Load dataset and check structure, nulls, data types |
| `02_eda.ipynb` | Visualize distribution of price, year, mileage, and condition |
| `03_feature_engineering.ipynb` | Create `car_age`, encode categorical columns, and add derived features |
| `04_model_baseline.ipynb` | Train a baseline XGBoost model and evaluate |
| `05_model_tuned.ipynb` | Perform hyperparameter tuning with RandomizedSearchCV |
| `06_feature_importance_and_insights.ipynb` | Plot feature importance and summarize insights |

---

💡 What I Learned
- How to clean and explore messy real-world data

- Why log-transforming skewed variables like price improves regression

- How to engineer interpretable features like car_age and mileage_per_year

- The importance of encoding and simplifying categorical variables

- The value of hyperparameter tuning in boosting model performance

👤 Author
Dean Choi
📧 cdh0118@gmail.com
🔗 LinkedIn
