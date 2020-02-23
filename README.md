# Airline on time performance
## by Carolina Negrelli


## Dataset

This data set contains information about 7.5 million flights in USA for 2019. It has a lot of basic information such as Date, Time, Airline, Delays and Cancellations. I had remove 55 points with really large delay times.

This data set is one of the selected by Udacity. But the file has been deleted from the source given in the dataset options [here](http://stat-computing.org/dataexpo/2009/the-data.html), insteed I had to go to the original source and download the full table [here](transtats.bts.gov/DL_SelectFields.asp). I downloaded the data from January 2019 to December 2019.


## Summary of Findings

In this exploration I investigate the relation between all variables. I found some things that I expected such as a huge correlation between Departure Delay and Arrival Delay or Distance and Elapsed Time. There are three main paths in this exploration:

- How delays correlates (or not) with other features such as Airline, Departure Airport, Route (combination of Departure and Arrival airports), Time, Date (Month and Day of Week), Elapsed Time.  
- What are the main causes of cancellations and how the cancellations are how this depend (or not) with the Origin Airport or Month.
- How some of the explored correlations change (or not) when we consider only flight from Rochester, NY (ROC airport), the city where I live.

I have found that delays have a bimodal distribution, with most of the delays around 20min and a little peak on large delays around 15hs. The delays have a little correlation with Airport, Airline and route. I expected that the Airlines with most flights to have the larger delays but this is not true. There is no relation between delays and Elapsed time or Departure Time. When we combine Day of Week and Month we notice that there are some combinations where the delays are considerably larger and some considerably low. The same happens when we combine Airline and Airport.  

Less than 2% of flights were cancelled. The cancellations are primary due to Weather followed by Carrier and National Air System. When we look by Airport this order is the same but some airports have really similar counts for two or three reasons. There are some specific routes that have a bigger count of cancellations. When we look by Month there ir some changes, but the tendency continuos the same.

When we look only Rochester the realations are very similar except for the combination of Day of Week and Month, there is no standing points in this case.




## Key Insights for Presentation

For the presentation, I focus on the features with more relation with the delays. First I present the distribution of the delays and then I show which are the airlines with most mean delays. Then I keep only the departure airports with most flights and plot which is the mean delays for them. Last, I show how the mean delays depends on the combination of Month and Day of Week. 

## Files:

exploration.ipynb: notebook with the exploratory data analysis.

exploration.html: exploratory data analysis in html.

slide_deck.ipynb: notebook with explanatory analysis.

slide_deck.html: presentation slides with the explanatory analysis.

I can't upload the data files due to the limited space (in Udacity and Github). To obtain the files you have to go to transtats.bts.gov/DL_SelectFields.asp and select the option all for all the months of 2019. You can download only one month at time, so you need to downoload 12 files. I haven't change the names of the files.  


## Sources:

transtats.bts.gov/DL_SelectFields.asp

http://stat-computing.org/dataexpo/2009/the-data.html

http://stat-computing.org/dataexpo/2009/supplemental-data.html

https://stackoverflow.com/questions/20906474/import-multiple-csv-files-into-pandas-and-concatenate-into-one-dataframe

https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.sort_values.html

https://seaborn.pydata.org/generated/seaborn.barplot.html

https://stackoverflow.com/questions/12096252/use-a-list-of-values-to-select-rows-from-a-pandas-dataframe
