# ETL_Twitter
Exploring the ETL Process through Twitter Scraping

## Overview
A script that downloads tweets data on a specific search topic using the standard search API. 

*Resources used:*
- **Twitter API**
- **Jupyter noteboook**
- **Python 3.7**
- **Tweepy**
- **Pandas**
- **Pymongo**
- **MongoDB atlas**


## Detailed steps

The script contains the following functions: 

* scape_tweets() - The tweets extracted have the following parameters:<br>
      * Search topic
      * The number of tweets to download per request
      * The number of requests
And returns a dataframe.

* Save_results_as_csv() - This function has the following parameters:
      * the dataframe from the scrape_tweets function
And returns a csv file with the following naming format:<br>
    * tweets_downloaded_yymmdd_hhmmss.csv (where ‘yymmdd_hhmmss’ is the current 	timestamp)<br>


The following attributes of the tweets would be extracted:<br>
   * Tweet text
   * Tweet id
   * Source
   * Coordinates
   * Retweet count
   * Likes count
   * User info
   * Username
        *Screenname
        *Location
        *Friends count
        *Verification status
        *Description
        *Followers count


The second part creates a MongoDB atlas database called Tweets_db and stores the extracted tweets into a 	collection named: raw_tweets.
