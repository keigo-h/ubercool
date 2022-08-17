# Tech Report
This is where you can type out your tech report.

### Where is the data from?
<br />
We collected our data from the city of Chicago’s database. We were able to make google searches and look through data.gov, to find government data on rideshare stats, along with data on covid in Chicago.The Chicago data portal contains data about a multitude of things in Chicago. <br /><br />

### How did you collect your data?
<br />
We collected data utilizing an api call to data in json form which we will parse to collect and store the data to use for our desired application. <br /><br />

### Is the source reputable?
<br />
We believe that this source is reputable since it comes directly from the city and not through some third party vendor such as Kaggle. Although Kaggle often contains reputable data, it is not always the case and is difficult to verify. This city can ensure that the data they collect is accurate and there is less work on our side to ensure if it is reputable. <br /><br />

### How did you generate the sample? Is it comparably small or large? Is it representative or is it likely to exhibit some kind of sampling bias?
<br />
We generated the sample by parsing json data provided to us by the city of Chicago. The data for ride sharing was collected because of a requirement as a part of a routine reporting thus the sampling is quite accurate in relation to the city of Chicago. This is not a piece of data rather it is viewing the city as a whole. If we were to look at the state of Illinois, and use the city of Chicago’s data it may lead to some inaccuracies since the city will not be representative of small suburban cities.<br />

With regards to the COVID data, the sample will more than likely be comparably small, since there are many cases where the tests are not reported to the city (at home test, not testing, not reporting, testing out of city/state).There will likely be a sampling bias since it will only show tests reported to the city. However, many tests were provided by the city thus, the data is still usable. We must be aware of these possible biases and possibly account for it to ensure the integrity of our results.<br /><br />



### Are there any other considerations you took into account when collecting your data? This is open-ended based on your data; feel free to leave this blank. (Example: If it's user data, is it public/are they consenting to have their data used? Is the data potentially skewed in any direction?)
<br />
For the ride share data there is no personal data, such as user-name, credit card info, however, data such as location, distance, price are visible. When using the ride share app, users are consenting to have this data shared and is made public to a certain degree by the city. As explained previously, this data is collected as a requirement by the city, thus it is unlikely to be extremely skewed in any one direction.
The covid data will be biased towards those using public services to get tested rather than testing at home or testing at a private clinic. The numbers may be lower, since not all tests are reported and many people who are positive are not testing which will skew the data. <br /><br />



### How clean is the data? Does this data contain what you need in order to complete the project you proposed to do? (Each team will have to go about answering this question differently, but use the following questions as a guide. Graphs and tables are highly encouraged if they allow you to answer these questions more succinctly.)
<br />
The data has been cleaned. There are many data points which we do not require, so we made sure to exclude those data points. We extracted all the data points that are required for our project idea. We have data sets that are stored by day for every month, and another data set which consists of the averages for every month. Depending on how our project progresses we may change how we filter our data. 

Before cleaning the datapoints were:<br />
![uncleaned](https://github.com/cs1951a-brown-spring-2022/ubercool/blob/main/data_deliverable/reports/tech_report/Data_Point_Screenshots/uncleaned.png?raw=true)

After cleaning the datapoints we are using are:<br/>
![uncleaned](https://github.com/cs1951a-brown-spring-2022/ubercool/blob/main/data_deliverable/reports/tech_report/Data_Point_Screenshots/cleaned.png?raw=true)

### How many data points are there total? How many are there in each group you care about (e.g. if you are dividing your data into positive/negative examples, are they split evenly)? Do you think this is enough data to perform your analysis later on?
<br />
For the covid data we currently have around 750 data points (every day for 2020 and 2021). For the transportation data we currently have 366 data points (only for 2020) but we plan on getting the data for 2021 as well. By the end we plan on having around 750 data points for both datasets. We believe that this is more than enough data points and if we need more we can split our data up to even more specific data points, however, getting data by day makes the most sense for our goal.<br /><br />

### Are there missing values? Do these occur in fields that are important for your project's goals?
<br />
As far as we know there are no missing values in our data. This is because the data is very comprehensive from a reputable source which ensured that the data points were all filled in. Originally, in the transportation dataset, there were many missing values in the location fields, but we removed these columns for our averaged data and will not be using these in our analysis. <br /><br />

### Are there duplicates? Do these occur in fields that are important for your project's goals?
<br />
There should not be any duplicate records in the data. <br /><br />


### How is the data distributed? Is it uniform or skewed? Are there outliers? What are the min/max values? (focus on the fields that are most relevant to your project goals)
<br />
The data is distributed within reasonable ranges for each field. There are no outliers that stick out to us as unlikely to have actually occurred. The max average price for a rideshare on any given day is 20.16(2020-08-10). The min average price for a rideshare on any given day is 13.94(2020-03-14). The min for the total number of covid cases in a day is 0 (on multiple days) and the max is 10279 (2021-12-28).<br /><br />

### Are there any data type issues (e.g. words in fields that were supposed to be numeric)? Where are these coming from? (E.g. a bug in your scraper? User input?) How will you fix them?
<br />
We do not believe that there are any data type issues. This is because the dates are formatted the same way for every dataset and because all of our other data points are represented as floats.<br /><br />


### Do you need to throw any data away? What data? Why? Any reason this might affect the analyses you are able to run or the conclusions you are able to draw?
<br />

We did not need to throw any data points away. We did not include some attributes since they are not required for what we need. Thus, not having certain attributes will not affect our results. The data we were able to collect was very comprehensive and there was not a lack of data. All of our values were within a reasonable range (ie no outliers) which allowed us to hold onto all data points required.<br /><br />


### Summarize any challenges or observations you have made since collecting your data. Then, discuss your next steps and how your data collection has impacted the type of analysis you will perform. (approximately 3-5 sentences) <br />

The covid data was relatively straightforward and after obtaining and there were no issues. Our main problem with collecting data came from data scraping for ride share data. Due to the sheer number of data per day (roughly 195833 data points per day) we found it difficult to prevent our code from timing out. By setting a higher threshold for timing out we were able to mitigate this problem. The other issue with this dataset was the time it took to collect the data. It took roughly 10-15 minutes per month to collect the data. Given this, if we want to collect a larger sample of data we must be aware of the time it takes and keep that in mind when making any changes. On a more positive note, since we have access to such a comprehensive dataset we can more comfortably use the data since we know it is coming from a large sample size. 
