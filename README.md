# Food-delivery-prediction
Predicting food delivery time using machine learning (Linear &amp; Logistic Regression)

## 📌 Project Objective

The main goal is to build predictive models that:
- **Estimate the time (in minutes)** required to deliver food.
- **Classify** deliveries into **Fast (≤ 30 mins)** or **Delayed (> 30 mins)**.

This helps improve delivery logistics, enhance customer satisfaction, and optimize agent performance.

---

## 🗂️ Dataset Overview

- **Source**: `Food_Delivery_Time_Prediction.csv`
- **Records**: 45,000+
- **Key Features**:
  - Categorical: `Type_of_order`, `Type_of_vehicle`
  - Numerical: `Delivery_person_Ratings`, `Age`
  - Geolocation: `Restaurant_latitude`, `Delivery_location_latitude`, etc.
  - Target for regression: `Time_taken(min)`
  - Engineered feature: `Distance_km` (using Haversine formula)

---

## 🧹 Data Preprocessing

- Handled missing values (mean/mode imputation)
- One-Hot Encoding for categorical variables
- Feature Engineering:
  - Calculated `Distance_km` from geo-coordinates
- Standardized continuous variables

---

## 📊 Exploratory Data Analysis (EDA)

- **Correlation Analysis**:
  - Delivery time ↑ with distance and traffic
  - Delivery time ↓ with higher ratings
- **Visualizations**: 
  - Boxplots, scatter plots, heatmaps
- **Outlier Detection**:
  - Handled extreme delays using boxplot logic

---

## 🤖 Machine Learning Models

### 1️⃣ Linear Regression (for predicting time)
- **Target**: `Time_taken(min)`
- **Performance**:
  - `R² Score`: 0.82
  - `MSE`, `MAE` also used

### 2️⃣ Logistic Regression (for classification)
- **Target**: Fast (1) vs Delayed (0)
- **Performance**:
  - Accuracy: 91%
  - ROC AUC: 0.85
  - F1 Score, Precision, Recall evaluated

---

## 📈 Key Insights

1. 🚦 **Distance** is the strongest predictor → Route optimization recommended
2. 🕒 Delivery delays increase during rush hours → Schedule more agents
3. 👨‍✈️ Poor delivery ratings → More delays → Recommend agent training
4. 🛵 Bikes outperform cars in short-distance deliveries

---

## 🧰 Technologies Used

- Python
- Jupyter Notebook
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (ML models)
- Haversine formula (for distance)
- Logistic & Linear Regression
