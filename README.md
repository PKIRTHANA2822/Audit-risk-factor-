 # Project Title: Audit Risk Factor
 
<img width="1024" height="430" alt="image" src="https://github.com/user-attachments/assets/62bd9803-4df4-4611-b8ef-59f3081a01aa" />
![Audit Risk Factor-Examples-1024x430](https://github.com/PKIRTHANA2822/Audit-risk-factor-/blob/6f185750f3ba64025ecf6d2df9a642f04c259119/Audit-Risk-2.jpg)

## ✅ Objective:
To build a predictive model that identifies potential risk in audit cases based on financial and operational attributes. The goal is to help auditors efficiently classify risky versus non-risky cases, improving audit planning and resource allocation.

## 💡 Why We Use It:
To automate the risk assessment process in auditing.
To minimize manual effort in identifying high-risk cases.
To provide data-driven insights for auditors and improve decision-making.
To detect patterns and relationships among financial attributes that are indicative of audit risk.

## 🔄 Step-by-Step Approach:
-Data Collection: Load the audit dataset (risk_factors.csv).
-Data Cleaning: Handle missing values.
-Exploratory Data Analysis (EDA): Understand the distribution, correlations, and patterns in the data.
-Feature Engineering: Remove redundant or highly correlated variables, and select key features.
-Model Building: Use Decision Tree Classifier to train a model on the dataset.
-Model Evaluation: Measure accuracy, recall, precision, specificity, and F1-score.
-Optimization: Retrain the model using only the most important features.
-Result Interpretation: Compare performance before and after optimization.

## 📊 Exploratory Data Analysis (EDA):
### Data Summary:
-Dataset has a mix of numerical and categorical variables.
-Only 1 missing value in the Money_Value column, filled with the median.

### Class Distribution:
-Plotted the count of Risk (target variable) using Seaborn.
-Slight class imbalance was detected, but not significant enough to affect model training.

### Correlation Analysis:
-Visualized the correlation matrix using a masked heatmap.
-Found that TOTAL and PARA_B are almost 100% correlated.
-Dropped TOTAL to avoid multicollinearity.

### 🧠 Feature Engineering:
-Removed the redundant feature TOTAL.
-Computed feature importance from the Decision Tree model.
-Selected features with importance > 0.1 for optimized training:
-These are likely the most influential in determining audit risk.

### 🏋️ Model Training:
-Used Decision Tree Classifier from Scikit-learn.
-Split the data into training and testing sets using train_test_split with stratification.
#### Evaluated model using:
-Accuracy
-Precision
-Recall
-Specificity
-F1 Score

### 🧪 Model Testing:
-Evaluated the trained Decision Tree on test data.

#### Confusion matrix was used to compute metrics:
-True Positives (TP)
-False Positives (FP)
-True Negatives (TN)
-False Negatives (FN)

Retrained model using only the most important features to check if performance remains consistent or improves.

### 📈 Output:
![Screenshot (2437)]()
