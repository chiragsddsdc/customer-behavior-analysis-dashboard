#  Customer Behavior Analysis & Visual Reporting

##  About
A data analytics project analyzing **3,900 customer shopping records** to uncover purchasing patterns, segment customers, and identify revenue drivers. Complete pipeline from data cleaning to PostgreSQL export to Power BI dashboard.

##  Tech Stack
- **Language:** Python, SQL
- **Libraries:** Pandas, NumPy, SQLAlchemy
- **Database:** PostgreSQL
- **Dashboard:** Power BI

##  Dataset
- **Records:** 3,900 customer entries
- **Features (18):** Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount (USD), Location, Size, Color, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Payment Method, Frequency of Purchases

##  What I Did

### 1. Data Cleaning & Feature Engineering
- Imputed missing Review Ratings using **category-wise median** (grouped imputation)
- Renamed all columns to snake_case for consistency
- Created **Age Group** using quartile binning (Young Adult / Adult / Middle-Aged / Senior)
- Created **Purchase Frequency Days** — mapped text frequencies to numeric days (Weekly=7, Monthly=30, Quarterly=90, etc.)
- Identified and dropped **redundant column** (promo_code_used was identical to discount_applied)

### 2. SQL Analysis (10 Advanced Queries)
| Query | Technique Used |
|-------|---------------|
| Total revenue by gender | GROUP BY, SUM |
| High spenders with discounts (above avg) | Subquery |
| Top 5 products by review rating | GROUP BY, AVG, ORDER BY |
| Avg purchase: Standard vs Express shipping | WHERE, GROUP BY |
| Subscriber vs non-subscriber spending | GROUP BY, Aggregation |
| Top 5 products by discount usage rate | CASE, Aggregation |
| Customer segmentation (New/Returning/Loyal) | CTE, CASE Statement |
| Top 3 products per category | CTE, Window Function (ROW_NUMBER) |
| Repeat buyers subscription analysis | WHERE, GROUP BY |
| Revenue contribution by age group | GROUP BY, ORDER BY |

### 3. Power BI Dashboard
- Built an interactive dashboard tracking:
  - Revenue breakdown by gender
  - Category-wise performance
  - Customer segmentation (New / Returning / Loyal)
  - Discount impact on revenue
  - Subscription status analysis
  - Age group revenue contribution

##  Project Structure
```
├── customer_shopping_behavior.csv                 # Dataset
├── Customer_Shopping_Behavior_Analysis.ipynb       # Python Notebook
├── customer_behavior_sql_queries.sql               # 10 SQL Queries
├── Customer_Dashboard.pbix                         # Power BI Dashboard (optional)
└── README.md                                       # Project Documentation
```

##  How to Run
1. Clone this repository
   ```bash
   git clone https://github.com/chiragsddsdc/customer-behavior-analysis-dashboard.git
   ```
2. Install dependencies
   ```bash
   pip install pandas numpy sqlalchemy psycopg2-binary
   ```
3. Open the notebook
   ```bash
   jupyter notebook Customer_Shopping_Behavior_Analysis.ipynb
   ```

##  Contact
- **Email:** chiragyadav2424@gmail.com
- **GitHub:** [github.com/chiragsddsdc](https://github.com/chiragsddsdc)

