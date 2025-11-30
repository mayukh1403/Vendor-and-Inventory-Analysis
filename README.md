# Vendor & Inventory Performance Analysis

## 📌 Project Overview
This project involves an end-to-end analysis of vendor performance and inventory efficiency for a retail/wholesale business. Using **Python** and **SQL**, I analyzed sales data to identify profitability drivers, supply chain risks, and inventory bottlenecks. The project concludes with statistical hypothesis testing to validate business assumptions regarding vendor performance.

## ❓ Business Problem
Effective inventory management is critical for profitability. The goal of this analysis was to address specific operational challenges, including:
* Identifying underperforming brands that require pricing adjustments.
* Assessing vendor dependency risks.
* Evaluating the cost benefits of bulk purchasing.
* Quantifying capital locked in slow-moving inventory.

## 🛠️ Tech Stack & Tools
* **Language:** Python
* **Database:** SQLite3 (SQL querying for data extraction)
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn (Heatmaps, Boxplots, Pareto Charts)
* **Statistical Analysis:** SciPy (T-tests, Confidence Intervals)

## 📊 Key Analysis & Methodology

### 1. Data Ingestion & Cleaning
* Designed an ingestion script to load raw CSV data into a SQLite database.
* Performed data cleaning to remove inconsistencies, filtering out transactions with negative Gross Profit or Profit Margins to ensure data quality.

### 2. Exploratory Data Analysis (EDA)
* Generated summary statistics and distribution plots to detect outliers in freight costs and stock turnover.
* Created a **Correlation Heatmap** to understand relationships between purchase price, sales volume, and profit margins. 
    * **Key finding:** Higher sales prices showed a negative correlation with profit margins, suggesting competitive pricing pressure.

### 3. Strategic Business Insights
* **Pareto Analysis of Vendors:** Identified that the top 10 vendors contribute **65.69%** of total purchases, highlighting a high dependency risk.
* **Pricing Opportunity:** Identified **198 specific brands** (e.g., *Santa Rita Organic*, *Crown Royal Apple*) that have low sales volume but significantly high profit margins (**66%-89%**), making them ideal candidates for promotional campaigns.
* **Bulk Purchasing Impact:** Analyzed unit costs across order sizes. Purchasing in "Large" quantities reduced the average unit price to **$10.78** compared to **$39.05** for small orders—a **~72% cost reduction**.
* **Capital Lock-up:** Calculated that **$2.71 Million** is currently locked in unsold inventory, with specific vendors like *Diageo North America* and *Jim Beam* contributing the most to this holding cost.

### 4. Statistical Hypothesis Testing
To validate if high-volume vendors are more profitable than low-volume vendors, I performed a **Two-Sample T-Test**.

* **Null Hypothesis ($H_0$):** No significant difference in profit margins between top-performing and low-performing vendors.
* **Result:** Rejected $H_0$ (P-Value: 0.0000).
* **Insight:** Surprisingly, low-performing vendors maintain **significantly higher profit margins (Mean: 41.55%)** compared to top performers (Mean: 31.17%), suggesting they operate on a premium pricing model despite lower volume.

## 📉 Visualizations
The project includes several key visualizations to communicate findings:
* **Pareto Chart:** Visualizing vendor contribution to total procurement.
* **Donut Chart:** Displaying market share of top 10 vendors.
* **Scatter Plot:** Segmentation of brands by Sales vs. Profit Margin to identify target brands for promotions.
* **Box Plots:** Demonstrating the impact of order size on unit purchase price.
* **Confidence Interval Histograms:** Comparing profit margin distributions between vendor groups.

## 💡 Recommendations
Based on the data, the following actions were recommended to stakeholders:
* **Diversify Supply Chain:** Reduce reliance on the top 10 vendors to mitigate risk.
* **Optimize Pricing:** Launch marketing campaigns for the 198 identified high-margin/low-sales brands.
* **Inventory Clearance:** Implement clearance strategies for the **$2.71M** in unsold stock to free up working capital.
* **Leverage Bulk Buying:** Standardize "Large" order sizes where storage permits to capitalize on the **72% unit cost reduction**.

---
*This project demonstrates the ability to translate raw data into actionable business strategies using statistical rigor and visualization.*
