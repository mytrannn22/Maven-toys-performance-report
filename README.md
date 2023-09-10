# [Power BI] Maven Toys Company - Executive Performance Summary

## I. Introduction

### 1. Context

Maven Toys is a fictitious chain of toy stores in Mexico. With first store launched in 1992, by 2016 Maven Toys has expanded to total of 50 stores located in all regions over the country.

The Maven Toys Executive team and Sales team are planning for sales and marketing strategies for the upcoming year. They want to know which stores and products to focus on. This project aims to provide stakeholders with significant insights from sales performance data and give them recommendations to take informative decisions.

### 2. About the Dataset

The dataset was provided by Maven Analytics and it can be found on their [website](https://mavenanalytics.io/blog/maven-toys-challenge). 

This project will use 3 out of 4 CSV files available in the dataset:

- Products table contains the 35 products sold at Maven Toys (each record represents one product), with fields containing details about the product category, cost, and retail price.
- Stores table contains the 50 Maven Toys store locations (each record represents one store), with fields containing details about the store location, type, and date it opened.
- Sales table contains the units sold in over 800,000 sales transactions from January 2017 to September 2018 (each record represents the purchase of a specific product at a specific store on a specific date).

### 3. Project Roadmap

#### 1. Prepare and Process

- Download the csv files and import them to Power BI Desktop.
- Use Power Query to transform data before loading: check and correct the data types, rename the columns in each table, remove unnecessary columns, remove duplicates and blank rows, etc.
- Import Mexico geographical data from the Internet, including cities, states, etc. then use Power Query to merge queries on "Store_Cities" field. 

#### 2. Data modeling

- Create a new dimension table that hold geography data of cities and corresponding regions.
- Create a common date table with the earliest and latest dates from fact table (Sales), add new date columns such as years, months, etc. necessary for the analysis.
- Create relationship between dimension tables and the fact table with one-to-many relationships.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/7f4f83b1-e104-42f4-9255-c57f2f183ba2)

#### 3. Analyze

- Aggregate data and perform calculations to dentify trends and relationships.
- Organize original fields, calculated columns and measures in different folders for better navigation. 
- Divide the report into 3 pages: Summary, Store Performance and Product Performance. 
- Metric selected: Total Sales, Profit, Profit Margin (for all pages), Total Orders (for Summary and Store Performance) and Quantity (Total Units Sold for Product Performance). Some other metrics are also created to compare the performance of stores, such as Average Daily Sales, etc.
- Visualize data, create metric parameters to enable stakeholders to dive deep into data and actively interact with the multi-dimensional report. 


## II. Performance Report

### 1. Performance Summary

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/59bd27d9-9688-4004-b3ae-e48d3c703c5b)

### 2. Stores Performance

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/327b7948-d021-43a7-9be8-d86d888c178b)

### 3. Products Performance

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/c99185d7-b51f-46d9-981c-6fcf4c5b63d1)

## III. Insights and Recommendations

### 1. Overall performance

- Total Sales and Profit share quite similar trend and patterns: slightly increase in Mar to May, followed by a decline in Aug to Sep, before reaching a peak in Dec (holiday seasons, Christmas and New Year gifts, amusement, gathering times).
- Whereas Profit Margin seems to have the reverse pattern, it reached the peak of more than 32% in Aug 2017, then steadily decreases overtime, but always remain above 25%.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/53be241e-a0db-45a2-81e3-9eac47f12a6a)

### 2. Stores

- **Region**: The number of stores and the Total Sales that each region contributes are proportional to each other: 60% of country revenue are derived from The North and the Center, corresponding to 60% of total stores located in these two regions. On average, a store in the Center region has daily sales of $551, $116 higher than the South. The company should prioritize the Center region when consider new stores expansion plan, while some actions can be targeted to the South to improve daily performance.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/2ff798f8-ecae-4860-bcc2-31bede83d641)

- **Location**: Nearly 60% of total Maven Toys stores are located in Downtown area. On average, each store in Airport area generates by far the most daily revenue with $708, exceeds 30% more than stores in other areas. The company should prioritize expanding with new stores in Airports.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/84972864-098e-45b6-8659-907173571ad3)

- **Top performers**: Maven Toys Ciudat de Mexico 1,2 along with Maven Toys Guadalajara 3 are tops stores in terms of Revenue, Order Quantity and Profit, whereas the most profitable store(highest Profit Margin) is Morelia 1 in Michoacan state.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/cc654221-22a8-417a-a415-ac65505c0ead)


### 3. Products

- **Product Categories**: Compare to same periods of 2017, in 2018, almost all categories records increases of 15-20%, noticeably Art & Crafts has grown 2.5 times in sales. However, the reverse trend is seen in Electronics, with the drop of 28% in revenue. Toys are Maven's key products that account for over 35% of total revenue, compared to 15-19% of other categories. In terms of unit quantity, Art & Crafts rank the first place with over 20K units sold each month in 2018. 3 products of Electronics category has the lowest quantity sold, but generates 15% of total revenue, and more noticeably, it brings nearly 25% of total profit of the company. It can be seen that there are significant differences in Profit Margin among product categories: Electronics rank first with over 40% (even almost 50% in earlier months of 2017), while Toys products bring just around 20% of profit margin.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/b19fc684-8d38-4f5d-9861-1cb9ed7ad410)
![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/e641bc10-baa1-48c7-9d7b-c5c86c3abe32)

- **Product**: Lego Bricks is by far the No.1 product in terms of total sales, while Colorbuds rank first in terms of Unit Quantity Sold and Profit. 

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/7229836a-a71f-4262-9089-b1778374534b)

- **Price Ranges**: Over 50% of products have prices from $10 to less than $20. The higher the prices, the less the profit margin.

![image](https://github.com/mytrannn22/Maven-toys-performance-report/assets/140190425/1a49cbc0-43aa-4f14-856f-34a413c9816e)

- **Some recommendations**: Diversify product portfolio, especially in Electronics category as it brings the most profit margin. It's necessary to investigate more on pricing strategies and the relationship among prices - revenue and profit, so that we can make informative decisions on adjusting pricing frames of products to optimize the overall performance.

