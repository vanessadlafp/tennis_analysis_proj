# Men's Professional Tennis Tour (ATP) Analysis: Project Overview

Inquiry raised by Toni Nadal's (Rafael Nadal's uncle and former coach) [Ted Talk](https://www.ted.com/talks/toni_nadal_el_valor_del_esfuerzo) where he gives his standpoint on the impact that technology might have on the circuit, causing players to lose intuituon in the court and thus creating a huge gap between young and more experienced players, probably explaining why it's taking so much to the new ones to replace the old ones nowadays.
 
* Cluster analysis of 2011 and 2019 top 100 ATP ranking players to determine characteristics that magnify the gap between top players and the rest, and how they've changed over time. 

* Identified 4 clusters for the years 2011 and 2019. However, seniority and the dominance of the Big Three (Djokovic, Nadal and Federer) have seemed to create a more competitive game for the rest of the players, as they have had to increase their tournement participation and strengthen all aspects of their game to improve their chances of defeating the champions. 

* Scraped stats for performance of the top 100 players for the years 2011 and 2019 from the ATP tour website using Python and Beautiful Soup.

* Applied Principal component analysis (PCA) for dimensionality reduction, and hence an optimal feature selection for the K-Means algorithm.

## Code and Resources Used

Python Version: 3.7
Packages: pandas, numpy, sklearn,scipy, matplotlib, seaborn, BeautifulSoup.

## Web Scraping

Scraped stats for top 100 players of the ATP circuits for last ranking update of the years 2011 and 2019 (last year without COVID-related regulations and therefore the most recent year suitable for comparison). With each player, we got the following:

* Ranking
* Player
* Age
* Points
* Tourn Played
* Turned Pro
* Aces
* Double Faults
* 1st Serve %	
* 1st Serve Points Won %	
* 2nd Serve Points Won % 
* Break Points Faced
* Break Points Saved %
* Service Games Played
* Service Games Won %	
* Total Service Points Won %	
* 1st Serve Return Points Won %	
* 2nd Serve Return Points Won %	
* Break Points Opportunities	
* Break Points Converted %	
* Return Games Played	
* Return Games Won %	
* Return Points Won %	
* Total Points Won %

## Data Cleaning

Following changes were made and variables were created to be able to use the data for its analysis:
* Parsed numeric data out of effectivities (expressed in %).
* Removed empty columns that previously had graphic information.
* Transformed 'Turned Pro' date into the career lenght of each player.
* Removed columns with stats that behave similarly for all players or were already explained by other variables:
          - Age
          - 1st Serve %
          - 1st Serve Points Won %
          - 2nd Serve Points Won % 
          - Break Points Faced
          - Break Points Saved %
          - Service Games Won %
          - 1st Serve Return Points Won %
          - 2nd Serve Return Points Won % 

## Exploratory Data Analysis (EDA)

Examined the distributions of the data. Below are a few highlights found:

![](https://github.com/vanessadlafp/tennis_analysis_proj/blob/main/career_length_2011.png) | ![](https://github.com/vanessadlafp/tennis_analysis_proj/blob/main/career_length_2019.png)
-----------------------------------------------------------------------------------------------------------------------------------------|-------


<img src="https://github.com/vanessadlafp/tennis_analysis_proj/blob/main/corr_map_2011.png" width="450" height="450"> | <img src="https://github.com/vanessadlafp/tennis_analysis_proj/blob/main/corr_map_2019.png" width="450" height="450">
-----------------------------------------------------------------------------------------------------------------------------------------|-------

## Cluster Analysis
1) Hierarchical clustering: dendogram to have an idea of main clusters.
2) K_Means: to see main tendencies.
3) K_Means clustering with PCA: to better define clusters.


<img src="https://github.com/vanessadlafp/tennis_analysis_proj/blob/main/Cluters_by_PCA_components_2011.png  " width="450" height="450"> | <img src="https://github.com/vanessadlafp/tennis_analysis_proj/blob/main/Cluters_by_PCA_components_2019.png  " width="450" height="450">
-----------------------------------------------------------------------------------------------------------------------------------------|-------

* Component 1: High effectivity both serving and returning (most complete game)          
* Component 2: Aces                                                                                                                                  
