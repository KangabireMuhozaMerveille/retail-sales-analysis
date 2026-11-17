# Retail Sales & Business Performance Analysis

## Project Overview

This project explores retail sales data to evaluate business performance, identify profitability trends, and uncover opportunities for improvement.

Using the Sample Superstore dataset, I performed data cleaning, exploratory data analysis (EDA), and customer-level analysis to understand how sales and profits vary across products, regions, customer segments, and individual customers.

The goal was to move beyond total sales figures and understand what drives business profitability, where losses occur, and which areas may require further investigation.

## Business Questions

This analysis aimed to answer the following questions:

- How do sales and profits change over time?
- Which product categories and subcategories generate the most revenue and profit?
- Which regions contribute most to overall business performance?
- Which customer segments generate the highest sales and profit margins?
- Who are the highest-revenue customers?
- Which customers generate losses despite making purchases?
- Is heavy discounting associated with lower profitability?

## Dataset

**Source:** [Sample Superstore Dataset – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

The dataset contains 9,994 retail transaction records and 21 original columns, covering:

- Order and shipping information
- Customer details
- Geographic information
- Product categories and subcategories
- Sales, quantity, discounts, and profit

## Tools and Technologies

- **Python** – Data analysis
- **Pandas** – Data cleaning, manipulation, and aggregation
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Google Colab / Jupyter Notebook** – Development environment

## Project Workflow

### 1. Data Cleaning and Preparation

The dataset was inspected and prepared for analysis through:

- Checking missing values and duplicate records
- Standardizing column names and text values
- Converting order and shipping dates into datetime formats
- Handling missing postal codes
- Removing the unnecessary Row ID column
- Creating additional time-based features, including order year, month, and year-month
- Calculating shipping duration in days

Negative profit records were retained because they represent loss-making transactions rather than necessarily indicating incorrect data.

### 2. Exploratory Data Analysis

The analysis focused on several dimensions of business performance:

**Sales and Profitability**
- Total sales and profit
- Number of unique orders and customers
- Average order value
- Overall profit margin

**Time-Based Analysis**
- Monthly sales trends
- Monthly profit trends
- Changes in business performance over time

**Product Performance**
- Sales and profit by product category
- Subcategory-level profitability
- Identification of loss-making product areas

**Regional Performance**
- Sales and profit across the four regions
- Number of orders and customers
- Regional profit margins

**Customer Segment Analysis**
- Performance of Consumer, Corporate, and Home Office segments
- Sales and profit contributions
- Comparison of profit margins

**Customer-Level Analysis**
- Top customers by sales
- Customers with the largest recorded losses
- Customer purchasing patterns and order frequency

**Discount and Profitability Analysis**
- Relationship between discounts and transaction profitability
- Average and maximum discounts among loss-making customers
- Identification of customers with high sales but negative total profit

## Key Business Findings

### 1. Regional Performance

The West region was the strongest performer, generating the highest sales and profit.

| Region | Sales | Profit | Profit Margin |
|---|---:|---:|---:|
| West | $725,457.82 | $108,418.45 | 14.94% |
| East | $678,781.24 | $91,522.78 | 13.48% |
| Central | $501,239.89 | $39,706.36 | 7.92% |
| South | $391,721.90 | $46,749.43 | 11.93% |

**Key insight:** The Central region had a considerably lower profit margin than the other regions, indicating a need to investigate its product mix, discounting practices, and operating costs.

### 2. Customer Segment Performance

| Segment | Sales | Profit | Profit Margin |
|---|---:|---:|---:|
| Consumer | $1,161,401.00 | $134,119.21 | 11.55% |
| Corporate | $706,146.40 | $91,979.13 | 13.03% |
| Home Office | $429,653.10 | $60,298.68 | 14.03% |

**Key insights:**
- Consumer generated the highest sales and total profit.
- Home Office had the highest profit margin at 14.03%.
- Corporate maintained a stronger profit margin than Consumer despite generating lower total sales.

### 3. Customer Profitability

Customer-level analysis revealed that high sales do not necessarily translate into high profitability.

- Sean Miller generated $25,043.05 in sales but recorded a total loss of $1,980.74.
- Tamara Chand generated $8,981.32 in profit, the highest among the top 10 customers by sales.
- Cindy Stewart recorded the largest loss among the customers examined, at $6,626.39.

**Key insight:** Evaluating customers using revenue alone can hide significant profitability issues.

### 4. Discounting and Loss-Making Customers

The analysis of the 10 most loss-making customers revealed several instances of relatively high discounting.

Examples included:

- Luke Foster: 32% average discount and 80% maximum discount.
- Sharelle Roach: 37% average discount and 70% maximum discount.
- Henry Goldwyn: 80% maximum discount.

**Key insight:** High discount levels appeared alongside substantial customer losses in several cases. Further transaction-level investigation would be needed to determine the contribution of discounting, product costs, and product mix to those losses.

## Business Recommendations

Based on the findings, the following actions could help improve business performance:

1. **Investigate regional profitability:** Examine the Central region's lower profit margin to identify products, discounts, or costs contributing to weaker performance.
2. **Optimize discount strategies:** Review heavily discounted transactions and consider profitability when setting discount limits.
3. **Strengthen profitable customer segments:** Explore opportunities to grow the Home Office segment while maintaining its relatively high profit margin.
4. **Evaluate customer profitability:** Monitor customer-level profit contributions instead of relying exclusively on revenue and order frequency.
5. **Review product performance:** Identify subcategories with recurring losses and assess their pricing, discounting, and costs.

## Project Structure

```text
retail-sales-analysis/
│
├── data/
│   └── README.md
│
├── images/
│   └── (analysis visualizations)
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_exploratory_data_analysis.ipynb
│
├── README.md
└── requirements.txt
```

## How to Run

1. Clone this repository:

```bash
git clone https://github.com/YOUR-USERNAME/retail-sales-analysis.git
```

2. Navigate into the project directory:

```bash
cd retail-sales-analysis
```

3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

4. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final).

5. Place the dataset in the `data/` directory and run the notebooks in numerical order.

## Conclusion

This project demonstrates how exploratory data analysis can be used to understand retail business performance beyond basic revenue reporting.

By examining sales, profitability, regional performance, customer segments, and discounting patterns, the analysis identified areas of strong performance as well as potential sources of financial losses.

The findings emphasize the importance of monitoring profit margins, evaluating customer profitability, and making data-informed decisions when developing business strategies.

---

**Author:** Your Name  
**Focus:** Data Analysis | Business Intelligence | Python | Data Science