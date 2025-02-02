# 🛒 Data Analysis with Python: Sales Transactions

## 📌 Overview
This project demonstrates data cleaning and transformation techniques in **Python** using **Pandas** and **NumPy**. The dataset contains sales transactions, and we apply various operations such as feature engineering, text processing, and merging external data.

## 📂 Dataset
- **`transaction2.csv`** – Contains sales transaction data.
- **`value_inc_seasons.csv`** – Provides seasonal data for transactions.

## 🔧 Features & Steps

### 📥 1. Data Loading
- Import CSV files using `pandas.read_csv()`
- Handle different delimiters (`,` and `;`)

### 📊 2. Data Exploration
- View first rows (`df.head()`)
- Summary statistics (`df.describe()`)
- Check data types (`df.info()`)

### 🔢 3. Feature Engineering
- Create new columns:
  - `CostPerTransaction = CostPerItem * NumberOfItemsPurchased`
  - `SellingPricePerTransaction = SellingPricePerItem * NumberOfItemsPurchased`
  - `ProfitPerTransaction = SalesPerTransaction - CostPerTransaction`
  - `Markup = ProfitPerTransaction / CostPerTransaction`
- Round `Markup` values to two decimal places

### 📅 4. Date Formatting
- Convert `Day` and `Year` to strings
- Combine `Day`, `Month`, and `Year` into a `Date` column

### ✂ 5. Text Processing
- Split `ClientKeywords` into `ClientAge`, `ClientType`, and `LengthofContract`
- Remove unnecessary brackets (`[` and `]`)

### 🔄 6. Merging External Data
- Merge seasonal information from `value_inc_seasons.csv` using the `Month` column

### 🧹 7. Data Cleaning
- Drop unnecessary columns (`ClientKeywords`, `Day`)
- Save cleaned data as **`ValueInc_Cleaned.csv`**
