# Customer Churn Analysis

**Author:** Shubham Kumar Dubey
**File:** `ShubhamKumarDubey_CustomerChurnAnalysis.ipynb`

---

## Project Description

Customer churn is one of the most critical business problems across industries such as telecom, banking, and SaaS. This project performs an end-to-end analysis of customer churn using a real-world-style dataset to:

- Identify key factors that drive customer churn
- Build and compare multiple machine learning classification models
- Provide actionable business recommendations to reduce churn
- Predict churn probability for new/unseen customers

---

## Dataset

| Property | Details |
|----------|---------|
| **File** | `customer_churn_dataset.csv` |
| **Rows** | 10,000 customers |
| **Columns** | 12 (11 features + 1 target) |
| **Target** | `Churn` (0 = No Churn, 1 = Churn) |
| **Source** | Kaggle — Customer Churn Dataset |
| **Link** | [https://www.kaggle.com/datasets/muhammadshahidazeem/customer-churn-dataset](https://www.kaggle.com/datasets/muhammadshahidazeem/customer-churn-dataset) |

### Feature Descriptions

| Feature | Type | Description |
|---------|------|-------------|
| CustomerID | Integer | Unique customer identifier |
| Age | Integer | Customer age |
| Gender | Categorical | Male / Female |
| Tenure | Integer | Months as a customer |
| Usage Frequency | Integer | Product usage frequency per month |
| Support Calls | Integer | Number of support calls made |
| Payment Delay | Integer | Days of payment delay |
| Subscription Type | Categorical | Basic / Standard / Premium |
| Contract Length | Categorical | Monthly / Quarterly / Annual |
| Total Spend | Float | Total amount spent |
| Last Interaction | Integer | Days since last interaction |
| Churn | Binary | 0 = Retained, 1 = Churned |

---

## Technologies Used

| Category | Libraries |
|----------|-----------|
| Data Manipulation | `pandas`, `numpy` |
| Visualisation | `matplotlib`, `seaborn` |
| Machine Learning | `scikit-learn`, `xgboost` |
| Class Imbalance | `imbalanced-learn` (SMOTE) |
| Notebook Environment | `jupyter`, `ipykernel` |

---

## Models Built

1. Logistic Regression
2. Decision Tree
3. Random Forest ✦
4. Gradient Boosting
5. AdaBoost
6. XGBoost ✦ *(typically best performer)*
7. K-Nearest Neighbors
8. Support Vector Machine

---

## Project Structure

```
Custome_churn/
│
├── customer_churn_dataset.csv              # Raw dataset
├── ShubhamKumarDubey_CustomerChurnAnalysis.ipynb  # Main notebook
├── requirements.txt                        # Python dependencies
├── README.md                               # This file
└── ShubhamKumarDubey_ProjectReport.docx     # Project report
```

---

## Setup & Run Instructions

### 1. Clone / Download the project

```bash
# If using git
git clone <repo-url>
cd Custome_churn
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook AnshumanDubey_CustomerChurnAnalysis.ipynb
```

### 5. Run all cells

In Jupyter: **Kernel → Restart & Run All**

---

## Key Results

| Metric | Best Model |
|--------|-----------|
| Accuracy | ~95%+ |
| ROC-AUC | ~0.98+ |
| F1 Score | ~0.95+ |

> Exact values depend on model training run; XGBoost / Random Forest typically lead.

---

## Key Findings

- **Tenure** is the strongest predictor — new customers churn most
- **Support Calls** ≥ 5 dramatically increase churn probability
- **Payment Delay** > 20 days is a strong churn signal
- **Monthly contracts** have 2–3× higher churn than Annual contracts
- **Basic-tier** subscribers churn more than Premium/Standard customers

---

## Output Files Generated

After running the notebook, the following PNG charts are saved:

| File | Content |
|------|---------|
| `churn_distribution.png` | Target variable distribution |
| `numerical_distributions.png` | Feature histograms by churn |
| `categorical_vs_churn.png` | Categorical churn rates |
| `correlation_heatmap.png` | Correlation matrix |
| `boxplots_churn.png` | Box plots by churn status |
| `churn_heatmap_sub_contract.png` | Subscription × Contract heatmap |
| `model_comparison.png` | All model metrics comparison |
| `roc_curves.png` | ROC curves for all models |
| `confusion_matrix_best.png` | Best model confusion matrix |
| `cross_validation.png` | 5-fold CV results |
| `feature_importance.png` | Random Forest feature importance |

---

*Customer Churn Analysis — Shubham kumar Dubey*
