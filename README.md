# House Price Prediction | Machine Learning Regression

A machine learning project focused on predicting residential house prices using regression algorithms. This project explores the complete machine learning workflow, from exploratory data analysis and data preprocessing to model development, hyperparameter tuning, and performance evaluation.

## Project Overview

This project uses the **House Prices – Advanced Regression Techniques** dataset from Kaggle to develop and compare different machine learning regression models.

The main objective is to investigate how different regression algorithms perform and whether techniques such as feature selection, hyperparameter tuning, and numerical feature scaling can improve prediction performance.

## Dataset

- **Source:** [Kaggle – House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)
- **Original training records:** 1,460
- **Original features:** 80 input features
- **Target variable:** `SalePrice`

The dataset contains residential property information, including overall quality, living area, construction year, garage information, neighbourhood, and other characteristics.

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Dataset inspection and statistical analysis.
- Missing-value investigation.
- Outlier detection using the Interquartile Range (IQR) method.
- Sale price distribution analysis.
- Numerical feature correlation analysis.
- Feature-selection investigation.

### 2. Data Preprocessing
- Training and testing dataset splitting.
- Duplicate removal.
- Missing-value handling.
- Categorical feature encoding:
  - Ordinal Encoding
  - Binary Encoding
  - One-Hot Encoding
- Numerical missing-value imputation.
- Outlier analysis and handling.

### 3. Model Development

Four baseline regression algorithms were investigated:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Support Vector Regression (SVR)

Further experiments investigated Ridge and Lasso Regression.

### 4. Model Optimization

The following experiments were conducted:

- Hyperparameter tuning using GridSearchCV.
- RandomizedSearchCV for Random Forest optimization.
- Five-fold cross-validation.
- Feature selection based on Pearson correlation.
- Numerical feature scaling using StandardScaler.

### 5. Model Evaluation

Models were evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Coefficient of Determination (R²)

## Results

The tuned Random Forest Regressor achieved the best reported performance.

| Metric | Result |
|---|---:|
| R² Score | 0.8877 |
| MAE | 17,562.65 |
| RMSE | 29,497.17 |

**Best-performing approach:** Random Forest with hyperparameter tuning using all available features.

## Key Findings

- Random Forest consistently achieved the strongest predictive performance.
- Hyperparameter tuning produced a modest improvement over the baseline model.
- Removing features based on weak individual Pearson correlations did not improve performance.
- Numerical feature scaling produced similar results for Random Forest.
- Feature selection combined with scaling did not outperform using all features.

## Technologies and Tools

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## Project Report

The complete academic report is available in the `reports/` directory.

## Future Improvements

- Experiment with XGBoost and LightGBM.
- Apply additional feature engineering.
- Investigate Bayesian hyperparameter optimization.
- Explore logarithmic transformation of the target variable.
- Apply SHAP for model interpretability.
- Evaluate generalization on additional housing datasets.

## Author

**Abdallah Idris Benseghir**

Master's Student in Artificial Intelligence  
Sunway University, Malaysia

**Academic Module:** MAI5043 – Applied Machine Learning
