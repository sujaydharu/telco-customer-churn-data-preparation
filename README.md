

# Activity 1: Dataset Preparation Activity (Telco Customer Churn)

**Course:** Machine Learning [ADPC509]  
**Class:** T.Y. B.Tech (AI & DS)  
**Academic Year:** 2026-27  
**Department:** Artificial Intelligence & Data Science  
**Institution:** Zeal College of Engineering and Research (ZCOER), Pune

## 📌 Project Overview

This project focuses on preparing the **Telco Customer Churn dataset** for exploratory data analysis and future machine learning tasks.

The dataset contains customer information such as services used, contract details, monthly charges, total charges, and churn status. The goal of this activity is to inspect, clean, explore, encode, and scale the data while preserving the original dataset.

## 🎯 Objectives

- Load and inspect the dataset
- Identify numerical and categorical features
- Check and handle missing values
- Check duplicate records and categorical consistency
- Perform exploratory data analysis (EDA)
- Encode categorical features
- Scale selected numerical features
- Validate and export the prepared dataset

## 📂 Dataset Information

| Property | Description |
|---|---|
| Dataset | Telco Customer Churn |
| Source | [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) |
| Original rows | 7,043 |
| Original columns | 21 |
| Data type | Numerical and categorical customer data |
| Potential target | `Churn` |
| Identifier column | `customerID` |

## 🛠️ Tools and Libraries

- Python
- Google Colab / Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 🔍 Data Preparation Steps

### Step 1: Select and Record the Dataset

The Telco Customer Churn dataset was selected for this activity. Its name, source, data type, number of rows, and number of columns were recorded.

### Step 2: Load and Inspect the Dataset

The dataset was loaded using Pandas. The first and last records, dataset shape, column names, and data types were inspected to understand its structure.

### Step 3: Identify Numerical and Categorical Features

Numerical and categorical columns were identified. The `Churn` column was considered a potential target, while `customerID` was identified as an identifier rather than a useful predictive feature. Summary statistics were generated for numerical columns.

### Step 4: Identify Missing Values

Missing values were checked for every column, including their counts and percentages. Blank values in `TotalCharges` were identified as missing data.

### Step 5: Handle Missing Values

A copy of the dataset was created for cleaning. The blank values in `TotalCharges` were converted into missing values and filled using the column’s median. The dataset was checked again to verify that missing values had been handled.

### Step 6: Check Duplicates and Category Consistency

Duplicate records were checked in the original dataset. Extra spaces were removed from categorical values, and unique category values were inspected for consistency.

After removing `customerID`, some rows may appear identical across the remaining features. These were retained because they may represent different customers with the same characteristics.

### Step 7: Perform Exploratory Data Analysis (EDA)

Summary statistics and frequency counts were examined. The notebook includes visualizations such as:

- Distribution of `MonthlyCharges`
- Customer counts by `Contract` type

The visualizations include titles and axis labels, followed by observations about the data.

### Step 8: Encode Categorical Features

Binary categorical features were converted into numerical values. Other categorical features were converted using one-hot encoding. The changes in the dataset’s columns and shape were examined after encoding.

### Step 9: Scale Numerical Features

Selected numerical features were standardized using `StandardScaler`:

- `tenure`
- `MonthlyCharges`
- `TotalCharges`

The identifier and target columns were not scaled. For a future predictive model, the scaler should be fitted on the training data only to avoid data leakage.

### Step 10: Validate and Save the Prepared Dataset

The final dataset was checked for its shape, remaining missing values, and duplicate records. The prepared dataset was exported separately as:

`prepared_telco_churn.csv`

## 📁 Repository Structure

```text
telecom_customer_churn/
│
├── Activity_1_Telecom_Customer_Data_Preparation.ipynb
├── Telco-Customer-Churn.csv
├── prepared_telco_churn.csv
└── README.md
```

## ▶️ How to Run

### Using Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload or open `Activity_1_Telecom_Customer_Data_Preparation.ipynb`.
3. Upload `Telco-Customer-Churn.csv` when required by the notebook.
4. Run the notebook cells from top to bottom.
5. The cleaned dataset will be saved as `prepared_telco_churn.csv`.
6. Download the prepared CSV from the Colab Files panel or using the notebook’s download code.

### Using Jupyter Notebook

1. Install Python and Jupyter Notebook, if they are not already installed.
2. Place the notebook and `Telco-Customer-Churn.csv` in the same project folder.
3. Open Jupyter Notebook and launch `Activity_1_Telecom_Customer_Data_Preparation.ipynb`.
4. Run the notebook cells from top to bottom.
5. The prepared dataset will be saved in the project folder as `prepared_telco_churn.csv`.

## 📌 Conclusion

The Telco Customer Churn dataset was inspected and prepared for further analysis. Missing values were handled, categorical values were checked and encoded, selected numerical features were scaled, and the identifier column was removed.

The final prepared dataset was saved separately as `prepared_telco_churn.csv`. This activity provided practical experience in data inspection, cleaning, exploratory analysis, encoding, scaling, and validation—important steps before building a machine learning model.

---

**Author:** Sujay Dharu - Student - Department of AI & DS, ZCOER Pune

