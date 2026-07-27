# Mp-Online-Assignment-5

# Employee Attrition Prediction using Decision Tree and Random Forest

**Author:** Sambhav Chhayala  

**Registration Number:** 23BCE10380 

**Application Number:** IN26011187

**Batch Number:** 2B

**Email ID:** sambhav.chhayala@gmail.com  

## Objective
The goal of this project is to build and compare Decision Tree and Random Forest classification models to predict employee attrition based on demographic, compensation, and job-related attributes[cite: 2].

## Dataset Link
- [Kaggle: IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)[cite: 2]

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `kaggle`

## Methodology
1. **Data Understanding**: Identified numerical and categorical attributes, confirming `Attrition` as the binary target variable[cite: 2].
2. **Data Preprocessing**:
   - Verified zero missing values[cite: 2].
   - Dropped constant/non-informative features (`EmployeeCount`, `EmployeeNumber`, `Over18`, `StandardHours`)[cite: 2].
   - Encoded binary target `Attrition` (`Yes`: 1, `No`: 0)[cite: 2].
   - One-hot encoded categorical features (`pd.get_dummies`)[cite: 2].
   - Split dataset into 80% training and 20% testing sets using stratified sampling[cite: 2].
3. **Model Development**: Trained a Decision Tree Classifier and a Random Forest Classifier (100 estimators)[cite: 2].
4. **Model Evaluation**: Evaluated using Accuracy, Precision, Recall, F1-Score, Confusion Matrices, and Feature Importance analysis[cite: 2].

## Results

| Metric | Decision Tree | Random Forest |
| :--- | :--- | :--- |
| **Accuracy** | 81.79% | **85.05%** |
| **Precision** | 40.91% | **70.00%** |
| **Recall** | **30.51%** | 11.86% |
| **F1-Score** | **34.95%** | 20.29% |

## Model Comparison
- **Accuracy & Precision**: Random Forest outperformed Decision Tree in accuracy (85.05%) and precision (70.00%), making significantly fewer false positive errors[cite: 2].
- **Recall**: Decision Tree captured more actual attrition cases (Recall: 30.51%) than standard Random Forest (11.86%), which biased predictions toward the majority class due to dataset imbalance[cite: 2].
- **Key Factors**: Feature importance analysis indicated that `MonthlyIncome`, `Age`, and `TotalWorkingYears` are the primary drivers of attrition[cite: 2].

## Conclusion
Random Forest provides superior generalization ability over single decision trees by combining predictions across an ensemble of decorrelated decision trees[cite: 2]. While single decision trees suffer from high variance and overfitting, random forests are less interpretable ("black-box")[cite: 2]. Addressing class imbalance via class weighting or SMOTE would further improve Random Forest's recall on employee churn[cite: 2].
