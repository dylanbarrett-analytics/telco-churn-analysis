# IBM Telco Customer Churn Analysis

---

## 📘 Introduction
This project analyzes customer churn patterns using the **IBM Telco Customer Churn** dataset. The goal is to identify factors that contribute to customers leaving, with a focus on actionable business insights. The final product is an interactive Tableau dashboard that allows users to explore churn trends by contract type, tenure, monthly charges, and number of service subscriptions — all powered by data prepped in Microsoft Excel. (I normally use SQL for data prep, but I wanted to experiment with Excel this time since this is a relatively small dataset.)

### 🧠 What is IBM?
**IBM (International Business Machines Corporation)** is a global technology company known for its work in **cloud computing, artificial intelligence, enterprise software, and data analytics**. In addition to offering business solutions and consulting services, IBM also provides educational resources and sample datasets — and that includes this synthetic Telco dataset.

---

## 🏢 About the IBM Telco Dataset
This dataset is a **fictional yet realistic simulation** of a telecommunications company. Each row represents a single customer and includes details such as:
- Basic demographics
- Contract type and overall tenure 
- Services subscribed to (internet, phone, streaming, etc.)  
- Billing information  
- Churn label (yes or no)

---

## 🎯 Project Goal
The goal of this project is to identify key patterns and risk factors associated with customer churn in this telecommunications setting. By focusing on variables such as contract type, tenure, and subscribed services, this analysis aims to highlight which customer segments are most likely to leave — and when.

Rather than relying heavily on demographic attributes, this project takes a business-focused approach by analyzing customer departures through the lens of **account behavior, billing characteristics, and service usage**.

---

## 🛠️ Tools Used

- **Microsoft Excel** – For overall data cleaning, exploration via PivotTables, and calculated fields based on grouping 
- **Tableau** – For designing an interactive dashboard with KPI cards, visualizations, and a dropdown parameter that increases level of detail

---

## 📊 Data Preparation & Exploration

The original dataset was cleaned and examined in Microsoft Excel. Key steps included:

- Created calculated fields to derive:
  - Total number of subscribed services (`ServiceCountGroup`)
  - Monthly charge buckets (`MonthlyChargeGroup`)
  - Tenure ranges (`TenureGroup`)
- Built pivot tables to explore churn by tenure, contract type, billing amount, and service combinations
- Used basic bar charts to identify high-risk segments (that was all that was necessary for this project)

---

## 📁 Excel Deliverables

Screenshots of all core PivotTables and charts have been saved in the `/images/` folder. These findings shaped the structure of the Tableau dashboard and helped prioritize which KPIs to highlight.

---

## 📐 Choosing the More Appropriate Metric

To ensure consistency and comparability across customer groups of varying sizes, this project uses churn rate — not raw churn counts — as the primary measure of risk. This rate provides a normalized view that highlights likelihood of departure, making it more actionable for any potential business strategies.
- Statistically speaking, a count can be biased by the size of the subset. For example, **Group A** may have 100 customers with a churn rate of 50%, while **Group B** has 1,000 customers with a churn rate of 25%. Even though **Group B** lost more customers in total (250 vs. 50), the **likelihood of churn** is actually much higher in **Group A**, and that's more statistically significant when it comes to studying the behaviors and decision-making of different groups of people. (Analytics and psychology complement each other so well.)

---

## 📈 Final Insights: Excel → Tableau
The final Tableau dashboard presents four key visualizations that guide users through the story of churn behavior with this data:

- **By Contract Type:** Reveals that customers on short-term (month-to-month) contracts are significantly more likely to cancel early.
- **By Tenure Group:** Confirms that churn risk is highest in the first 6 months of a customer’s lifecycle, further cementing a "short-term, more churn" narrative.
- **By Monthly Charges:** Shows that customers paying over $70/month are much more likely to leave.
- **By Service Count (parameterized):** Reveals that churn peaks at 2–5 subscribed services. (This was interesting as my initial hypothesis was that the peak would occur at 0-1 services.)
  - **Interactive Parameter View:** Adds an increased level of detail, allowing users to explore churn rate by service count in combination with tenure or billing granularities.

All charts are designed for clarity and consistency, with custom reference lines (overall average churn rate), and dynamic tooltips. KPI cards summarize key metrics while maintaining a sleek, modern visual design (given Tableau Public's design limitations).

---

## 🔎 Additional Insights Explored (Not Included in Final Dashboard)

- **Fiber Optic Customers Are the Most Likely to Leave**  
  An interesting correlation regarding choice of internet service, but it really has nothing to do with time or cost, so it wouldn't fit the storyline.
- **Churn by Service Count Alone**  
  Definitely provided the foundation for insights, but truly lacked context without the expanded detail levels of tenure or price.

---

## ✅ Final Thoughts
This project demonstrates how Microsoft Excel and Tableau can be used together to uncover meaningful business insights, even from a synthetic dataset. By focusing on behavioral variables such as tenure, billing, and service bundling, basic demographics are relegated to the sideline in order to find the most significant churn risk patterns (at least in this particular dataset).

---

## 🌐 View the Dashboard  
[📎 View on Tableau Public](https://public.tableau.com/app/profile/dylan.barrett1539/viz/UnderstandingChurnPatternsBehindCustomerDepartures/Dashboard)
