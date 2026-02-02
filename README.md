# Customer Segmentation & Revenue Insights using RFM Analysis

## 📌 Project Overview
This project performs **customer segmentation using RFM (Recency, Frequency, Monetary) analysis** on transactional retail data to understand customer behavior, revenue contribution, and churn risk. The analysis segments customers into actionable groups such as **VIP customer, Loyal cuustomer, High value cuustomer, Regular customer, and Chrun risk cuustomer** to support data-driven retention and revenue strategies.

---

## 🧩 Business Problem
The business lacks clarity on:
- Which customers drive the most revenue
- Which customers are at risk of churn
- How to prioritize customer engagement and marketing spend

Without segmentation, customer strategies are applied uniformly, leading to inefficient resource allocation and potential revenue loss.

---

## 🎯 Project Objectives
- Segment customers using **Recency, Frequency, and Monetary (RFM)** metrics  
- Identify high-value, loyal, regular, and churn-risk customers  
- Analyze revenue, purchase behavior, and engagement patterns by segment  
- Generate actionable insights for retention and revenue optimization  

---

## 📂 Dataset Description
The dataset was gotten from (https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) contains over **525,000 transaction records** with the following fields:
- Invoice  
- Invoice Date  
- Customer ID  
- Quantity  
- Unit Price  
- Country  

After cleaning (removing invalid customers, duplicates, negative quantities, and zero prices), **400,916 valid transactions** were used for analysis.

---

## 🛠 Methodology

### 1. Data Cleaning & Preparation
- Removed transactions with missing Customer IDs  
- Dropped duplicate records  
- Filtered out negative quantities and zero-priced transactions  
- Created a **TotalPrice** feature (Quantity × Price)  
- Converted Customer ID to integer for aggregation  

### 2. Feature Engineering (RFM)
Customer-level RFM metrics were created:
- **Recency** – Days since the customer’s last purchase  
- **Frequency** – Number of unique invoices  
- **Monetary** – Total customer spend  

This resulted in an RFM table of **4,312 unique customers**.

---

### 3. RFM Scoring
- Assigned RFM scores using **quantile-based ranking (1–5)**  
- Higher scores represent better customer behavior  
- Combined RFM scores into a three-digit `rfm_score`

---

### 4. Customer Segmentation
Customers were classified using business rules based on RFM scores:

| Segment Name | Description |
|--------------|------------|
| **VIP customer** | High recency, frequency, and monetary value |
| **High value cuustomer** | High recency and frequency |
| **Loyal cuustomer** | High frequency customers |
| **Regular customer** | Average purchasing behavior |
| **Chrun risk cuustomer** | Low recency, indicating churn risk |

---

### 5. Segment Distribution
Customer distribution by segment:
- **Chrun risk cuustomer:** 32.44%  
- **Regular customer:** 27.55%  
- **VIP customer:** 21.13%  
- **Loyal cuustomer:** 14.87%  
- **High value cuustomer:** 4.01%  

The largest segment consists of **churn-risk customers**, highlighting a critical retention challenge.

---

## 📊 Segment Performance (KPIs)

Key performance indicators were calculated per segment:
- Number of customers  
- Total revenue  
- Total purchases  
- Average recency  
- Average order value  

### Key Findings:
- **VIP customer**
  - Highest total revenue (~5.6M)
  - Highest total purchases
  - Highest average order value
  - Most recent engagement (lowest recency)

- **Loyal cuustomer**
  - Strong contribution to revenue and purchase volume
  - High engagement frequency

- **Chrun risk cuustomer**
  - Largest customer group
  - Longest average recency (~199 days)
  - Indicates high churn risk and potential revenue loss

- **High value cuustomer**
  - Smallest segment
  - Lowest revenue contribution
  - Opportunity for upsell and growth strategies

---

## 📈 Visual Insights
- Bar charts comparing **total revenue**, **customer count**, **total purchases**, and **average order value** by segment  
- Visual evidence that **VIP customers dominate revenue**, while **churn-risk customers dominate volume**

---

## 💡 Business Recommendations
- Prioritize retention strategies for **VIP customer** and **Loyal cuustomer** segments  
- Launch win-back and reactivation campaigns for **Chrun risk cuustomer**  
- Develop upsell and bundle strategies to grow the **High value cuustomer** segment  
- Allocate marketing resources based on **segment-level revenue impact**

---

## 🔧 Tools & Technologies
- Python (Pandas, NumPy)  
- Data Visualization (Matplotlib, Seaborn)  
- Jupyter Notebook  

---

## 📈 Business Value
This project demonstrates how transactional data can be transformed into customer-level insights that support:
- Churn reduction  
- Revenue optimization  
- Targeted marketing and customer engagement strategies  


📦 Customer Segmentation & Revenue Insights using RFM Analysis-python

├── README.md

├── notebooks/

│   └── churn_analysis.ipynb

├── data/

│   ├── raw/

│   └── processed/

├── visuals/

│   └── churn_trends.png
