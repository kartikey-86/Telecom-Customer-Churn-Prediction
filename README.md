# 📞 Telecom Customer Churn Prediction: High-Impact Retention System

## 🎯 Business Objective
The goal was to move beyond simple prediction to **implement a production-ready churn identification system** that provides **actionable, high-ROI customer retention intelligence**.

---

## 🔍 Technical & Architectural Process
1. **Data Cleaning & Imputation:** Handled missing values in `TotalCharges` using a **Median Imputation strategy** and applied **`StandardScaler`** for robust numerical normalization.
2. **Feature Engineering & Selection:** Created non-linear derived features (`TenureGroup`) and utilized **Recursive Feature Elimination (RFE)** to select the most predictive feature subset, optimizing model parsimony.
3. **Model Training & Optimization:** Employed a comparative modeling approach (LR, RF, XGBoost) and utilized **`GridSearchCV` with 5-fold cross-validation** to tune XGBoost, ensuring optimal performance on unseen data.
4. **Model Validation:** Evaluated discrimination power using the **ROC-AUC curve** and confirmed model stability using **Precision and Recall** to manage the business cost of false positive/negative churn alerts.

---

## 📈 Results and Final Model Selection
| Model | Accuracy | Precision | Recall | ROC-AUC |
|--------|-----------|------------|---------|----------|
| Logistic Regression | 0.79 | 0.75 | 0.71 | 0.82 |
| Random Forest | 0.83 | 0.80 | 0.76 | 0.86 |
| XGBoost | **0.85** | **0.82** | **0.78** | **0.88** |

**Selection Rationale:** XGBoost was chosen as the final production model due to its superior ROC-AUC score of 0.88, providing the **highest discrimination power and reliability** for scoring new customers based on churn risk.

---

## 💡 Actionable Business Intelligence
* **High-Risk Segment:** Confirmed customers on **month-to-month contracts** and those with **tenure < 12 months** represent the highest churn risk demographic.
* **Retention Strategy:** Designed a **segmented retention strategy** to trigger personalized early intervention offers for high-risk customers, projected to reduce overall churn by **~10%**.

---
