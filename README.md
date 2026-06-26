# Customer Churn Prediction & Revenue Risk Dashboard

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat&logo=powerbi&logoColor=black)
![Dataset](https://img.shields.io/badge/Dataset-IBM%20Telco%20(Kaggle)-20BEFF?style=flat)

> **End-to-end analytics project** identifying $139,131 in monthly revenue at risk across 7,043 telecom customers — using Python, SQL, Logistic Regression, and Power BI.

---

## The Business Problem

A telecom company is losing **26.5% of its customers every period**. That translates to **$139,131 in monthly recurring revenue** walking out the door. The business doesn't know:
- Which customers are about to leave before they do
- Why customers are really leaving (hint: it's not price)
- Which customer segment is bleeding the most revenue

This project answers all three questions.

---

## Key Findings

| Finding | Data |
|---|---|
| Overall churn rate | **26.5%** (1,869 of 7,043 customers) |
| Monthly revenue at risk | **$139,131** |
| Month-to-month contract churn | **42.7%** — 15x higher than 2-year contracts |
| 2-year contract churn | **2.8%** |
| Fiber optic churn rate | **41.9%** — highest-paying customers, highest churn |
| #1 churn reason | **Attitude of support person** (not price, not a competitor) |
| Electronic check payment churn | **45.3%** — highest of all payment methods |
| ML model: active customers flagged at high risk | **102 customers** (≥70% churn probability) |
| ML revenue at risk (active customers) | **$8,280/month** |

> **Business insight**: The data says this is a service quality problem, not a pricing problem. The fix is customer service training and contract conversion incentives — not discounts.

---

## Tech Stack

| Layer | Tools |
|---|---|
| Data cleaning & EDA | Python · Pandas · Matplotlib · Seaborn |
| SQL analysis | SQLite3 (in-memory, via Python) |
| Machine learning | scikit-learn · Logistic Regression · Pipeline · ColumnTransformer |
| Dashboard | Power BI Desktop (3-page interactive dashboard) |
| Notebook | Google Colab |

---

## Project Structure

```
customer-churn-prediction/
│
├── README.md                          ← You are here
├── customer_churn_prediction.ipynb    ← Full analysis notebook (Colab)
├── Telco_Churn_Predictions.csv        ← Cleaned data + ML predictions (output)
│
├── charts/
│   ├── chart1_contract_churn.png
│   ├── chart2_tenure_density.png
│   ├── chart3_monthly_charges_box.png
│   └── chart4_revenue_lost_reasons.png
│
├── dashboard/
│   ├── customer_churn_dashboard.pbix  ← Power BI file
│   └── dashboard_screenshots/
│       ├── page1_churn_overview.png
│       ├── page2_revenue_analysis.png
│       └── page3_ml_predictions.png
│
└── data/
    └── Telco_Churn.csv.xlsx           ← Raw source data (IBM Telco, Kaggle)
```

---

## How to Run

### 1. Clone the repo
```bash
git clone https://github.com/knavyasai/customer-churn-prediction.git
cd customer-churn-prediction
```

### 2. Run in Google Colab
- Open `customer_churn_prediction.ipynb` in [Google Colab](https://colab.research.google.com/)
- Upload `Telco_Churn.csv.xlsx` when prompted
- Run all cells top to bottom
- The notebook outputs `Telco_Churn_Predictions.csv` (cleaned data + ML churn probabilities)

### 3. Open the Power BI Dashboard
- Open `dashboard/customer_churn_dashboard.pbix` in Power BI Desktop
- If prompted to reconnect data: Get Data → Text/CSV → select `Telco_Churn_Predictions.csv`

---

## Dashboard Pages

### Page 1 — Churn Overview (Executive Summary)
4 KPI cards · Churn rate by contract type · Churn by internet service · Churn rate by tenure group

### Page 2 — Revenue & Segment Analysis
Monthly revenue at risk · Stacked bar: revenue loss by contract + internet segment · Churn rate by charge tier · Churn rate by payment method

### Page 3 — Churn Reasons & ML Predictions
Top 10 churn reasons by customer count · Top 5 reasons by revenue impact · ML churn probability distribution · High-risk active customer table (≥70% ML confidence) · Churn rate matrix: Contract × Internet Service

---

## Model Performance

| Metric | Score |
|---|---|
| Accuracy | ~81% |
| ROC-AUC | ~84% |
| Model | Logistic Regression (sklearn Pipeline) |
| Train / Test split | 80% / 20% |

---

## Dataset

**IBM Telco Customer Churn** — available on [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
7,043 rows · 33 original columns · 28 after cleaning

---

## Author

**Navya Sai** · MBA in Business Analytics (Manipal) · B.E. Electronics & Communication Engineering  
[LinkedIn](https://linkedin.com/in/knavyasai) · [GitHub](https://github.com/knavyasai)
