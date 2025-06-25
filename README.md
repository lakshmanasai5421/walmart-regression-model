# Linear Regression Model for Weekly Sales Prediction

This project demonstrates how to build a **Linear Regression model** using **Scikit-learn** to predict `Weekly_Sales` based on key business features like `Temperature`, `Fuel_Price`, `CPI`, and `Unemployment`.

The workflow includes:

---

## 🚀 Objective

To create and evaluate a linear regression model from scratch and using Scikit-learn, and understand how features affect sales predictions.

---

## 📦 Dataset Overview

The dataset includes the following columns:

* **Weekly\_Sales**: Target variable (scaled)
* **Temperature**: Environmental temperature (scaled)
* **Fuel\_Price**: Local fuel prices (scaled)
* **CPI**: Consumer Price Index (scaled)
* **Unemployment**: Unemployment rate (scaled)

---

## 🧠 Project Workflow

### 1. **Data Preparation**

* Load data using pandas
* Apply **feature scaling** (StandardScaler or MinMaxScaler)
* Drop features with no variance (like `Unemployment` if all values are same)

### 2. **Train-Test Split**

* Use `train_test_split()` from Scikit-learn
* Example:

  ```python
  from sklearn.model_selection import train_test_split
  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
  ```

### 3. **Model Training**

* Use `LinearRegression()` from `sklearn.linear_model`
* Fit model on training data

### 4. **Model Evaluation**

* Evaluate using:

  * **Mean Squared Error (MSE)**
  * **R² Score**
* Example output:

  ```
  Mean Squared Error: 0.89
  R² Score: 0.16
  ```

---

## 📉 Observations

* R² score of 0.16 indicates the model isn't explaining much variance
* Negative custom accuracy suggests poor performance
* Features may have too little variance or too much noise

---

## 🔍 Tips for Improving Accuracy

* Drop low-variance or non-informative features
* Use tree-based models like RandomForest or GradientBoosting
* Add polynomial features if you suspect non-linear patterns
* Visualize feature importance
* Use correlation matrix to drop irrelevant columns

---

## ✅ Final Thoughts

This project is a foundational example to understand linear regression, feature scaling, and model evaluation. The same structure can be extended to more complex models and real-world business cases.

