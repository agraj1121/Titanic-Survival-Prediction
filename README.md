# Titanic Survival Prediction using Random Forest

## Project Overview

This project builds a **Random Forest Classifier** to predict whether a passenger survived the Titanic disaster using passenger information such as age, gender, passenger class, fare, and family details.

The project demonstrates a complete Machine Learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, feature importance analysis, hyperparameter tuning, and performance evaluation.

---

## Objective

Develop a Random Forest classification model capable of predicting passenger survival based on passenger characteristics while applying real-world data preprocessing techniques.

---

## Dataset

- **Dataset:** Titanic Survival Dataset
- **Rows:** 418
- **Columns:** 12

### Features

- PassengerId
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked
- Survived (Target)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Project Workflow

```
Load Dataset
        ↓
Data Inspection
        ↓
Data Cleaning
        ↓
Missing Value Handling
        ↓
Categorical Encoding
        ↓
Exploratory Data Analysis
        ↓
Train-Test Split
        ↓
Random Forest Classifier
        ↓
Model Evaluation
        ↓
Feature Importance
        ↓
GridSearchCV Hyperparameter Tuning
        ↓
Final Evaluation
```

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removed unnecessary columns:
  - PassengerId
  - Name
  - Ticket
  - Cabin
- Filled missing values in the **Age** column using the **median**
- Removed the row containing the missing **Fare** value
- Applied **One-Hot Encoding** to:
  - Sex
  - Embarked
- Verified that the dataset contained no missing values after preprocessing

---

## Exploratory Data Analysis

The following analyses were performed:

- Target class distribution
- Survival by gender
- Survival by passenger class
- Feature distributions
- Correlation heatmap
- Outlier analysis using boxplots

### Key Findings

- The dataset is slightly imbalanced with more passengers who did not survive.
- Female passengers had a significantly higher survival rate than male passengers.
- Passenger class influenced survival outcomes.
- Fare contained several outliers.
- Age also contained a few outliers.
- Gender was the strongest feature related to survival.

---

## Model Used

**Random Forest Classifier**

Train-Test Split:

- Training Set: 80%
- Testing Set: 20%

---

## Model Performance

| Metric | Score |
|---------|------:|
| Accuracy | **1.00** |
| Precision | **1.00** |
| Recall | **1.00** |
| F1 Score | **1.00** |

### Confusion Matrix

| | Predicted 0 | Predicted 1 |
|---|---:|---:|
| **Actual 0** | 53 | 0 |
| **Actual 1** | 0 | 31 |

The model correctly classified every sample in the test dataset.

---

## Feature Importance

| Rank | Feature | Importance |
|------|---------|-----------:|
| 1 | Sex_male | 0.8268 |
| 2 | Fare | 0.0618 |
| 3 | Age | 0.0472 |
| 4 | Parch | 0.0212 |
| 5 | SibSp | 0.0125 |

### Observation

Gender was by far the most influential feature for predicting passenger survival, followed by Fare and Age.

---

## Hyperparameter Tuning

Hyperparameter tuning was performed using **GridSearchCV** with 5-fold cross-validation.

### Tuned Parameters

- n_estimators
- max_depth
- min_samples_split
- min_samples_leaf
- max_features

The tuned model achieved the same performance as the baseline model, indicating that the default Random Forest model was already highly effective for this dataset.

---

## Machine Learning Concepts Covered

- Data Cleaning
- Missing Value Handling
- Feature Selection
- One-Hot Encoding
- Exploratory Data Analysis (EDA)
- Random Forest Classification
- Feature Importance
- Hyperparameter Tuning using GridSearchCV
- Model Evaluation

---

## Project Structure

```
Titanic-Survival-Prediction/
│
├── titanic.ipynb
├── train.csv
└── README.md
```

---

## Future Improvements

- Perform advanced feature engineering using passenger titles extracted from names.
- Create new features such as Family Size and IsAlone.
- Compare Random Forest with XGBoost, Gradient Boosting, and Logistic Regression.
- Evaluate using ROC-AUC and Cross-Validation.
- Deploy the trained model using Streamlit or Flask.

---

## Conclusion

This project demonstrates a complete end-to-end Machine Learning workflow using the Random Forest algorithm. The dataset was successfully cleaned, preprocessed, and analyzed before training the model. The Random Forest Classifier achieved **100% Accuracy, Precision, Recall, and F1 Score** on the test dataset, with feature importance analysis showing that passenger gender was the strongest predictor of survival.

The project highlights the effectiveness of Random Forest for classification tasks while providing practical experience with data preprocessing, exploratory data analysis, model evaluation, and hyperparameter tuning.

---

## Author

**Agraj Shukla**

Machine Learning Portfolio Project – Titanic Survival Prediction using Random Forest