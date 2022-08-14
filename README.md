# 911-Calls-Capstone-Project

## Overview

For this capstone project I analyzed 911 call data from a Kaggle data set leveraging the NumPy, Pandas, Matplotlib, and Seaborn libraries. I found that the zip code 19401 had the most 911 calls with 6979 reported calls, while Lower Merion had the highest 911 calls of all townships with 8443 calls. Furthermore I created visualizations to understand the reasons/departments for a 911 call, and the most popular days of the week and months of the year with average 911 calls. Below are my results.

### Calls by Department
![capstone_project_pic_1.png](capstone_project_pic_1.png)

I ran a simple lambda function to create a new column splitting the title of the reason. In doing so, I found that the three reasons for 911 calls were to contact EMS (48877 calls), the Traffic department (35695 calls), and the Fire department (14920 calls).

### Calls by Day of the Week
![capstone_project_pic_2.png](capstone_project_pic_2.png)

Next I aggreagated my data to focus on the day of the week from 2015 to 2020 to analyze trends. The bar chart above visualizes that EMS 911 calls occur the most on Fridays with around 7,500 calls, and the least on Sundays with around 6,500 calls. Similarly traffic 911 calls occur the least on Sundays with around 3,500 calls, but the most 911 calls fall on Tuesday with around 6900 calls. However fire 911 calls are around the same number of calls regardless of the day of the week, hovering around 2100 calls per day of the week.

### Calls by Month over the Past Year
![capstone_project_pic_3.png](capstone_project_pic_3.png)

Then I took a step back and focused on each month between 2015 to 2020 to analyze trends. The bar chart above visualizes that EMS 911 calls occurred the most in January with just over 6,000 calls, and the least in December with around 3,900 calls. Similarly traffic 911 calls occur the most in January with around 5,200 calls, and the least calls fall in December with around 3000 calls. Fire 911 calls occur the most in January and July with around 1,900 calls, and the least in December. I'm not surprised that fire department 911 calls occur the most in July due to the weather/temperature as it is a peak month of summer where the weather can be hot and dry.

## Filling in the Missing Data

As you will notice, the above graph is missing data for a few months. I accounted for this by filling in information by creating a groupby object called byMonth, where I grouped the DataFrame by the month column and used the count() method for aggregation. I also leveraged seaborn's lmplot() to create a linear fit on the number of calls per month to determine is my plot is accurate. 

### My simple line plot that fills in the missing months:
![my_aggregation_attempt.png](my_aggregation_attempt.png)

### Seaborn's lmplot()
![seaborns_attempt.png](seaborns_attempt.png)

Ultimately my aggregation and Seaborn's lmplot() assume that September, October, and November is trending downwards for total 911 calls. With my methodology, September had around 8,750 calls, October had around 8,500 calls, and November had around 8,250 calls. Seaborn estimates that September was between 9,000 to 11,900 calls (likely 9,500 calls), October was between 8,500 to 11,990 calls (likely 9,250 calls), and November was between 8,000 to 11,990 calls (likely 9,000 calls). I believe both models are effective as Seaborn provides a more accurate range of calls, but my aggregated model is likely a more accurate representation of the total 911 calls.

## Diving Deeper

### 2016 Aggregated 911 Calls Data

After observing the data at a high level by departement, and timestamp in general, I dove into the data provided for the year 2016 to see if I could find any interesting trends. Below is an image of the overall 911 call data from 2016:

![capstone_project_pic_4.png](capstone_project_pic_4.png)

### 2016 
![capstone_project_pic_5.png](capstone_project_pic_5.png)

Cool heatmaps
![capstone_project_pic_6.png](capstone_project_pic_6.png)

![capstone_project_pic_7.png](capstone_project_pic_7.png)
