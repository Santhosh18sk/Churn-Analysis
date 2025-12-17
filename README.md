# 📊 Customer Churn Analytics  
**Tools Used:** Excel | SQL (MySQL) | Power BI  

#### 🔹 Customer Churn Main Dashboard
![Customer Churn Main Dashboard](https://github.com/Santhosh18sk/Churn-Analysis/blob/main/Dashboard%20Images/Main%20Dashboard.png?raw=true)


---

## 🧩 Problem Statement
Customer churn refers to customers leaving a business over time.  
The aim of this project is to analyze customer churn patterns, understand which factors influence churn the most, and provide clear insights that can help improve customer retention.

This project follows a **complete analytics workflow**, combining data collection, SQL-based analysis, structured data modeling, and interactive Power BI dashboards.

---

## 📂 Dataset
The dataset contains bank customer information related to demographics, account details, engagement behavior, and churn status.

### Dataset Columns
- **customer_id** – Unique identifier for each customer  
- **credit_score** – Credit score of the customer  
- **country** – Customer’s country  
- **gender** – Gender of the customer  
- **age** – Age of the customer  
- **tenure** – Number of years the customer has been with the bank  
- **balance** – Account balance  
- **products_number** – Number of products owned by the customer  
- **credit_card** – Credit card ownership (1 = Yes, 0 = No)  
- **active_member** – Activity status (1 = Active, 0 = Inactive)  
- **estimated_salary** – Estimated salary  
- **churn** – Customer churn status (1 = Churned, 0 = Retained)  

---

## 🛠️ Data Collection & Preparation

### Tools Used
- Excel  
- Power BI  
- SQL (MySQL)  

### Excel
- Initial inspection of the dataset  
- Removed null values  
- Checked for duplicates  
- Renamed columns for clarity  
- Basic formatting before loading into Power BI  

### Power BI
- Imported cleaned data  
- Verified data types  
- Standardized categorical values:
  - Credit card → Owned / Not Owned  
  - Activity status → Active / Inactive  
  - Churn → Churned / Not Churned  

---

## 🧮 Conditional Columns & Grouping
To make analysis easier and more meaningful, grouped columns were created:

- Age Group  
- Credit Score Group  
- Account Balance Group  
- Tenure Group  

Each group was created using **separate dimension tables**, connected to the main fact table using **ID-based relationships**.  
This ensured correct sorting, filtering, and clean analysis across visuals.

---

## 🧱 Data Modeling
- Created reference tables for all grouped columns  
- Established many-to-one relationships  
- Followed a clean fact–dimension modeling approach  

---

## 📌 KPIs
The following KPIs were created:

- Total Customers  
- Customers Lost  
- Churn Rate (%)  

---

## 🔍 SQL Exploratory Data Analysis (EDA)
SQL was used to validate Power BI results and perform deeper exploratory analysis on churn behavior.

### Key Findings from SQL
- Overall churn rate is **20.37%**
- Female customers churn at **25.07%**, while male customers churn at **16.46%**
- Germany has the highest churn rate at **32.44%**, significantly higher than France and Spain
- The average age of churned customers is **44.84 years**, while retained customers average **37.41 years**
- Customers aged **51–60** show the highest churn rate
- Churned customers have a **higher average account balance (~91K)** compared to retained customers
- Customers holding **3 or more products** show extremely high churn, especially in Germany
- Inactive customers churn significantly more than active customers
- High-risk customer segments were identified using SQL `HAVING` conditions (country + product combinations)

SQL analysis helped **confirm and strengthen** insights observed in the Power BI dashboard.

---

## 📊 Visualizations (Power BI)

### Donut Charts
- Customers by Gender  
- Customers by Credit Card Status  
- Customers by Activity Status  

### Charts & Tables
- Customers Lost by Tenure Group  
- Customers and Churn Rate by Credit Score Group  
- Customers and Churn Rate by Age Group  
- Churn Rate by Account Balance Group  

**Conditional formatting** was applied **only** to the *Account Balance Group churn table* to highlight churn rates above **25%**.

### Slicers
- Country  
- Activity Status  



---

#### 🔹 Active Customers Dashboard
![Active Customers Dashboard](https://github.com/Santhosh18sk/Churn-Analysis/blob/main/Dashboard%20Images/Active%20Customers.png?raw=true)

---

#### 🔹 Customer Analysis by Gender Dashboard
![Customer Analysis by Gender Dashboard](https://github.com/Santhosh18sk/Churn-Analysis/blob/main/Dashboard%20Images/Female%20Customers.png?raw=true)

---


## 🔎 Insights & Findings

### Customer Segmentation
- Female customers churn more than male customers (**25.07% vs 16.46%**).
- Inactive customers show a much higher tendency to churn compared to active customers.
- Credit card ownership alone does not significantly reduce churn.
- Germany stands out as the highest churn region.
- Customers owning more than two products show very high churn, indicating possible over-selling.

### Behavioral Insights
- Customers aged **51–60** are the most likely to churn.
- The average age of churned customers is **44.84 years**, which is notably higher than retained customers.
- High account balance customers are at greater churn risk, directly impacting revenue.
- Churn is observed among both short-tenure and long-tenure customers.

---

## 💡 Recommendations

### Engagement Strategy
- Re-engage inactive customers early using targeted communication.
- Improve follow-ups for middle-aged customers.

### Product Strategy
- Avoid aggressively pushing more than two products.
- Analyze why customers with 3+ products are leaving.

### Regional Strategy
- Investigate service or pricing issues in Germany.
- Run region-specific retention programs.

### High-Value Customer Retention
- Closely monitor high-balance customers.
- Offer loyalty benefits or personalized support.

### Monitoring & Prevention
- Continuously track high-risk segments identified through SQL.
- Use inactivity and product overload as early warning signals.

---

## 🏁 Conclusion
This project demonstrates a **customer churn analytics solution using Excel, SQL, and Power BI**.  
By combining SQL-driven exploration, proper data modeling, and clear dashboard storytelling, the analysis delivers actionable insights to help reduce churn and improve customer retention.
