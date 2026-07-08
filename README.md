# 📊 Personal Finance Data Analytics Portfolio

## 📌 Project Metadata
* **Project Name:** Personal Finance Data Analytics
* **Dataset File:** `Portfolio_Data_Cleaning_and_Visualization_v1 Divka.xlsx`
* **Author:** Divka Mayasari
* **Role:** Data Analyst Enthusiast
* **Tools Used:** Google Sheets, Microsoft Excel (Data Cleaning, Data Modeling, Clustered Bar Charts)
* **Target Output:** Automated Cash Flow Tracking & Side-by-Side Financial Performance Chart

---

## 📖 Case Study: Personal Finance Data Wrangling & Visualization

### 1. Background & Business Problem
Tracking personal finance is essential for long-term budget planning, but raw transaction records often suffer from fragmentation and poor formatting. 

In this case study, the user's initial tracking system stored financial transactions in separate, isolated sheets (`Income` and `Expense` tabs), causing data silos. Furthermore, the currency entries contained manual text strings (e.g., `Rs1.000,00`), which made the values mathematically unreadable by standard analytical software. As a result, calculating aggregated summaries and building comparative data charts was functionally impossible.

The core objective of this project is to clean the data, restructure the isolated sheets into a single structured schema, and develop an intuitive dashboard containing a side-by-side financial chart to easily evaluate monthly or daily income vs. expense performance.

### 2. Data Cleaning & Transformation Process (ETL Workflow)
To build a sustainable visualization data source, the following data engineering steps were performed:
<img width="720" height="1612" alt="Screenshot_20260708-150440" src="https://github.com/user-attachments/assets/20fe0406-d613-498d-a986-e3f3659ec31c" />

* **Handling Currency Text Anomalies:** Removed the hardcoded `Rs` characters and manual dot/comma text dividers from transaction values. Re-entered them as raw integers (e.g., changing `Rs1.000,00` into a clean number `1000`) so computational formulas can execute correctly.
* **Proper Data Type Formatting:** Selected the raw integer fields and dynamically applied the official system-wide **Accounting/Currency** formatting via the spreadsheet tool ribbon. This displays currency symbols properly while keeping the core cell values as pure numbers.
* **Schema Consolidation (Data Integration):** Consolidated the data from the fragmented `Income` and `Expense` sheets into a unified, flat relational schema on a primary master sheet (Dashboard).
* **Removing Chart Noise:** Excluded static "Total" summary rows from the visualization data range boundaries to prevent chart scale distortion.

### 3. Data Schema & Metadata Dictionary
The integrated data model on the consolidated spreadsheet is organized vertically under the following relational structure:
<img width="720" height="1612" alt="Screenshot_20260709-002056" src="https://github.com/user-attachments/assets/5f5cfb15-9f11-44d9-8460-5bc63442fc4c" />
<img width="720" height="1612" alt="Screenshot_20260709-002109" src="https://github.com/user-attachments/assets/bc79dc7a-c462-43da-aae1-2d62fb186811" />

| Column Name | Data Type | Sample Value | Description |
| :--- | :--- | :--- | :--- |
| `Date` | Date (DD/MM/YY) | `19/06/22` | The exact recorded date of the transaction. |
| `Income` | Numeric (Currency) | `1000` | Total revenue/earnings credited on that date. |
| `Expense` | Numeric (Currency) | `800` | Total expenditure/costs debited on that date. |

### 4. Data Visualization Design
A **Clustered Column Chart (Side-by-Side Bar Chart)** was successfully generated from the master dataset:
* **X-Axis:** Represents the chronological progression of time (`Date`).
* **Y-Axis:** Represents the net transaction amount in the localized currency.
* **Visual Encoding:** Uses two contrasting, side-by-side color bars for each time unit (e.g., Emerald Green for **Income** and Crimson Red for **Expense**) to provide instant visual perception of net savings or potential deficits.
<img width="720" height="1612" alt="Screenshot_20260709-002135" src="https://github.com/user-attachments/assets/96f3682b-6efc-467a-ae1c-ce8c5728f59a" />

---

## 🚀 How to Review and Run This Project
1. **Download the Asset:** Download the `Portfolio_Data_Cleaning_and_Visualization_v1 Divka.xlsx` file from this repository to your local drive.
2. **Open the Spreadsheet:** Open the downloaded workbook using local software like **Microsoft Excel** or import the file directly into your personal **Google Sheets** workspace.
3. **Explore Dashboard:** Navigate to the main integrated sheet to interact with the working data rows and the responsive side-by-side clustered column graph.

### 5. Insights & Financial Conclusion
Based on the consolidated cash flow data and the generated side-by-side bar chart, several key financial analytical insights can be concluded:

* **Positive Net Cash Flow:** Throughout the recorded period, the financial status consistently maintained a positive net cash flow. The total income managed to comfortably outpace total expenditures, ensuring a healthy financial buffer.
* **Peak Performance Analysis:** The highest financial liquidity occurred on **23/06/22**, where income reached its peak at `2000`, while the lowest operational revenue was recorded on **22/06/22** at `500`.
* **Expense Volatility & Management:** While expenditures remained lower than incoming revenue across all tracked dates, the variance between bars highlights shifting daily habits. Monitoring these visual gaps helps identify unnecessary spending spikes and optimize saving rates.
* **Strategic Recommendation:** To improve future financial health, it is recommended to implement a static percentage-based budgeting rule (e.g., the 50/30/20 rule) directly into the spreadsheet to automatically flag dates where expenses exceed the ideal safety threshold.
* 
