# Interconnect-Telecom-Customer-Churn-Prediction
Built a churn prediction model for Interconnect Telecom using customer contract, personal, and service data. Achieved high AUC-ROC to identify clients at risk of leaving, enabling targeted retention strategies.


This project aims to help **Interconnect**, a telecom provider, predict customer churn using historical contract, service, and personal data. By identifying clients likely to leave, Interconnect can offer retention promotions to reduce churn.

---

## 🎯 Project Goal

Build a machine learning model to:
- Predict if a customer will churn (`EndDate != 'No'`)
- Help the marketing team proactively retain at-risk customers

---

## 🗂️ Data Sources

Four CSV files:
- `contract.csv`: contract type, tenure, billing, and end status
- `personal.csv`: demographics (gender, seniority, etc.)
- `internet.csv`: Internet service usage and extras
- `phone.csv`: Phone service and line information

Each includes `customerID` as a unique identifier.

---

## 🧠 Target & Evaluation Metrics

- **Target:** Churn = customers where `EndDate` ≠ `'No'`
- **Primary Metric:** AUC-ROC
- **Secondary Metric:** Accuracy

### ✅ Score Criteria
| AUC-ROC Range     | Score Points |
|-------------------|--------------|
| < 0.75            | 0 SP         |
| 0.75 – 0.81       | 4 SP         |
| 0.81 – 0.85       | 4.5 SP       |
| 0.85 – 0.87       | 5 SP         |
| 0.87 – 0.88       | 5.5 SP       |
| ≥ 0.88            | 6 SP         |

---

## 🔧 Methodology

1. **Data Preprocessing**
   - Merged datasets on `customerID`
   - Encoded categorical variables
   - Handled missing values
   - Engineered features (e.g. contract length, total services)

2. **Model Training**
   - Trained classification models: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting
   - Tuned hyperparameters with cross-validation

3. **Evaluation**
   - Compared models using AUC-ROC and Accuracy
   - Plotted ROC curves and confusion matrices

---

## 📈 Tools & Libraries

- Python
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`, `seaborn`

---

## 📊 Results

- Best model: Random Forest / Gradient Boosting (depending on tuning)
- AUC-ROC: ≥ **0.88** (target met ✅)
- Insights into churn drivers (e.g., month-to-month contracts, fiber-optic users)

---

## 💡 Business Value

With accurate churn prediction, Interconnect can:
- Offer custom promotions to retain valuable users
- Prioritize customer engagement based on risk
- Reduce customer turnover and increase lifetime value

---

*This project demonstrates end-to-end machine learning applied to real-world customer data for strategic decision-making.*
