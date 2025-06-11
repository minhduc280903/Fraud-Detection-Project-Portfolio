# Project: Credit Card Fraud Detection using Machine Learning

**Author:** [Vũ Minh Đức]  
**Contact:** [ducvm.ueb@gmail.com]

---

## 1. Project Overview

This project is an end-to-end demonstration of solving a real-world classification problem in the financial industry. The primary goal is to build a high-performance machine learning model to detect fraudulent credit card transactions from a highly imbalanced dataset.

This project showcases my ability to:
-   Conduct Exploratory Data Analysis (EDA) to uncover key data characteristics.
-   Implement advanced techniques to handle severely imbalanced data.
-   Build, train, and critically evaluate different machine learning models.
-   Interpret model results to provide actionable business insights.

## 2. Key Technical Challenges & Solutions

The most significant challenge in this dataset is the **severe class imbalance**, with fraudulent transactions accounting for only **~0.17%** of the data.

To address this, two primary strategies were employed:
*   **For Random Forest:** Applied **SMOTE (Synthetic Minority Over-sampling Technique)** on the training set to create synthetic fraudulent samples and balance the classes.
*   **For XGBoost:** Utilized the built-in `scale_pos_weight` parameter, which adjusts the weight of the minority class during training.

## 3. Model Comparison & Results

Two powerful models were built and compared. The evaluation focused on **Recall** as the most critical metric, prioritizing the detection of actual fraud cases.

| Metric                | Random Forest (with SMOTE) | **XGBoost (with Weighting)** |
| --------------------- | -------------------------- | ------------------------------ |
| **Recall (Fraud)**    | ~0.82                      | **~0.85**                      |
| **Precision (Fraud)** | **~0.88**                  | ~0.85                          |
| **AUC-ROC**           | ~0.91                      | **~0.92**                      |

**Conclusion:** The **XGBoost** model was selected as the superior model due to its higher **Recall score**, indicating a better ability to minimize costly false negatives.

## 4. Actionable Insights from Feature Importance

By analyzing the feature importances from the XGBoost model, we can identify the key drivers of fraud. This analysis provides valuable insights for the business/risk team, suggesting that features like **V14, V4, and V12** are the strongest indicators of fraudulent activity.

![Feature Importance Chart](link_to_your_feature_importance_chart_image.png) 
*(Lưu ý: Bạn có thể chụp ảnh màn hình biểu đồ Feature Importance từ notebook và tải lên repository, sau đó dán link ảnh vào đây để hiển thị).*

## 5. How to Run

1.  Ensure you have Python and Anaconda installed.
2.  Clone this repository.
3.  Install necessary libraries: `pip install -r requirements.txt` (You would need to create this file).
4.  Open and run the `Phan_Tich_Gian_Lan.ipynb` notebook in Jupyter.

---
*This project was completed as part of my self-learning journey to become a Data Analyst in the financial technology sector.*
