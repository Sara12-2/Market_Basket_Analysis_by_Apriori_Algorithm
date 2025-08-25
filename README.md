📂 Market_Basket_Analysis_By_Apriori_Algorithm
========================================================

# 🛒 Market Basket Analysis Dashboard  

This project implements **Market Basket Analysis (MBA)** using the **Apriori Algorithm** and **Association Rule Mining**.  
It provides an interactive **Streamlit dashboard** that allows users to upload transactional data (CSV/Excel), run frequent itemset mining, and generate association rules to discover product relationships.  

---

## 🚀 Features
- 📂 Upload **CSV/Excel** transaction files  
- 🧾 Automatically extract **InvoiceNo & Description**  
- 🔍 Apply **Apriori Algorithm** for frequent itemsets  
- 📈 Generate **Association Rules** with metrics:
  - Support  
  - Confidence  
  - Lift  
- 📊 Display results inside dashboard  
- 📥 Download rules as **CSV**  

---

## 🗂 Dataset Requirement
Your dataset must contain at least the following columns:  
- **InvoiceNo** → Unique transaction ID  
- **Description** → Product/item description  

Example:
| InvoiceNo | Description   |
|-----------|--------------|
| 1001      | Bread        |
| 1001      | Butter       |
| 1002      | Milk         |

---

## 🛠️ Installation

Clone the repository and install dependencies:
```bash
git clone https://github.com/your-username/MarketBasketAnalysis.git
cd MarketBasketAnalysis
pip install -r requirements.txt
```
## ▶️ Usage

Run the Streamlit app:
```bash
streamlit run app.py
```

Upload your .csv or .xlsx transaction file

Select minimum support threshold with the slider

View frequent itemsets & association rules

Download rules as CSV

## 📂 Project Structure
```bash
MarketBasketAnalysis/
 ├── app.py                # Streamlit dashboard script
 ├── requirements.txt      # Required dependencies
 ├── README.md             # Project documentation
 └── sample_data.csv       # Example dataset
```
## 📌 Future Improvements

🔗 Visualization of rules (Network Graph)

📊 Support for multiple metrics comparison

☁️ Deploy on Streamlit Cloud / HuggingFace Spaces

## 👩‍💻 Skills Learned

Data Preprocessing (pandas, cleaning text data)

Transaction Encoding (mlxtend TransactionEncoder)

Frequent Itemset Mining (Apriori Algorithm)

Association Rule Mining (support, confidence, lift)

Interactive Dashboards (Streamlit)

CSV/Excel Handling in Python

👨‍💻 Developed with ❤️ using Python, Pandas, Mlxtend, and Streamlit

========================================================

## 📦 requirements.txt
streamlit
pandas
mlxtend
openpyxl
🐍 app.py
```bash
import streamlit as st
import pandas as pd
from mlxtend.frequent_patterns import apriori, association_rules
from mlxtend.preprocessing import TransactionEncoder

st.title("🛒 Market Basket Analysis (Excel & CSV Supported)")
```
