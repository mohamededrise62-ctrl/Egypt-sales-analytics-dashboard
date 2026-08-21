## 🛠️ Data Pipeline & Power Query Steps

Data was ingested, cleaned, and transformed using **Power Query** before loading into the Data Model:

1. **Data Ingestion & Cleaning:**
   * Removed duplicate records and null values across `Orders`, `Products`, and `Customers` tables.
   * Standardized text formats (Trimmed spaces, Capitalized Each Word) for customer names and region fields.
   * Merged `FirstName` and `LastName` to create a clean `FullName` column.
2. **Data Type Assignment:**
   * Enforced strict data types across fields: `Price` and `Sales` set to Currency, `Date` set to Date format, and IDs set to Text/Integer.
3. **Custom Calendar Table Creation:**
   * Generated a dynamic `Calendar` dimension table featuring attributes for `Year`, `Month Number`, `Month Name`, and `MMM-YYYY` for custom time-intelligence filtering.
4. **Data Modeling (Power Pivot):**
   * Built a multi-table relational schema establishing 1-to-many relationships between `Calendar`, `Customers`, `Products`, and the core `Orders` fact table.

---

## 📊 Dashboard Features & Metrics

* **Key KPIs:** Real-time visibility into **Total Sales ($101M+)**, **Total Units Sold (108K+)**, and **Active Regions (5)**.
* **Category Breakdown:** Pie chart highlighting average sales percentage across categories (*Clothing, Electronics, Books, Toys, Furniture*).
* **Product Insights:** Bar chart evaluating the **Top 10 Total Sales per Product** (*Laptop, Jacket, Shoes, Tablet, etc.*).
* **Trend Analysis:** Line chart mapping monthly sales performance from January to December.
* **Interactive Slicers:** Dynamic filtering by **Region** (*Alexandria, Aswan, Cairo, Giza, Mansoura*), **Category**, and **Month**.

---

## 📁 Repository Structure

├── data/
│   └── raw_sales_data.xlsx       # Source dataset
├── Egypt_Sales_Analytics.xlsx    # Main Excel file with Power Query & Power Pivot Model
└── README.md                     # Documentation


---

## 🚀 How to Use

1. Clone or download this repository.
2. Open `Egypt_Sales_Analytics.xlsx` using Microsoft Excel (Power Pivot enabled).
3. Interact with the slicers on the **Sheet2** dashboard tab to filter insights dynami
