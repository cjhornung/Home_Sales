# Home_Sales
In this challenge, I used SparkSQL to determine key metrics about home sales data. 

## Methodology: 
- Spark to create temporary views
- Partition the data, cache and uncache a temporary table, and 
- Verify that the table has been uncached.

## Results:
1: A Spark DataFrame is created from the dataset:

![1](https://github.com/cjhornung/Home_Sales/assets/134234019/40b6fdfd-6678-4fbc-a11b-7e3fcacc1b09)

2: A temporary table of the original DataFrame is created:

![2](https://github.com/cjhornung/Home_Sales/assets/134234019/ec9662c8-52f3-4982-a892-7a8c6742bd9e)

3: A query is written that returns the average price, rounded to two decimal places, for a four-bedroom house that was sold in each year:

![3](https://github.com/cjhornung/Home_Sales/assets/134234019/32525914-e410-4876-afbd-01583b949467)

4: A query is written that returns the average price, rounded to two decimal places, of a home that has three bedrooms and three bathrooms:

![4](https://github.com/cjhornung/Home_Sales/assets/134234019/51a55592-8e16-4fc7-bb14-6a0cb9e2fd41)

5: A query is written that returns the average price of a home with three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet for each year built rounded to two decimal places:

![5](https://github.com/cjhornung/Home_Sales/assets/134234019/8e23effb-0790-4e40-a32d-e9dd015b28d7)

6: A query is written that returns the view rating for the average price for homes that are greater than or equal to $350,000, rounded to two decimal places:

![6](https://github.com/cjhornung/Home_Sales/assets/134234019/4517afb9-d93d-404d-9679-8d84b1c6790f)

7 - 8: A cache of the temporary "home_sales" table is created and validated:

![7](https://github.com/cjhornung/Home_Sales/assets/134234019/d9d8219f-c4dd-4eea-a071-2dc56da6abf8)

9: The query from step 6 is run on the cached temporary table, and the run time is computed:

![8](https://github.com/cjhornung/Home_Sales/assets/134234019/84e5cf74-82f1-43b2-869d-0015f922fb40)

10 - 11: A partition of the home sales dataset by the "date_built" field is created, and the formatted parquet data is read:

![9](https://github.com/cjhornung/Home_Sales/assets/134234019/6b77f961-fedd-4795-b0ff-294a47a0136b)

12: A temporary table of the parquet data is created:

![10](https://github.com/cjhornung/Home_Sales/assets/134234019/41fa5ef0-c72a-4133-a6d9-216b8e1abe2d)

13: The query from step 6 is run on the parquet temporary table, and the run time is computed:

![10](https://github.com/cjhornung/Home_Sales/assets/134234019/6064ecf8-2c08-440a-bd4f-ec6eedbec62a)

14 -15: The "home_sales" temporary table is uncached and verified:

![11](https://github.com/cjhornung/Home_Sales/assets/134234019/dfa52c65-b27d-4f8f-af02-0c3dd6276ed3)
