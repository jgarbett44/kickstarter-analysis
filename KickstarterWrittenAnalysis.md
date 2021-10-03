# Kickstarting with Excel

## Overview of Project

Louise is looking to fund her new play using a Kickstarter campaign. To maximize her chances for success, we are looking for trends or for other insight in an excel file that contains data for comparable campaigns.

### Purpose

After observing one play near its goal quickly, Louise wants to look at the outcome of theater campaigns, especially plays, in relation to their launch dates and their funding goals, to see what she can learn.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

It's possible that the time of year when a campaign is started makes a difference in its outcome. By comparing outcomes with launch dates in the data, we can see what months have shown the greatest success or failure. Also, we can sort the data to show only theater events, or we can drill down further to see only plays, so that Louise can find the closest comparison to her campaign.

Starting with a pivot table filtered by the years and the parent category, then filtered to show only successful, failed, and canceled events, I created two charts, Outcomes Based on Launch Date and Theater Outcomes by Launch Date:

https://github.com/jgarbett44/kickstarter-analysis/blob/main/OutcomesBasedonLaunch_all.png
https://github.com/jgarbett44/kickstarter-analysis/blob/main/Theater_Outcomes_vs_Launch.png


### Analysis of Outcomes Based on Goals

In addition to launch date, the amount of the goal is likely to effect the outcome. To make for a good comparison, I divided the goal amounts into 12 rows, starting with "less than 1000" and ending at "50,000 or more". Next I used the COUNTIFS function to calculate the number successful, the number failed and the number canceled.  Finally, to visualize this relationship between the goal and the result, I created a line chart:

https://github.com/jgarbett44/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png


### Challenges and Difficulties Encountered

Seeing 0 for all goal numbers made me question whether the COUNIFS formula was done properly, so I checked the raw data. It confirmed that there were no canceled plays, regardless of the goal amount. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

May is the best month to start a kickstarter, with the greatest percentage of outcomes being successful. Also, it is the month with the greatest quantity of successful outcomes. On the other hand, December has lowest quantity of successful outcomes, and February and March show nearly as many failures as successes. So December, February and March are the worst months to launch.

- What can you conclude about the Outcomes based on Goals?

The lower the goal, the higher the chance for success. Also, the vast majority of campaigns (889 of 1047 or 85%) had a goal under $10,000.

- What are some limitations of this dataset?

For goals above $25,000, there is so little data that conclusions are less firm than they can be for the smaller amounts. Also, by looking at months and not years for the launch date, we are not taking into account larger events, like a pandemic, that could skew the data.

- What are some other possible tables and/or graphs that we could create?

We could incorporate years into our pivot table to identify outliers, like 2020 COVID, that might affect the data. Also, we could chart outcomes among all categories to see how often theater events are successful compared to other types of campaigns.
