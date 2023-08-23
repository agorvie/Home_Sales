
# Home Sales Challenge Project
Welcome to the Home Sales Challenge Project! In this project, I'll be using SparkSQL to analyze home sales data and extract essential insights.

## Instructions
Import Dependencies: The provided code initializes the Spark environment and imports necessary packages.

Read Data: The code reads the home sales data from an AWS S3 bucket into a DataFrame and creates a temporary view named "home_sales".

Question 1: Calculated the average price for a four-bedroom house sold in each year, rounded to two decimal places. The result is displayed in a DataFrame named avg_price_df.

Question 2: Calculated the average price of homes built in each year that have three bedrooms and three bathrooms, rounded to two decimal places. The result is displayed in a DataFrame named avg_price_by_year_built_df.

Question 3: Determined the average price of homes built in each year with three bedrooms, three bathrooms, two floors, and a size of 2,000 square feet or more, rounded to two decimal places. The result is displayed in a DataFrame named avg_price_by_year_sqft_df.

Question 4: Find the "view" rating for the average price of homes costing $350,000 or more. The query's runtime is measured, and the result is displayed in a DataFrame named avg_home_over_350k_df. The runtime is shown in seconds.

Cache Table: The home_sales temporary table is cached using the command spark.catalog.cacheTable("home_sales").

Check Caching: The code checks if the home_sales table is cached using the command spark.catalog.isCached('home_sales').

Question 4 (Cached): The same query from Question 4 is executed using the cached data. The runtime is measured and displayed, allowing you to compare it to the uncached runtime.

Data Partitioning: The code partitions the formatted Parquet home sales data by the "date_built" field.

Create Parquet Table: A temporary table named home_sales_partitioned is created for the partitioned Parquet data.

Question 4 (Parquet): The same query from Question 4 is executed using the Parquet data. The runtime is measured and displayed for comparison with the cached version.

Uncache Table: The home_sales temporary table is uncached using the command spark.catalog.uncacheTable("home_sales").

Verification: The code checks if the home_sales table is no longer cached and provides a verification message.

## Conclusion
In this Home Sales Challenge Project, I successfully leveraged SparkSQL to analyze a dataset of home sales data and derive key insights. By applying various SQL queries to the dataset, I answered specific questions related to average prices for different home characteristics, such as the number of bedrooms, bathrooms, floors, and size. I also investigated the relationship between "view" ratings and home prices for properties costing $350,000 or more. Additionally, I explored the benefits of caching by measuring query runtimes before and after caching the data, showcasing the performance improvements caching can offer. Moreover, I demonstrated the effectiveness of data partitioning and Parquet format for optimized query performance. Throughout the project, I effectively utilized Spark's capabilities for efficient data manipulation and analysis. This experience not only honed my SparkSQL skills but also highlighted the significance of optimizing data processing techniques to gain valuable insights from large datasets efficiently.
