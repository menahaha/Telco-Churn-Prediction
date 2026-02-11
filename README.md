# Telco Customer Churn Prediction (Track 1 - Tabular ML)
## Dataset
- Dataset: Telco Customer Churn Dataset  
- Source: Kaggle  
- Link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn  

The dataset contains customer information such as:
- Contract type
- Monthly charges
- Tenure
- Payment method
- Internet service details

---

## Project Workflow

### 1. Data Loading and Cleaning
- Dropped unnecessary column (`customerID`)
- Converted `TotalCharges` to numeric
- Filled missing values
- Encoded categorical features using one-hot encoding

### 2. Exploratory Data Analysis (EDA)
EDA was performed to understand churn patterns:
- Churn distribution
- MonthlyCharges vs Churn
- Contract type impact on churn

## Train / Validation Split Method
The dataset was split using a **stratified split** to maintain churn class balance:

- **80% Training Data**
- **20% Validation Data**

```python
train_test_split(
    X, y,
    test_size=0.2,
    stratify=y,
    random_state=42
)
