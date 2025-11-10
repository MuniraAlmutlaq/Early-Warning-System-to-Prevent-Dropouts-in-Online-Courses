# ⚠️ Developing an Early Warning System Using AI Techniques to Prevent Dropouts in Online Courses

The project encompasses a comprehensive process of data preparation, exploratory analysis, feature engineering, and the training and evaluation of various machine learning classification models.

---

## 🚀 Project Overview

The primary goal of this project is to build a predictive model that identifies students at high risk of dropping out of a MOOC. This allows for proactive intervention strategies.

---

## 💾 Data Preparation Phase

This phase processes the raw `Courses.csv` dataset, which was found to contain **641,138 entries** and **21 columns**.

### Key Steps:

1.  **Target Variable Engineering:** A new binary target variable, `dropout`, was created based on the existing course completion status (`certified`).
2.  **Missing Value Imputation:**
    * The categorical feature `gender` was imputed by randomly sampling from the existing non-null values.
    * Numerical features such as `nevents` and `nchapters` were also systematically imputed.
3.  **Exploratory Data Analysis (EDA):** In-depth analysis was conducted to understand feature distributions, correlations, and the nature of the target variable.

---

## ⚙️ Models Development Phase

This phase focuses on training, optimizing, and evaluating classification models to predict the engineered `dropout` status.

### Model Pipeline

1.  **Dependency Installation:** Key machine learning libraries, including `catboost`, were installed and imported.
2.  **Class Imbalance Handling:** To mitigate the severe class imbalance in the target variable, an **undersampling** technique was applied. The majority class (dropouts) was sampled down to match the size of the minority class (non-dropouts), resulting in a balanced training set.
3.  **Model Evaluation:** The following classification models were evaluated using techniques like cross-validation and hyperparameter tuning:
    * **CatBoost Classifier**
    * **Gradient Boosting Classifier (GB)**
    * **Multi-Layer Perceptron (MLP) Classifier**

### Results Summary

The models were highly effective on the balanced dataset, with the final optimized classifiers reporting very strong performance across key metrics such as **Precision, Recall, F1-Score, and Accuracy**.
