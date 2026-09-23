# Customer Shopping Behavior Analysis

## Project Overview

This end-to-end data analytics project examines customer shopping behavior to uncover purchasing patterns, customer segments, product performance, and revenue opportunities.

The project follows a complete analytics workflow: raw CSV data was cleaned and transformed using Python, stored and analyzed in PostgreSQL, and visualized through an interactive Power BI dashboard.

## Project Objectives

The main objectives were to:

* Clean and prepare raw customer shopping data
* Explore customer demographics and purchasing behavior
* Store the cleaned dataset in a PostgreSQL database
* Answer business questions using SQL
* Identify important customer and product trends
* Build an interactive Power BI dashboard
* Transform analytical findings into actionable business insights

## Dataset

The dataset contains approximately **3,900 customer transactions** and includes information about:

* Customer age and gender
* Geographic location
* Products and categories
* Purchase amounts
* Seasons, colors, and sizes
* Subscription status
* Shipping preferences
* Discounts and promotional codes
* Previous purchases
* Purchase frequency
* Customer review ratings

## Tools and Technologies

| Tool                            | Purpose                                          |
| ------------------------------- | ------------------------------------------------ |
| Python                          | Data preparation and transformation              |
| Pandas                          | Data cleaning and exploratory analysis           |
| SQLAlchemy                      | Loading the cleaned dataset into PostgreSQL      |
| PostgreSQL                      | Data storage and business analysis               |
| SQL                             | Querying, aggregation, and customer segmentation |
| Power BI                        | Interactive dashboard development                |
| Google Colab / Jupyter Notebook | Python development environment                   |

## Project Workflow

```text
Raw CSV Dataset
       ↓
Data Exploration
       ↓
Python Data Cleaning
       ↓
Feature Engineering
       ↓
PostgreSQL Database
       ↓
SQL Business Analysis
       ↓
Power BI Dashboard
       ↓
Business Insights
```

## Data Cleaning and Preparation

The data preparation process included:

* Importing and inspecting the CSV dataset
* Checking column names and data types
* Identifying missing values
* Handling missing customer review ratings
* Checking for duplicate records
* Standardizing column names using `snake_case`
* Removing unnecessary or redundant columns
* Creating new analytical features
* Validating the cleaned dataset before database loading

## Feature Engineering

New features were created to support deeper analysis, including:

* **Age groups** for customer demographic analysis
* **Purchase frequency in days** for behavioral analysis
* **Customer segments** based on previous purchase activity

Customers were classified into groups such as:

* New customers
* Returning customers
* Loyal customers

## PostgreSQL Integration

After cleaning the data, the Python DataFrame was loaded into PostgreSQL using SQLAlchemy.

```python
from sqlalchemy import create_engine

engine = create_engine(
    "postgresql+psycopg2://username:password@localhost:5432/customer_behavior"
)

df.to_sql(
    "customer",
    engine,
    if_exists="replace",
    index=False
)
```

> Database credentials are not included in this repository for security reasons.

## Business Questions

SQL was used to investigate questions such as:

1. How does total revenue compare between male and female customers?
2. Which customers used discounts but still spent more than the average customer?
3. Which products received the highest average review ratings?
4. How does average spending differ between Standard and Express shipping?
5. Do subscribed customers spend more than non-subscribed customers?
6. Which products are purchased most frequently with discounts?
7. How are customers distributed among New, Returning, and Loyal segments?
8. What are the three most purchased products in each category?
9. Are repeat customers more likely to subscribe?
10. How much revenue is contributed by each age group?

## Dashboard

The Power BI dashboard provides an interactive overview of customer shopping behavior.

### Main KPIs

* Total number of customers
* Average purchase amount
* Average review rating
* Total revenue

### Dashboard Visualizations

* Revenue by product category
* Sales by category
* Revenue by age group
* Customer subscription distribution
* Customer segmentation
* Purchase behavior by gender
* Shipping and discount analysis

Add a screenshot of the dashboard to the repository and update the filename below if necessary:

```markdown
<img width="1345" height="756" alt="image" src="https://github.com/user-attachments/assets/f85599ff-c6dc-4f5a-8fd1-511f88d65209" />

```

## Key Insights

The analysis revealed several important patterns:

* Clothing generated the highest overall revenue among the product categories.
* Young adult and middle-aged customers made significant contributions to revenue.
* Most customers were not subscribed, indicating an opportunity to improve subscription conversion.
* Loyal and returning customers represented valuable targets for retention campaigns.
* Product performance varied across categories, ratings, and discount usage.
* Discounts influenced purchasing behavior, but they did not always produce stronger customer value.
* Customer segmentation made it easier to identify groups requiring different marketing strategies.

## Business Recommendations

Based on the analysis, the business could:

* Create targeted campaigns for high-value age groups
* Develop personalized offers for loyal and returning customers
* Encourage non-subscribers to join the subscription program
* Promote highly rated and frequently purchased products
* Review the effectiveness of discount campaigns
* Use customer segments to improve marketing personalization
* Introduce loyalty benefits to encourage repeat purchases
* Optimize inventory around high-performing categories and products

## Repository Structure

```text
customer-shopping-behavior-analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── notebooks/
│   └── customer_behavior_analysis.ipynb
│
├── sql/
│   └── customer_behavior_queries.sql
│
├── dashboard/
│   ├── customer_behavior_dashboard.pbix
│   └── dashboard.png
│
├── .gitignore
└── README.md
```

The folder names can be adjusted to match the actual structure of this repository.

## How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
cd customer-shopping-behavior-analysis
```

### 2. Install the Python libraries

```bash
pip install pandas sqlalchemy psycopg2-binary jupyter
```

### 3. Create the PostgreSQL database

Create a PostgreSQL database named:

```text
customer_behavior
```

### 4. Configure the database connection

Update the connection details in the notebook with your own PostgreSQL username, password, host, port, and database name.

Do not upload real passwords or other database credentials to GitHub.

### 5. Run the notebook

Open the notebook using Google Colab or Jupyter Notebook and execute the cells in order.

### 6. Run the SQL analysis

Open `customer_behavior_queries.sql` in pgAdmin and execute the queries against the `customer_behavior` database.

### 7. Open the dashboard

Open the `.pbix` file using Power BI Desktop. Update the PostgreSQL connection if Power BI requests database credentials.

## Skills Demonstrated

This project demonstrates practical skills in:

* Data cleaning and transformation
* Exploratory data analysis
* Feature engineering
* Python and Pandas
* PostgreSQL database integration
* SQL querying and aggregation
* Customer segmentation
* Business problem solving
* Power BI dashboard development
* Data visualization and storytelling
* End-to-end analytics workflow design

## Future Improvements

Possible future improvements include:

* Predicting customer purchasing behavior using machine learning
* Building a customer churn prediction model
* Calculating Customer Lifetime Value
* Developing a product recommendation system
* Adding sales forecasting
* Automating the data-loading pipeline
* Publishing the dashboard through Power BI Service

## Project Background

This project was completed as a guided portfolio project based on a data analytics tutorial. I independently followed and implemented the complete workflow to strengthen my practical understanding of Python, PostgreSQL, SQL, and Power BI.

Tutorial: [Customer Shopping Behavior Data Analytics Project](https://youtu.be/5PrZvPeUw60)

## Author

**Radka Angel**

Software Engineering graduate developing practical expertise in data analytics, backend development, SQL, and business intelligence.

* GitHub: [Add your GitHub profile](YOUR_GITHUB_URL)
* LinkedIn: [Add your LinkedIn profile](YOUR_LINKEDIN_URL)

## Acknowledgements

Thanks to the original tutorial creator for providing the project guidance and dataset used as the foundation for this learning project.
