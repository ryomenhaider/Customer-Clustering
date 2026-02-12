# Customer Segmentation Analysis
**Prepared by:** Haider Ali

---

## 📋 Introduction
The goal of this analysis is to group customers based on Age, Annual Income, and Spending Score. Understanding these segments is crucial for personalized offers and targeted marketing campaigns. For this analysis, we used the Mall Customers Dataset from Kaggle. The methodology and results are discussed in detail below.

---

## 📊 Data Overview
The dataset contains **200 customers** with the following features:

| Feature | Description |
|---------|-------------|
| CustomerID | Unique identifier for each customer |
| Gender | Male or Female |
| Age | Customer age in years |
| Annual Income (k$) | Customer income in thousands of dollars |
| Spending Score (1-100) | Score representing purchasing behavior |

**Note:** For clustering, we focused on **Age, Annual Income, and Spending Score**, as these features are most relevant for grouping similar customers.

---

## 🧹 Data Cleaning
Data cleaning ensures accurate and reliable analysis. The following steps were performed using **Pandas**, a Python library for data manipulation:

| Step | Action |
|------|--------|
| **Initial Inspection** | Viewed the first five rows to understand the structure and values of the dataset |
| **Statistical Overview** | Examined summary statistics (mean, std, min, max) to identify unusual patterns |
| **Data Types** | Checked data types for each column and converted where necessary |
| **Removal of Irrelevant Columns** | Dropped the `CustomerID` column as it does not contribute to clustering |
| **Duplicates** | Checked for duplicate rows; **none were found** |
| **Encoding Categorical Variables** | Converted the `Gender` column to numerical format: Male = 0, Female = 1 |

---

## 🧠 Clustering

### Overview
To better understand our customers, we grouped them into **five distinct segments** based on three key attributes:

- **Age** – How old the customer is  
- **Annual Income** – Yearly income in thousands of dollars  
- **Spending Score** – A score representing purchasing behavior  

The goal was to identify patterns in customer behavior and provide actionable recommendations for marketing and sales strategies.

### Method
We used a **clustering approach** to divide customers into five distinct segments.  
Each segment represents a group of customers who are **similar in age, income, and spending behavior**.

> **Key idea:** Customers in the same segment behave similarly, so businesses can design campaigns tailored to each group.

---

## 📌 Segment Profiles and Insights

| Segment | Who They Are | Key Characteristics | Recommendations |
|---------|--------------|---------------------|-----------------|
| 🟢 **Young High-Spenders** | Young customers who spend a lot | Avg Age: 26, Avg Income: $60k, **High Spending Score** | Offer premium products, personalized upsells, trendy campaigns |
| 🟡 **Average Young** | Younger customers with moderate spending | Avg Age: 28, Avg Income: $45k, **Moderate Spending Score** | Engage via social media campaigns, promotional offers |
| 🔵 **Older Low-Spenders** | Older customers who spend less | Avg Age: 45, Avg Income: $50k, **Low Spending Score** | Encourage loyalty programs, discounts, special deals |
| 🟠 **High Income Moderate-Spenders** | Wealthy customers who spend moderately | Avg Age: 35, Avg Income: $90k, **Moderate Spending Score** | Upsell relevant products, personalized campaigns |
| ⚪ **Other / Miscellaneous** | Customers not in the above groups | Mixed ages and spending patterns | Use generalized marketing strategies |

---

## 📈 Visualization

### Overview
Visualizations help see customer patterns at a glance.  
We plot **Annual Income vs Spending Score**, since these two features are most relevant to marketing strategies.

- Each cluster is highlighted in a **different color**  
- It’s easy to identify **high-value vs low-value customers**  
- Clients can immediately see which groups are high-spenders, moderate-spenders, or low-spenders

### Interpretation
| Region | Profile | Strategy |
|--------|---------|----------|
| **Top-right clusters** | High income + High spending | 🎯 **Premium product targets** |
| **Bottom-left clusters** | Lower income + Low spending | 💰 **Discount/loyalty targets** |
| **Middle clusters** | Moderate spending | 📧 **Personalized campaigns** |

> **Visualization makes it obvious which segments to focus on first.**

---

## ✅ Key Takeaways

- 🔍 **High-value customers are easy to spot** — focus marketing efforts on them first  
- 📉 **Low-spending segments can be nurtured** with discounts and loyalty programs  
- 🎯 **Segment-specific strategies improve ROI** compared to generic campaigns  
- 📊 **Clustering gives a clear, actionable roadmap** to tailor marketing and maximize revenue based on customer behavior

---

## 🛠️ Tools Used
- **Python** (Pandas, Scikit-learn, Matplotlib/Seaborn)
- **Jupyter Notebook** for development
- **Kaggle Dataset**: Mall Customers Dataset

---

## 📁 File Structure