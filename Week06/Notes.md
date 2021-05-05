
For this assignment, will work on a dataset consisting of data aggregated from across the world, with data related to the spread of the COVID19 pandemic. Please complete the following tasks:



Obtain the dataset from here: https://coronadatascraper.com/timeseries.csv.zip . Details and some interesting work associated with it is found here: https://coronadatascraper.com/#home
Extract the .csv file from the zipped archive, and load it into a Dask dataframe.
Using this dataframe as the starting point, perform the following steps:
Create a new dataframe object that consists of samples (i.e., rows) corresponding to states in the US.
During the time period 2020-Jan-01 to 2021-Feb-28, rank states in terms of their per-capita mortality? Compute per-capita mortality during a specific period as the ratio of total deaths during that time period, to the average population of the state (compute the average population during the time period).
During the same time period, compute the case fatality rate (CFR) per month, using one of the approaches defined in this scientific brief from the World Health Organization: https://www.who.int/news-room/commentaries/detail/estimating-mortality-from-covid-19. This computation should yield an array of dimensions 50 (states) X 14 (months). State the assumptions you are making in computing this metric.
Using this matrix as input, compute the ranking of states, on how the CFR rate changed over time. This computation will involve an aggregation of of month-to-month changes in CFR. Note that some of these month-to-month changes can be positive (CFR increases from a previous month to the current month) or negative (CFR decrease from a previous month to the current month), or zero (no change in CFR). You need to aggregate these individual changes, across all time periods.
For each of the above operations, explain using appropriate reasoning, whether using a parallelized and/or distributed way of performing the computation makes sense.
