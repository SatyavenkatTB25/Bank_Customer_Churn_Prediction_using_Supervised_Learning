# 📊 Bank Customer Churn Prediction using Supervised Learning in R

This project applies supervised machine learning models in R to predict bank customer churn based on historical customer data. The goal is to help financial institutions identify at-risk customers early and take proactive retention measures.

## 🔍 Problem Statement

Customer churn poses a significant threat to the financial industry by impacting revenue and customer lifetime value. By predicting which customers are likely to leave, banks can implement personalized retention strategies and improve customer satisfaction.

## 📁 Dataset

- Source: [Kaggle - Bank Customer Churn Dataset](https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset)
- Each row represents a customer; each column represents demographic or financial attributes.

### Features Used:
- `credit_score`, `country`, `gender`, `age`, `tenure`, `balance`, `products_number`, `credit_card`, `active_member`, `estimated_salary`
- Target: `churn` (0 = No, 1 = Yes)

## ⚙️ Methodology

### 🧹 Data Preprocessing
- Verified and removed missing values
- Excluded `customer_id` (identifier)
- Converted categorical variables where necessary (e.g., `churn` to factor for Naive Bayes)
- Random 80/20 train-test split

### 📈 Exploratory Data Analysis (EDA)
- Churn distribution (imbalanced)
- Credit score vs. churn trends
- Balance vs. estimated salary correlation
- Age distribution and churn hotspots

## 🤖 Models Built

| Model                          | Accuracy | Test Error | Sensitivity | Specificity |
|-------------------------------|----------|------------|-------------|-------------|
| Linear Discriminant Analysis  | 81.42%   | 0.1858     | 23.59%      | 95.55%      |
| Quadratic Discriminant Analysis | 84.54% | 0.1546     | 40.26%      | 95.36%      |
| Logistic Regression (Normal)  | 81.87%   | 0.1813     | 21.54%      | 96.62%      |
| Logistic Regression (Poly deg 7) | 84.24% | 0.1576     | 34.87%      | 96.30%      |
| Naive Bayes                   | 84.09%   | 0.1591     | 30.77%      | 97.12%      |

## 🧪 Model Evaluation

- Accuracy: Overall performance
- Sensitivity: Identifying churners correctly
- Specificity: Minimizing false positives
- 10-fold cross-validation used for polynomial logistic regression

## 📊 Key Insights

- Churners are more likely to have lower credit scores and fall into the 41–50 age group.
- Active members and customers with credit cards showed lower churn tendencies.
- Naive Bayes had the highest specificity, while QDA offered the best balance of sensitivity and accuracy.

## 📌 Tools and Technologies

- **Language**: R
- **Packages**: `MASS`, `stats`, `naivebayes`, `ggplot2`
- **Techniques**: EDA, Logistic Regression, Polynomial Features, LDA, QDA, Naive Bayes, Cross-Validation
