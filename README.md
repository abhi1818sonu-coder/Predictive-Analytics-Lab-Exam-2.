# Predictive-Analytics-Lab-Exam-2.
Objective

The aim of this lab exam is to perform a binary classification task using an appropriate machine learning algorithm. The project involves conducting Exploratory Data Analysis (EDA), developing a classification model, visualizing the decision boundary, and evaluating the model’s performance.

Dataset Description

The dataset consists of the following variables:

Feature1 (Numerical)

Feature2 (Numerical)

Target (Categorical: Yes / No)

The original dataset contained 1020 observations.

During preprocessing:

20 rows with missing values in the Target column were removed

1 extreme outlier (Feature1 = 10000) was eliminated

After cleaning, the final dataset used for analysis contained 999 samples.

Exploratory Data Analysis (EDA)

The following steps were carried out:

Data Inspection

Verified data types of all variables

Generated descriptive statistics

Identified missing values

Handling Missing Values

Rows with missing Target values were removed

Outlier Detection

The Interquartile Range (IQR) method was applied to Feature1

A significant outlier (Feature1 = 10000) was removed

Class Distribution

No: 784 samples

Yes: 215 samples

Class imbalance ratio ≈ 3.65 : 1

Visualizations

Bar plot for class distribution

Histograms with KDE for feature distribution

Boxplots grouped by class

Scatter plot (Feature1 vs Feature2)

Correlation heatmap

Correlation with Target

Feature1 correlation: -0.044

Feature2 correlation: -0.008

Both features exhibit very weak correlation with the target variable.

Model Building
Algorithm Used: Logistic Regression
Reason for Selection

Suitable for binary classification tasks

Provides interpretable coefficients

Outputs class probabilities

Enables visualization of decision boundaries

Preprocessing Steps

Applied stratified 80/20 train-test split

Used StandardScaler to normalize features

Addressed class imbalance using class_weight = 'balanced'

Cross-Validation (5-Fold Stratified)
Metric	Value
CV Accuracy	0.5215 ± 0.0325
CV ROC-AUC	0.5279 ± 0.0267

The model performance is close to random guessing (~0.5), suggesting weak relationships between features and the target.

Decision Boundary

The decision boundary was visualized in the original feature space:

The background represents predicted probability P(Yes)

The dashed boundary corresponds to P = 0.5

Data points are plotted according to their class labels

Observation

The boundary appears almost linear and fails to clearly separate the classes, indicating limited predictive capability.

Model Evaluation (Test Set)
Metric	Value
Accuracy	55.50%
Precision (Yes)	0.2745
Recall (Yes)	0.6512
F1-Score (Yes)	0.3862
ROC-AUC	0.5392
Confusion Matrix

True Negatives (TN): 83

False Positives (FP): 74

False Negatives (FN): 15

True Positives (TP): 28

Result Interpretation

Accuracy is only slightly higher than random prediction

ROC-AUC (~0.54) indicates weak classification ability

High recall but low precision for the "Yes" class

Overall performance is limited due to weak feature relevance

Conclusion

The Logistic Regression model was successfully implemented along with proper preprocessing, scaling, cross-validation, and evaluation. However, due to the weak correlation between features and the target variable, the model demonstrates limited predictive performance. The decision boundary further confirms poor class separability.

This project successfully fulfills all required components:

✔ Exploratory Data Analysis

✔ Model Development

✔ Decision Boundary Visualization

✔ Performance Evaluation

Libraries Used

NumPy

Pandas

Matplotlib

Seaborn

Scikit-learn
