
# DoorDash Predictive Modeling Project – README

## 1. Dataset Overview
This project uses the **DoorDash Delivery Dataset**, which includes operational and behavioral features related to delivery performance.  
Key variables include:

- Delivery duration, delivery distance, order value  
- Pickup and drop-off coordinates  
- Wait time, preparation time, and other operational timestamps  
- Rider availability and market-level conditions  
- Engineered features such as estimated travel speed  

The dataset contains a large number of observations, making it suitable for machine learning–based regression.

---

## 2. Problem Statement
The goal of this project is to **predict DoorDash delivery duration** using available operational data.  
This is important for improving ETA accuracy, optimizing driver allocation, and enhancing customer experience.

---

## 3. Methodology

### 3.1 Preprocessing
- Cleaning missing values  
- Outlier removal  
- One-hot encoding categorical variables  
- Standardization of continuous features  
- Feature engineering  
- Train–test split  

### 3.2 Models Evaluated
- Linear Regression (baseline)  
- Ridge & Lasso Regression  
- Random Forest  
- Gradient Boosting  
- XGBoost  

### 3.3 Hyperparameter Tuning
Tuning with **GridSearchCV**, optimizing:
- n_estimators  
- max_depth  
- learning_rate  
- regularization parameters  

### 3.4 Why the Best Method Worked
Gradient Boosting / XGBoost performed best due to:
- Ability to model nonlinear relationships  
- Robustness against noisy and high-dimensional data  
- Strong generalization performance  
- Useful feature importance outputs  

---

## 4. Results

### 4.1 Evaluation Metrics
- MAE  
- MSE  
- RMSE  
- R² Score  
- 5-fold Cross-Validation averages  

### 4.2 Cross-Validation Summary
5-fold CV confirmed the model's stability and generalization ability.

---

## 5. Conclusions

### Why We Chose the Final Model
- Best predictive performance  
- Lowest error across metrics  
- Stability across folds  
- Handles complex interactions well  

### Limitations
- Sensitive to data drift  
- Lacks real-time features like traffic or weather  
- Assumes the dataset is representative across markets  

---

## 6. How to Use the Notebook

### Requirements
```
pandas
numpy
scikit-learn
matplotlib
seaborn
xgboost
```

### Running
1. Open `CSM148_DoorDash_Project.ipynb` in Google Colab  
2. Upload dataset or mount Google Drive  
3. Run all cells in order  
4. Outputs include preprocessing, model training, hyperparameter tuning, and evaluation  

---

## 7. Repository Structure
```
|–– README.md  
|–– CSM148_DoorDash_Project.ipynb  
|–– data/  
|     └── dataset.csv  
|–– plots/  
|–– models/
```
