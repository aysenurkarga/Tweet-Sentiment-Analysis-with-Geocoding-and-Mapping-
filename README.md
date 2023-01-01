# Tweet-Sentiment-Analysis-with-Geocoding-and-Mapping-
***#Introduction***

This script utilizes the tweepy library to access Twitter's API and retrieve tweets based on a user-specified location, start date, and end date. The tweets are then processed and analyzed to provide insight on the following:

***# Top trending topics***

Word cloud visualization of the tweets
Overall sentiment of the tweets (positive, neutral, or negative)
Geolocation of the tweets (if available)
The script also allows the user to input a Twitter user ID and retrieve information about the user, including their gender and age (if available).

***# Dependencies***

Before running this script, you will need to install the following dependencies:

**tweepy**: pip install tweepy

**pandas**: pip install pandas

**textblob**: pip install textblob

**folium**: pip install folium

**seaborn**: pip install seaborn

**wordcloud**: pip install wordcloud


***# The necessary libraries are imported:***

**tweepy** is used to access the Twitter API.

**pandas** is used to store and manipulate the data from the tweets.

**textblob** is used to perform sentiment analysis on the tweets.

**folium** is used to create a map visualization of the tweets.

**seaborn** is used for data visualization.

**WordCloud** is used to create a word cloud visualization of the tweets.

The Twitter API is authenticated using the provided ***consumer_key***, ***consumer_secret***, ***access_token***, and ***access_token_secret***. These values should be replaced with your own API keys and secrets, which you can obtain by creating a developer account on the Twitter Developer website.

The code prompts the user for a location, start date, and end date to search for tweets. These values are used to call the ***api.search_tweets()*** function, which searches for tweets matching the given criteria.

The tweets are stored in a pandas DataFrame and the top 5 trending topics are printed. This is done by lowercasing all the tweets, splitting them into individual words, and counting the frequency of each word. The top 5 most common words are then printed.

A word cloud visualization of the tweets is created and displayed. This is done by joining all the tweets into a single string and passing it to the ***WordCloud*** object. The resulting image is then displayed using ***matplotlib***.

The overall sentiment of the tweets is calculated using ***TextBlob*** and printed. This is done by iterating through each tweet, performing sentiment analysis on it using TextBlob, and adding the resulting polarity value to a running total. At the end, the code checks the value of the total polarity and prints a message based on whether it is positive, neutral, or negative.

If the DataFrame contains ***coordinates*** data, a map is created using ***folium*** with markers and a heatmap of the tweet locations. The map is then saved and opened in a new tab. If the coordinates data is not available, an error message is printed.

Finally, the code prompts the user for a user ID and retrieves the user's data from the Twitter API. The user's gender and age are then printed.


***# Setup***

Before running the script, you will need to obtain a set of Twitter API keys. These keys can be obtained by creating a Twitter developer account and creating a new "app" under the "Apps" tab. Once you have created an app, click on the app to view the "Details" page and scroll down to the "Keys and Tokens" section to find your consumer_key, consumer_secret, access_token, and access_token_secret.

***# Running the script***

To run the script, open a terminal window and navigate to the directory where the script is saved. Then type the following command:

python twitter_analyzer.py

The script will prompt you to enter a location, start date, and end date. You can enter a city, country, or region for the location. The start and end dates should be entered in the format YYYY-MM-DD.

Once you have entered this information, the script will retrieve tweets from the specified location and date range and perform the following actions:

**1)** Print the top 5 trending topics found in the tweets.

**2)** Generate and display a word cloud visualization of the tweets.

**3)** Determine the overall sentiment of the tweets (positive, neutral, or negative) and print the result.

**4)** If geolocation data is available for the tweets, generate a map visualization showing the locations of the tweets. The map will also display a heatmap of the tweet locations.

**5)** After these actions have been completed, the script will prompt you to enter a Twitter user ID. You can enter the user ID of any public Twitter user (e.g. "1234567890"). If the user has provided their gender and age in their Twitter profile, the script will print this information.


