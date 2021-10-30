# <h1 align="center">academy_award_proj</h1>
# <h2 align="center">Exploratory Data Analysis and data scraping for the Academy Award winners and nominees for Best Picture</h2>

## Code and Resources Used:
* **Python Version:** 3.8
* **Jupiter Notebook:** 6.3
* **Web Scraping:** https://www.youtube.com/channel/UCq6XkhO5SZ66N04IcPbqNcw , http://www.omdbapi.com/ , https://www.youtube.com/channel/UCiT9RITQ9PW6BhXK0y2jaeg
* **Packages:**  BeautifulSoup, pandas, numpy, matplotlib, seaborn, json, pickle, nltk, wordcloud

## Web Scraping
**I am scraping data from wikipedia page using BeautifulSoup library, also I am using omdbapi.com for scraping some missing data.**
* title
* Directed by
* 'Written by',
* 'Produced by'
* 'Starring', 
* 'Cinematography',
* 'Edited by',
* 'Music by',
* 'Distributed by',
* 'Release date',
* 'Running time',
* 'Country', 
* 'Language',
* 'imdb', 
* 'metascore',
* 'rotten_tomatoes', 
* 'plot', 
* 'genre', 
* 'awards', 
* 'Screenplay by',
* 'Story by', 
* 'Based on', 
* 'Production company', 
* 'Budget', 
* 'Box office',
* 'Production companies', 
* 'Countries', 
* 'Languages', 
* 'Narrated by'


## Data Cleaning
After scraping the data, I needed to clean it up so that it was usable for eda. I made the following changes and created the following variables:
* Convert running time into an integer
* Clean up references [1]
* Convert dates into datetime object
* Split up the long strings
* Removing unnecessary columns for eda 
* Adding necessary columns for eda('month', 'year', 'rotten_tomatoes_norm', 'metascore_norm', 'won', 'sum_of_awards')
* Adding running time values to the movies that we were missing data
* Adding won values for the movies that we were missing data

## EDA(Exploratory Data Analysis)
*  Normalizing imdb, metascore, rotten_tomatoes columns to have RATINGS 0-10(imdb stays the same)
*  Top 10 winners, top 10 winners and nominees acording to IMDB
*  Combining IMDB and Rotten tomatoes top 10 score
*  Creating a scatterplot exploring the relationship between IMDB ratings and RT ratings.
*  Top 10 longest and shortest movies that won Academy Award for Best International Feature Film
*  Top 10 most successful films acording to awards and nominations they recieved
*  Creating a plot to compare Winners and nominees through the months
*  Creating countplot to visualize most common genres or combinations of genres in the dataset
*  Exploring the relationship between the Budget and the awards.
*  Exploring the relationship between the year in which movie is released and its awards
*  Exploring the relationship between the Budget and the Box office.
*  Exploring the relationship between the Budget and the Year the movie is Released.
*  How successful were the movies who won an Oscar comparing to the ones who didn't? Measuring the awards and nominations they recieved.
*  Comparing Distribution of Scores Across Sites
*  Checking the most common words used in the plot
*  Checking the most common words used in the plot in the last 30 years to compare with all time most common words 

### Final thoughts: By analysing this data we can see that Drama is by far most populat genre in the academy. We can notice that the Budget and Box office normally are highly correlated aslo the Budget for the movies is growing over the Years as we see previosly and which is kind of expected because of the inflation and the growth of the movie industry. Sum of the awards and the year that is also normal beacause nowadays have a lot more movie festivals than before. Interesting thing is that the stories did't change to much over time. Also I found interesting that the 12th month of the year (December) we have the most nominees and winners.
