# DIABETES ONSET PREDICTION: AN APPLICATION OF SUPERVISED LEARNING MODELS

![Uploading image.png…]()

## Introduction
Diabetes is a group of metabolic disorders characterized by high blood sugar levels over a prolonged period. Symptoms of diabetes can include frequent urination, increased thirst, and increased hunger. If left untreated, diabetes can lead to serious complications such as cardiovascular disease, stroke, chronic kidney disease, foot ulcers, and damage to the eyes. 

This case study utilizes a dataset from the National Institute of Diabetes and Digestive and Kidney Diseases to predict diabetes among female patients of Pima Indian heritage who are at least 21 years old. The goal is to develop a machine learning model that accurately predicts whether a patient has diabetes based on several diagnostic measurements.

## Dataset Description
The dataset comprises medical predictor variables and a target variable, **Outcome**, which indicates whether the patient has diabetes (1) or not (0). The features included are:

1. **Pregnancies**: Number of times pregnant
2. **Glucose**: Plasma glucose concentration measured during an oral glucose tolerance test
3. **Blood Pressure**: Diastolic blood pressure (mm Hg)
4. **Skin Thickness**: Triceps skin fold thickness (mm)
5. **Insulin**: 2-Hour serum insulin level (mu U/ml)
6. **BMI**: Body mass index (weight in kg/(height in m)^2)
7. **Diabetes Pedigree Function**: A function that scores the likelihood of diabetes based on family history
8. **Age**: Age in years
9. **Outcome**: Class variable (0 or 1)

The dataset consists of **768 observation units** and **9 variables**.

## Objective
The primary objective is to build a machine learning model that can accurately predict the presence of diabetes in patients based on the provided features.

## Data Preprocessing

### Handling Missing Values
The dataset contained a total of **652 missing values** distributed across various features. The missing values were imputed using the median of each variable to ensure that the central tendency was maintained without distorting the data distribution.

### Outlier Detection
Outliers were identified in the following features:
- **Pregnancies**: Yes
- **Blood Pressure**: Yes
- **Skin Thickness**: Yes
- **Insulin**: Yes
- **BMI**: Yes
- **Diabetes Pedigree Function**: Yes
- **Glucose**: No
- **Age**: No
- **Outcome**: No

Appropriate techniques, such as boxplots, were utilized to visualize and address outliers in the dataset.

## Feature Engineering
Feature engineering is crucial for enhancing model performance. In this dataset, new variables were created based on **BMI**, **Insulin**, and **Glucose** to capture additional relationships and patterns. 

### Categorical Variable Encoding
To convert categorical variables into numerical values, both Label Encoding and One Hot Encoding methods were applied. This step is essential for enabling the machine learning algorithms to interpret the data correctly.

## Model Building
The cleaned and preprocessed dataset was used to train various machine learning algorithms, including:

Logistic Regression
K-Nearest Neighbors (KNN)
Decision Tree Classifier
Random Forest Classifier
Gradient Boosting Classifier
Support Vector Machine (SVM)
XgBoost
Hyperparameter tuning was performed for each algorithm to improve model performance. This involved optimizing parameters such as learning rate, number of estimators, maximum depth, and others to achieve the best results.

## Conclusion
This analysis demonstrated the importance of data preprocessing, feature engineering, and appropriate modeling techniques in predicting diabetes among Pima Indian women. The XgBoost model achieved the highest score of 91.56%, highlighting its effectiveness for this classification task. The insights derived from the analysis not only contribute to the field of healthcare but also provide a foundation for future research and improvements in diabetes prediction methodologies.
