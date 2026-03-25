## 🚀 Open in Google Colab

[Open Notebook](https://colab.research.google.com/drive/1xrMdygUjfVaBLnALdKxdsdADKF1gqrWO?authuser=1#scrollTo=o42gyjuD5boQ)
# Airbnb-price-prediction-Toronto
Airbnb price prediction using real Toronto data with ML models, feature engineering, and model comparison.
# 🏠 Airbnb Price Prediction (Toronto)

## 📌 Project Overview

The goal of this project is to predict Airbnb listing prices in Toronto using real-world data.

The dataset was obtained from Inside Airbnb (CC BY 4.0), which provides publicly available data on Airbnb listings.

---

## 📊 Dataset

* Source: Inside Airbnb
* Location: Toronto
* Rows: ~21,000 listings
* Features: property characteristics, location, reviews, availability

---

## 💡 Problem Statement

Predict listing price based on:

* Location (latitude, longitude, neighbourhood)
* Property characteristics (accommodates, bedrooms, beds, bathrooms)
* Listing details (room type, property type, availability)
* Social proof (reviews and ratings)

---

## ⚙️ Data Preprocessing

* Removed rows with missing target (`price`)
* Cleaned price column (removed `$` and `,`, converted to numeric)
* Applied log transformation to target (`log(price)`) to reduce skewness
* Handled missing values using median imputation
* Extracted numeric values from `bathrooms_text`
* Encoded categorical variables using One-Hot Encoding

---

## 📈 Exploratory Data Analysis

* Price distribution was highly right-skewed
* Majority of listings are low to mid-priced, with a long tail of expensive properties
* Log transformation significantly improved distribution shape

---

## 🤖 Models

The following models were trained and compared:

* Linear Regression (baseline)
* Ridge Regression
* Random Forest Regressor

All models were implemented using a preprocessing pipeline to ensure consistent transformations.

---

## 📊 Results

| Model         | RMSE (log scale) |
| ------------- | ---------------- |
| Random Forest | **0.4007**       |
| Ridge         | 0.4402           |
| Linear        | 0.4405           |

---

## 🔍 Key Findings

* Random Forest outperformed linear models, indicating non-linear relationships in the data
* Linear and Ridge regression performed similarly, suggesting regularization was not a limiting factor
* Location and property features likely interact in complex ways

---

## ⚠️ Limitations

* Dataset contains noise and missing values typical for real-world data
* Some potentially important features (e.g., text descriptions) were not used

---

## 🚀 Future Improvements

* Remove or cap extreme price outliers (e.g., above 99th percentile)
* Experiment with more advanced models (e.g., Gradient Boosting, XGBoost)
* Feature engineering on location (distance to city center, clustering)
* Use text data (listing descriptions) for additional signal

---

## 🧠 Conclusion

This project demonstrates how real-world tabular data requires:

* careful preprocessing
* handling of skewed distributions
* appropriate model selection

Tree-based models performed better due to their ability to capture non-linear relationships.

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib

---
