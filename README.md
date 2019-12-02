
# API Practice - Paired Lab

## Introduction

For some further practice with APIs (and with SQL!), we're going to work on a single big lab to apply what we've learned in Module 1!

![](https://media.tenor.com/images/faa7904870d4661b3f077f1c49fbbb46/tenor.gif)

## The Goal

Start by examining the data dictionary for the SQL database we'll be working with, which comes from this [kaggle page](https://www.kaggle.com/laudanum/footballdelphi). Familiarize yourself with the tables it contains, and what each column means. We'll be using this database to get data on each soccer team and calculate some summary statistics. 

Unlike previous labs, this lab is more open-ended. At minimum, you'll need to:

* Query the SQL database
* Calculate summary statistics
* Get the weather data from the DarkSky API

Upon completion of this lab, you should be able to see/access the following information:

* The name of the team
* The total number of goals scored by the team during the 2011 season
* The total number of wins the team earned during the 2011 season
* The team's win percentage on days where it was raining (in Berlin) during games in the 2011 season. 

![](https://media.giphy.com/media/4TkcwHdT1LSLw2rrEN/giphy.gif)

## The Data

You'll find a database containing information about soccer teams and the matches they've played in the file `database.sqlite`. 

### Getting the Weather Data

You'll need to figure out if it was raining or not during the game. The database itself does not contain this information, but it does contain the date on which the game was played. For this, you'll need to use the [DarkSky API](https://darksky.net/dev) to get the historical weather data for that day. 

Note that each game is played in a different location, and this information is not contained in our SQL database. However, the teams in this database are largely German, so go ahead and just use the weather in Berlin, Germany as a proxy for this information. If it was raining in Berlin on the day the game was played, count that as rain game-- **_you do not need to try and figure out the actual weather at each game's location, because we don't have that information!_**

#### NOTE: The DarkSky API is limited to 1000 free API calls a day, so be sure to test your model on very small samples. Otherwise, you'll hit the rate limit!

### Some Advice

![](https://media2.giphy.com/media/11F0d3IVhQbreE/giphy.gif)

This is a paired afternoon lab, meant to take just one afternoon. You may run out of time, and that's okay! But do make sure to comment your code *while you're writing it* in case you don't have time today and want to go back later.

ALSO: It's okay to use external tools to make your life easier -- that's what they're for! Using tools like the [DB Browser for SQLite](https://sqlitebrowser.org/) to visualize and interact with your SQL database, or [Postman](https://www.getpostman.com/) to test your API query, is one aspect of working smarter (not harder)! 
