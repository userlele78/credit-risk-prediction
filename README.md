# Debt Repayment Prediction

This repository contains the code and data used in the **Data Science Talent Competition (Round 2)**, where the **Crazy Chipmunk** team implemented machine learning models to predict customers' debt repayment behavior.

[Link to Dataset](https://drive.google.com/file/d/1Ibmg67yrqAHEd3GbbwICfIyEgXOHzpsC/view?usp=sharing)
## Overview

The goal of the project is to differentiate between customers who repay their loans on time and those who don't, using various features from the dataset. The approach focuses on:
- **Feature engineering** to enhance model performance.
- **Data cleaning** and preprocessing to prepare the dataset for modeling.
- **Model evaluation** using performance metrics like **F1 Score** and **ROC-AUC**.

## Problem Definition

The task is to predict whether a customer will repay their loan on time (label 0) or not (label 1). The imbalance between these two classes requires careful handling to avoid biased predictions.

## Approach

### Data Preprocessing
- **Feature Selection:** Remove redundant columns, handle missing values, and normalize data.
- **Feature Engineering:** Created new features to better distinguish between customers who repay and those who don't.
- **Handling Imbalanced Data:** Implemented strategies to manage class imbalance by focusing on key discriminating features.

### Models Used
1. **Gradient Boosting**
2. **XGBoost**
3. **CatBoost**
4. **LightGBM**
5. **Logistic Regression**
6. **Random Forest**

The **Gradient Boosting** and **XGBoost** models performed best based on the ROC-AUC and F1-Score.

## Results

| Model                   | ROC-AUC | F1 Score |
|--------------------------|---------|----------|
| Gradient Boosting         | 0.810   | 0.869    |
| XGBoost                   | 0.808   | 0.868    |
| CatBoost                  | 0.808   | 0.868    |
| LightGBM                  | 0.807   | 0.868    |
| Logistic Regression       | 0.805   | 0.864    |
| Random Forest             | 0.805   | 0.868    |

**Gradient Boosting** showed the highest performance, with good generalization on the test set, indicating that the model is not overfitting.

## Features

- **Data Cleaning:** Removed duplicated and irrelevant features.
- **Outlier Handling:** Some features with extreme values were removed, while others were kept due to their significance for prediction.
- **New Feature Creation:** Additional features like `Diff_in_` and `RATIO_` were created to better capture customer behavior.

## Evaluation Metrics
- **F1 Score:** Balanced measure of precision and recall.
- **ROC-AUC:** Measures the area under the receiver operating characteristic curve, useful for imbalanced datasets.

## Conclusion

The combination of **Gradient Boosting** and **XGBoost** produced the best results for predicting customer repayment behavior. These models efficiently handle the complexity of the dataset and the imbalance between the two classes.
