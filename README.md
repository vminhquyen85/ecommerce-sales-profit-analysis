# ecommerce-sales-profit-analysis
Python notebook analysis of e-commerce sales &amp; profit: trends, category/region performance, correlation, and high-sales low-margin insights.
# E-commerce Sales & Profit Analysis (Python Notebook)

## 1. Project Overview
This project analyzes an e-commerce dataset to understand sales and profit performance over time and across categories/regions.
The analysis is completed in a Python Jupyter Notebook and focuses on actionable business insights.

## 2. Objectives (Research Questions)
- How do Sales and Profit change over time? Are there peak and low months (seasonality/campaign effects)?
- Which Categories and Regions contribute the most to Sales and Profit?
- Does Profit Margin increase with Sales?
- Which high-sales items show relatively low margins (High Sales – Low Margin), and what actions can improve profitability?

## 3. Dataset
**File source:** `(https://www.kaggle.com/datasets/nalisha/e-commerce-sales-and-profit-analysis-dataset?resource=download)`  
**Rows / Columns:** 3,500 rows × 7 columns  
**Time Range:** 2022-01-01 to 2024-12-31

**Columns**
- `Order Date`: date of order
- `Product Name`: product name
- `Category`: product category
- `Region`: sales region
- `Quantity`: units sold
- `Sales`: revenue
- `Profit`: profit

> Note: The dataset does not include COGS/discount/promotion, so margin is calculated as `Profit / Sales` (proxy).

## 4. Tools & Technologies
- Python (pandas, numpy)
- Visualization: matplotlib, seaborn
- Notebook: Jupyter Notebook (`.ipynb`)

## 5. Methodology
### 5.1 Data Preparation / Cleaning
- Converted data types (dates and numeric columns).
- Checked duplicates.
- Outlier handling using IQR method (1.5×IQR) on numeric columns to create a cleaned dataset for analysis.

### 5.2 Exploratory Data Analysis (EDA)
- Monthly aggregation to analyze trends and variations.
- Grouped performance analysis by:
  - Category (Sales, Profit, Profit Margin)
  - Region (Sales, Profit, Profit Margin)

### 5.3 Analysis Beyond Visualization
- Correlation analysis (heatmap) to understand relationships between Quantity, Sales, Profit, and Profit Margin.
- High Sales – Low Margin analysis:
  - Identified categories with high revenue impact but relatively lower margins.
  - Identified top-selling products with the lowest margins.
- Simple what-if scenario:
  - Estimated additional profit if profit margin increases by +1% for top-selling low-margin products (e.g., Smartphone/Tablet).

## 6. Key Findings
- Sales and Profit are strongly correlated, while Profit Margin does not necessarily increase with Sales.
- Monthly performance shows clear variation (peak vs. low months), suggesting time-based effects (seasonality/campaigns).
- High Sales – Low Margin focus:
  - Category-level: prioritize optimizing the largest revenue category first (impact-based).
  - Product-level: within top-selling products, identify those with the lowest margins for targeted improvements.

## 7. Recommendations
- Prioritize margin improvements for top-selling, low-margin products (e.g., Smartphone/Tablet) because small margin gains can yield meaningful profit increases.
- Monitor Profit Margin alongside Sales when planning growth (avoid “high sales, low margin” months).
- Plan inventory and operational readiness around peak months; optimize strategies during low months.

## 8. Limitations
- No COGS/discount/promotion fields are available, so the margin metric used is `Profit / Sales` (proxy).
- Results may change if additional cost or marketing variables are included.

## 9. Repository Structure
- `Minh_Quyen_Vu_Final_Project.ipynb` — final notebook (full analysis)
- `README.md` — project documentation

