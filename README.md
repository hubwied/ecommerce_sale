# E-Commerce Sales Exploratory Data Analysis (EDA)

## 📊 Project Overview
This project demonstrates an end-to-end exploratory data analysis (EDA) on e-commerce sales data using Python. The primary objective is to transform raw transaction records into actionable business insights by identifying top-selling products, seasonal trends, customer behavior patterns, and geographical hotspots. 

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3.13
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Analysis:** `scipy` (Welch's t-test)

## ⚙️ Methodology & Features
* **Data Cleaning:** Handled missing values, removed duplicates, and performed datetime casting.
* **Feature Engineering:** Created calculated columns such as `total_sales`, `year`, `month`, and `day_of_week` to enable time-series analysis.
* **Statistical Validation:** Applied Welch's t-test to validate the significance of sales variance between different days of the week.
* **Customer Segmentation:** Aggregated transactional data to identify high-value and high-frequency buyers.

## 💡 Key Business Insights
* **Revenue Drivers:** The **Laptop** is the undisputed top-selling product, driving the majority of revenue alongside Cameras and Smartphones. Overall, the **Accessories** category slightly outperforms Electronics and Appliances.
* **Geographical Hotspots:** Sales are heavily concentrated in specific urban centers, with **New York, Houston, and Los Angeles** generating the highest total revenue.
* **Temporal Trends & Statistical Proof:** 2023 sales peaked notably in **March and August**. Weekly analysis shows **Thursday** is the most profitable day, while **Wednesday** is the weakest (a Welch's t-test confirmed this difference is statistically significant, *p < 0.05*).
* **Customer Loyalty:** The data proves the existence of highly valuable repeat buyers (e.g., Customer #1418 with 5 distinct purchases), highlighting a prime opportunity for VIP retention strategies.
* **System & Data Discovery:** An attempted Market Basket Analysis revealed a critical system quirk: **every single `order_id` contains only one item**. Customers are making separate transactions for multiple items, which indicates a potential friction point in the store's checkout architecture.
* **Price vs. Quantity:** Pearson correlation analysis revealed no significant relationship (0.039) between a product's price and the quantity ordered, suggesting inelastic demand within this specific product range.

## 🎯 Recommendations & Next Steps
1. **Targeted Marketing:** Focus ad spend on high-revenue products (Laptops, Cameras) and direct campaigns heavily towards New York, Houston, and LA to maximize ROI.
2. **Mid-Week Promotions:** Introduce special discounts, flash sales, or free shipping incentives specifically on **Wednesdays** to balance the statistically significant drop in mid-week sales.
3. **Loyalty Program Implementation:** Since the data confirms the existence of repeat customers, immediately establish a VIP retention program. A full **RFM (Recency, Frequency, Monetary)** analysis should be the next analytical step to segment these users.
4. **Checkout UX Investigation:** The UX/IT team must investigate why customers are generating separate order IDs for single items. Allowing multiple items per cart/order will enable future Market Basket Analysis (cross-selling) and likely increase the Average Order Value (AOV).
