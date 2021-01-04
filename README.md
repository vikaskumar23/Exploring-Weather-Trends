# Exploring weather trends
The objective of this project to analyze weather data from a given data set using Excel, Google sheets, Python or R and create a report based on that analysis.

## Introduction
In this project we will analyze New Delhi and global weather data to compare the weather trends of New Delhi to overall global temperature trends. We will try to find some insights like:
- Trends in Delhi and Global Temperature
- Is there any relation between Delhi and Global Temperature
- which has more variability in temperature and many more...

## Data Required for Project

**weather_data.csv :** This dataset is extracted from udacity sql workspace that contain ```global``` and ```all cities of world``` weather data (in celcius) from year 1796 to 2013. 
- Following query is used to extract the data:
    ```
    select c.year, c.avg_temp as city_temp, g.avg_temp as global_temp
    from city_data c
    join global_data g on c.year=g.year
    and c.city='Delhi'
    order by 1;
    ```
- This dataset has 3 columns
    - **year** : Year in which temperature is recorded
    - **city_temp** : Temperature of Delhi city in the given year
    - **global_temp** : Global Temp in the given year

- Quality issue with the dataset
    - **city** weather data has some empty fields

## Steps performed to prepare the data for analysis
1. Data is extracted from udacity sql workspace using sql query.
2. Data is loaded in Excel.
3. Calculated the average of city_temp and fill all the null cells in city_temp with the average value.
4. Then calculated the moving average for both city data and global data.
5. Then created plots to anlyze trends

## Calculation of Moving Average
- Select and go down till the 5th row of city_temp and use AVERAGE() function to calculate the average temperature for the first 5 years in a new column.
- Then drag the same formula till the end of data
- Repeat the above 2 steps for global data also and finally we have running average for city and global weather data.

## Analysis Process
- Bivariate plots like line and scatter plots are created for the analysis.
- Then statistical analysis is performed
- Analysis reported is included in the repo with name ```weather_trends.pdf```

## References
www.udacity.com