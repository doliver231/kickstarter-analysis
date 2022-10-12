# Kickstarting with Excel

## Overview of Project

Louise intends to fund her play, *Fever*, with a specific budget and limited resources. In order for her to reach her goals and become successful, Kickstarter data was analyzed from other global crowdfunding campaigns over the years to uncover trends related to theatrical play projects.

### Purpose

The purpose of the Kickstarter analysis is to determine how specific factors in crowdfunding campaigns affect whether one can be successful, specifically regarding *when* campaigns are being launched and proposed funding goals.

## Analysis and Challenges

The Kickstarter dataset contained a lot of information, and it was necessary to condense the data as much as possible. First step to do was to apply any necessary filters to target the categories of interest. In this project, our main focus was on any campaign relating to theatrical plays.

### Analysis of Outcomes Based on Launch Date

In this section of the analysis, the goal was to determine any trends relating launching campaigns at certain times of the year and their outcomes, whether it succeeded, failed, or got cancelled. The first step was to isolate the specific dataset to analyze by creating a Pivot Table. In this table, the columns were assigned to the outcomes of the campaigns, and the rows to dates that they were launched. For better clarification, these dates were grouped into months of the year. Filters, such as "Parent Category" and "Year", were added as well to focus specifically on theater campaigns between 1970 and 2017. The "cancelled" outcomes were also removed from the table to focus mainly on whether campaigns succeeded or failed. Another Pivot Table was also created with the data filtered specifically for theaterical plays instead of its parent category, "theater". Pivot Charts in the form of line graphs were created based on the data in the tables to visually show the correlation between launch date and outcome of the campaign.

![Theater Outcomes vs. Launch Dates](https://github.com/doliver231/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

![Play Outcomes vs. Launch Dates](https://github.com/doliver231/kickstarter-analysis/blob/main/Resources/Play_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

For this analysis, the focus was made on the funding goals of each campaign and how that could have an effect on the outcomes. The funding goals dataset is substantial and with a big range. Therefore, the best option was to group the goal amounts into different ranges, such as "less than 1000", "1000 to 4999", and so forth. Using the COUNTIFS function, a table was created to feature the counts of outcomes for each range of goal amounts. Within the COUNTIFS functions used, specific criteria were designated such as the data points needed to be for plays and specific for each outcome category. Using SUM function, the total number of projects were calculated in the table for each range of goal amounts. Percentages of the total campaign projects for each outcome were then calculated and displayed on a line graph.

![Outcomes vs. Goals](https://github.com/doliver231/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

One challenge that was encountered was using the COUNTIFS function properly. The main point was to count the amount of data points at a certain range of funding goal amounts, for each outcome category. But these points needed to be filtered to display only those relating to theatrical play campaigns. Applying a filter on the original Kickstarter worksheet to display only "play" compaign projects was not enough. One needed to add that specific criteria within the COUNTIFS function to actually have a filtered dataset displaying only those relating to plays. It is very easy to omit something so small within a function, not notice it, and have it display an error. This can even be applied to the properly converting the Unix Time Stamps within the Kickstarter dataset to understandable date formats. It is all a matter of trial and error, and eventually discovering what are missing within the Excel functions used.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date? Based on launch date, one can conclude that successful outcomes tend to occur at the start of the summer season. We can see that by the month of May, there was a spike of successful outcomes for theater campaigns, from 71 to 111. That trend slowly declined as the weather turned colder and the months neared the end of the year. Specifically for play campaigns, the trend was exactly the same, spiking during the month of May from 57 to 93, and slowly declining as the months progressed. We can also conclude that during the month of December, there was very close to 50/50 successful to failed theaterical projects, specifically plays. The trend of cancelled theater projects remained pretty constant throughout the year, with January being that one time range with the most.

- What can you conclude about the Outcomes based on Goals? It is clear that there are far less campaigns happening with funding goals greater than $5,000. The rate of succession decreases as the funding goal amounts increase. The percentage of successful campaigns range from 73-76% for goals under $4,999. The percentage of failed campaigns are at their highest with funding goals greater than $45,000, despite the small amount of campaigns in that range. Louise should lower her estimated budget for her play if she wants a good chance at becoming successful.

- What are some limitations of this dataset? One limitation that this dataset has is there aren't enough campaigns relating to theatrical plays. The Kickstarter workbook contains data from campaigns from all over the world, from different time periods, and falling under a multitude of different categories. However, we are trying to pinpoint those that are as closely similar to Louise's crowdfunding project for a US play with an estimated budget of $10,000. Only about 16% of the Kickstarter workbook shows play campaigns in the US that can be useful for any analysis, which is not enough.

- What are some other possible tables and/or graphs that we could create? Other possible visualizations that can be created could be comparing outcomes by country. Every country has their own currency, culture, and other factors that can play a part in whether a campaign will be successful or not. Maybe during the month of May, the rate of succession is at its highest in the US, but in a country whose in a completely different time zone, this might not be the case at all. Another table/graph can be possibly made comparing the succession of different parent-subcatergory campaigns, such as theater-plays versus theater-musicals.