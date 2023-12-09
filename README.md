# Data Wrangling and Analyzing 
This is a Udacity nano degree project to wrangle and analyze data. The goal of the project is to analyze data from We Rate Dogs twitter account and identify which tweets are most likely to be retweeted and favorited.

# Software and Packages:
Jupyter Notebook  
Pandas  
Numpy  
Matplotlib  
Requests  
Tweepy
Json  
Timeit

# Data Wrangling Report

Three different sources of data from twitter feed of WeRateDogs is gathered and loaded into
pandas dataframes.  

**Gathering:** Twitter-archived-enhanced.csv was downloaded manually and loaded into a pandas dataframe. Image-predictions.tsv was downloaded programmatically and loaded into a
dataframe. For the Twitter API data, tweet-json.txt file is manually downloaded. Tweet-json.txt
required several operations before it could be loaded into a pandas dataframe.  

**Assessing:** Assessing of data was done both visually and programmatically on all the three
dataframes. Few quality issues and tidiness issues were identified in the data.  

**Cleaning:** Copies of original dataframes were made. All the quality issues and tidiness issues
identied in the assess stage were defined, coded, and tested. Image Predictions and Twitter JSON
API data were merged into the twitter archive table. It was later found that there was some
valuable information embededed in the source column of the twitter archive table, which was
extracted. All the other columns which are insignificant to analysis were dropped.


# Quality Issues
**Twitter Archive Table:**  

1.Not all tweets are original; few are retweets and replies  
2.Rating Numerator greater than denominator  
3.Timestamp is not a correct datatype  
4.Few records may be after August 1st, 2017  
5.Expanded urls are missing on few tweets  
6.No null values in names, but few dog names are none  
7.Ratings where the text has a decimal value has incorrect numerator value: 13.5/10 is captured as 5/10 (tweet_id = 883482846933004288)  
8.A text with date of 11/15/15 has been misinterpreted as rating of 11/15  
9.Change ratings_denominator to float to make it consistent with numerator  
10.timestamp column name shadows the built-in type timestamp  
11.Few original tweets are without images  

**Image Prediction Table:**  

1.Possible incompleteness in data. 2075 records (images) for a total of 2097 original tweets (not reply or retweets)  
2.Columns p1, p2, and p3 are in both lower and Upper case  


# Tidiness Issues  
1.Image predictions can be merged with twitter archive table as tweet IDs is common between the tables and no duplicate tweet IDs.  
2.Twitter api json table can be merged with twitter archive table as there are no duplicates tweet IDs.  
3.In Twitter_archive table, there are 4 different columns for each of the dog stage.

# Analysis Insights

<img width="672" alt="image" src="https://github.com/vamshi8719/Data-Wrangling/assets/56979563/4cca0860-7c1f-4232-a7ea-d9db8ace06c8">

<img width="619" alt="image" src="https://github.com/vamshi8719/Data-Wrangling/assets/56979563/a3fd8beb-8a90-451b-a36d-ebcc6dc85262">

<img width="596" alt="image" src="https://github.com/vamshi8719/Data-Wrangling/assets/56979563/532bbeb4-0945-45f7-850a-ea760fad82a2">

<img width="535" alt="image" src="https://github.com/vamshi8719/Data-Wrangling/assets/56979563/a1decc3b-8bba-4d73-b8ef-91c5428ae924">

<img width="547" alt="image" src="https://github.com/vamshi8719/Data-Wrangling/assets/56979563/1b0d4720-57be-4035-89c9-dbf01d5c264e">


