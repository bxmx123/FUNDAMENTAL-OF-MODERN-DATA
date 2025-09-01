# README – Modern Data Exploration with BI Tools
*(Based on Online Retail Dataset, using Power BI Desktop)*

## 1. Project Background
This project leverages a real-world dataset (**Online Retail, 2009–2011**) and explores it with **Power BI Desktop** to simulate data-driven business decision-making in a retail e-commerce scenario.

## 2. Business Questions
The analysis focuses on three questions:
1. **Sales trends**: Are there seasonal or yearly sales patterns?
2. **Customer value**: Which customers contribute the most, and is revenue concentrated?
3. **Returns**: Are returns concentrated in specific countries or products?

## 3. Data Source
- Kaggle: [Online Retail Dataset (UCI)](https://www.kaggle.com/datasets/vijayuv/onlineretail)  
- Data scope: 2009–2011, 541,909 transactions, fields include InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country.

## 4. Data Preprocessing
In Power Query:
- Changed data types: InvoiceDate → Date/Time; Quantity → Integer; UnitPrice → Decimal; CustomerID → Integer.
- Removed invalid rows: UnitPrice ≤ 0; marked Quantity < 0 as returns.
- Handled missing values: Description Null → “Unknown Product”; CustomerID Null → removed.
- Derived fields:
  - Total Sales = Quantity × UnitPrice
  - YearMonth = FORMAT(InvoiceDate, "YYYY-MM")
  - IsReturn = IF(Quantity < 0, "Return", "Sale")

## 5. Visualizations
The dashboard includes 5 visuals:
1. Sales trend line chart (YearMonth vs Total Sales)
2. Sales by country bar chart (Country vs Total Sales)
3. Returns vs sales pie chart (IsReturn vs Total Sales)
4. Top 10 customer spending bar chart (CustomerID vs Total Sales)
5. Product sales treemap (Description vs Quantity)
+ Slicers: YearMonth, Country, CustomerID.

## 6. Insights
- Sales show seasonal peaks.
- A small group of customers contribute a large share of sales → concentration risk.
- Returns are concentrated in certain products and countries, possibly due to logistics or product issues.

## 7. Recommendations
1. Boost promotions and stock before seasonal peaks.
2. Maintain key customers and expand mid/low-tier customers.
3. Investigate high-return products/countries, improve quality/logistics.
ntation (this file)
│-- PPT_Slides.pptx        # Presentation slides
```
