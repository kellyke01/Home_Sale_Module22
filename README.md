In this module I first imported the PySpark SQl function into the notebook. I then had it read the revised csv in the starter code into a spark Dataframe.
I made a temporary table called home_sales. 
I was then able to set up a sql for each of these questions in the DataFrame:
  What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
  What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
  What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
  What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? 
    Determine the run time for this last query, and round off your answer to two decimal places.

I then cached my table home_sales and checked to make sure it was cached.
Using the cached data I ran the last sql query that calculated the average price of a home per "view" rating having an average home price greater than or equal to $350,000.
I also determined the run time and compared it to the uncached runtime. 
In this I determined that cached time was cut in half compared to the original run time before i cached the data.

After I ran those querys I partitioned by the 'date_built' field on the parquet home sales data and again ran the same query in this new table.
I compared it to the unchache runtime and it was about the same time, if not a little faster, than the cached data.

At the end of the assignment I uncached the home_sales temporary table and verified it is now uncached using PySpark.
