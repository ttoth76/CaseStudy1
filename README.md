# Aundrae Allison, Tamas Toth - SMU Case study brewery analysis

## MSDS 6306: Doing Data Science

Description

The Beers data set contains a list of 2410 US craft beers and Breweries
data set contains 558 US breweries. The data sets descriptions are as
follows.

**Beers.csv:**

-   Name: Name of the beer.
-   Beer_ID: Unique identifier of the beer.
-   ABV: Alcohol by volume of the beer.
-   IBU: International Bitterness Units of the beer.
-   Brewery_ID: Brewery id associated with the beer.
-   Style: Style of the beer.
-   Ounces: Ounces of beer.

**Breweries.csv:**

-   Brew_ID: Unique identifier of the brewery.
-   Name: Name of the brewery.
-   City: City where the brewery is located.
-   State: U.S. State where the brewery is located.

**beer_consumption_by_state_2021.csv**

-  full: The full name of a state
-  consumption: beer consumption
-  unit: beer consumption unit

**fav_beer_state.csv**

-  full: The full name of a state
-  fav_beer: The name of the favorite beer for the state


#### Intention is to answer key business questions through Exploratory Data Analysis and Machine Learning Modeling to help Budweiser to drive potential business opportunities in the United States. The Analysis is focusing on beers and breweries as well as relationship to consumers.


__Analysis Questions:__

1.  How many breweries are present in each state?

2.  Merge beer data with the breweries data. Print the first 6
    observations and the last six observations to check the merged file.
    (RMD only, this does not need to be included in the presentation or
    the deck.)

3.  Address the missing values in each column.

4.  Compute the median alcohol content and international bitterness unit
    for each state. Plot a bar chart to compare.

5.  Which state has the maximum alcoholic (ABV) beer? Which state has
    the most bitter (IBU) beer?

6.  Comment on the summary statistics and distribution of the ABV
    variable.

7.  Is there an apparent relationship between the bitterness of the beer
    and its alcoholic content? Draw a scatter plot. Make your best
    judgment of a relationship and EXPLAIN your answer.

8.  Budweiser would also like to investigate the difference with respect
    to IBU and ABV between IPAs (India Pale Ales) and other types of Ale
    (any beer with “Ale” in its name other than IPA). You decide to use
    KNN classification to investigate this relationship. Provide
    statistical evidence one way or the other. You can of course assume
    your audience is comfortable with percentages … KNN is very easy to
    understand conceptually.

In addition, while you have decided to use KNN to investigate this
relationship (KNN is required) you may also feel free to supplement your
response to this question with any other methods or techniques you have
learned. Creativity and alternative solutions are always encouraged.

1.  Knock their socks off! Find one other useful inference from the data
    that you feel Budweiser may be able to find value in. You must
    convince them why it is important and back up your conviction with
    appropriate statistical evidence.


2.  Codebook, Both CSV files and a ReadMe.md The Readme file describes
    the purpose of the project and codebook. The repo can be structured
    however you like, but it should make sense and be easily navigated.

#### __Summary__
##### - Used 4 data sets for the analysis. 
#####   * Beers
#####   * Breweries
#####   * Beer Consumption by State per Capita (2021)
#####   * The most popular beer in every US state (2021)

##### - Identified missing values in ABV and IBU as well as empty string in Style variables.
##### - Budweiser have 558 breweries in the United States. The top five states with the highest number of breweries are:
##### 1. CO - 47
##### 2. CA - 39
##### 3. MI - 32
##### 4. OR - 29
##### 5. TX - 28
##### -ND, NH and MT are the states with the highest amount of beer consumption per capita per state. Contrary to this, Budweiser have very low number of breweries in these states. 
##### -The total number of unique style beers produced by Budweiser is 100.
##### -Number of unique style beers produced in Colorado: 61
##### -Colorado is producting 61% of the total beer styles Budweiser has in its portfolio.
##### -Median ABV values by state are uniformly distributed and ranging between 4% and 6%.
##### -Median IBU values by state are uniformly distributed and ranging between 22 and 57.5.
##### -Colorado is producing the highest alcohol content beer with 12.8%. This beer is produced in Upslope Brewing Company and it is a Belgian Style Ale.
##### -Oregon is producing the most bitter beer with 138 IBU value. This beer is produced in Astoria Brewing Company and it is a Bitter Bitch Imperial IPA.
##### 1. The products alcohol content is ranging between 0.001 and 0.128
##### 2. 25% of the products alcohol content is less than or equal to 0.05
##### 3. 50% of the products alcohol content is above and below of 0.056
##### 4. 75% of the products alcohol content is less than or equal to 0.067
##### 5. Average alcohol content of the products is 0.059
##### 6. Product portfolio is mostly comprised of mild alcohol content beers
##### 7. There is no reason to believe that the ABV data set is not coming from a normal distribution.
##### -There is a positive linear relationship between ABV and IBU. The beer alcohol content increase is associated with the bitterness. ~26% of the variance in IBU can be explained by changes in ABV.
##### -Built a KNN model to investigate the difference with respect to IBU and ABV between IPAs and Ales.
##### -The KNN model predicted the beer style classes with ~80% accuracy and 8.3% misclassification rate.
##### -This KNN model generalizes well on this data set and we can conclude that ABV and IBU are good verables predicting the sytle of the beers.
##### -The model predicts ALEs with IBU above 95 and ABV above 0.06 as IPA. It seems like that a more bitter and stringer beer would represent IPA rather than ALE for the model. IPAs are predicted more consistantly however some of the lower alcohol content and lower IBU IPAs are predicted as ALEs.
##### -Built a Naive Bayes model for the prediction but the model performance was not as good as the KNN one therefore I did not pursue this model further.
##### -Budweiser is the most popular beer in 23 states. 

#### __Recommendations__
##### 1. There is an opportunity to increse data quality for the ABV and IBU variables.
##### 2. I recommend Budweiser to carry out a market analysis in ND, NH, and MT to better understand potential market opportunities to increase sales given the high amount of beer consumption in these states.
##### 3. Study the beer styles to see if there is a need to reclassify some of the beers from IPA to Ale and vice versa based on ABV and IBU values. This could better represent product quality and beer taste which in return could result in more customers. 
##### 4. I can see opportunities for Budweiser to further increase their presence in those states where their beer is the most popular by increasing the number of breweries. Budweiser has very low number of breweries in these states however consumption is the highest and Budweiser is the most popular beer: MT, SD, NH, WV, IA and SC. Further to the potential increase in sales in these states the supply chain cost may be reduced as well by local distributions.
