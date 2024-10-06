# Home Sales Big Data Analysis with SparkSQL/PySpark

This project involves analyzing home sales data using SparkSQL/PySpark. The goal is to gain insights into home prices by running various SQL queries, leveraging caching for performance improvements, and using partitioned parquet data for efficient data management. This analysis focuses on understanding price trends based on home features, including the number of bedrooms, bathrooms, and views, as well as how these trends vary over time.

## Summary
The project explores a dataset of home sales using PySpark, with the following key tasks:
- Loading the home sales data into a Spark DataFrame.
- Performing SQL queries to extract valuable insights, such as the average home price per year for different property types.
- Utilizing caching to optimize query performance and comparing the execution times of cached versus uncached data.
- Partitioning the dataset by `date_built` and saving it as Parquet files to manage data more efficiently.
- Rerunning queries on the parquet data and comparing performance with cached data.
- Ensuring that caching and uncaching operations are correctly implemented and verified.

By the end of this project, we will understand how data can be processed and analyzed using PySpark, and how performance improvements can be achieved by leveraging caching and partitioning strategies.

## Instructions

### 1. File Renaming
Rename the `Home_Sales_starter_code.ipynb` file as `Home_Sales.ipynb`.

### 2. Import Required Libraries
Import the necessary PySpark SQL functions required for the assignment.

### 3. Load Data
Read the `home_sales_revised.csv` data file into a Spark DataFrame.

### 4. Create Temporary Table
Create a temporary table named `home_sales` from the DataFrame to facilitate SQL queries.

### 5. SQL Queries

#### a) Average Price for Four-Bedroom Homes (Per Year)
Write a query to calculate the **average price of a four-bedroom house** sold each year, rounded to two decimal places.

#### b) Average Price of Homes with Three Bedrooms and Bathrooms (Per Year)
Write a query to calculate the **average price of homes** that have three bedrooms and three bathrooms, for each year they were built, rounded to two decimal places.

#### c) Average Price of Large Homes with Specific Criteria (Per Year)
Write a query to calculate the **average price of homes** that meet the following conditions:
- Three bedrooms
- Three bathrooms
- Two floors
- Living area greater than or equal to 2,000 square feet.

The result should be grouped by the year the homes were built and rounded to two decimal places.

#### d) Average Price of Homes with View Rating Above $350,000
Write a query to calculate the **average price of homes per "view" rating** where the average home price is greater than or equal to $350,000. Record the runtime for this query and round off the average price to two decimal places.

### 6. Cache the Temporary Table
Cache the `home_sales` temporary table to optimize query performance.

### 7. Verify Cached Table
Ensure that the temporary table is cached using the appropriate PySpark function.

### 8. Rerun Query on Cached Data
Rerun the query from step 5(d) on the cached data and measure the runtime. Compare the cached runtime with the uncached runtime.

### 9. Partition Data by `date_built`
Partition the home sales dataset by the `date_built` field and save the formatted data as Parquet files.

### 10. Create Temporary Table from Parquet Data
Create a temporary table from the Parquet data to enable further analysis.

### 11. Rerun Query on Parquet Data
Rerun the query from step 5(d) on the Parquet temporary table and compare its runtime with the cached and uncached runtimes.

### 12. Uncache the `home_sales` Table
Uncache the `home_sales` temporary table to free up memory resources.

### 13. Verify Uncached Table
Verify that the `home_sales` temporary table has been uncached using PySpark.

## Contact

Thay Chansy - [@thaychansy](https://twitter.com/thaychansy) - or thay.chansy@gmail.com


Please visit my Portfolio Page: thaychansy.github.io (https://thaychansy.github.io/)
