# BEER_CHALLENGE_DATA_SCIENCE
ANALYSIS OF REVIEW OF DATA WITH REVIEWS FOR DIFFERENT BEERS

## This file explains the Assumptions Made wherever applicable and the Observations/Results Obtained for 6 major questions along with minor findings.

## Along with the Exploratory Analysis nad Pre-processing of the Dataset, this project attempts to answer the following major questions based on facts gathered from the analysis.

# PLOTS Used to Support the Below Statements are included in another section and in notebook code (.ipynb file) showing the observations gathered.



1.	Rank top 3 Breweries which produce the strongest beers?

As can be noticed from the below result obtained in the code, the 3 prominent brewers with strongest beers are brewers with Brewer_Id : [6513 , 35, 2958] ranked in the order of the strength of  strongest beers produced by them.


TOP 3 Brewers with the Strongest Beers:

  beer_ABV  beer_beerId  beer_brewerId
     57.7        73368           6513
     27.0        25759             35
     19.5        58656           2958




2.	Which year did beers enjoy the highest ratings? 

    YEAR WITH HIGHEST RATINGS FOR BEERS IS: 2011. Reviews are classified into High and Low ratings after being carefully averaged into one average review column.
    Pivot Table and Pandas Groupby Functionalities are used to plot and identify the Year with Highest Ratings(magnitude wise).



3.	 Based on the user’s ratings which factors are important among taste, aroma, appearance, and palette?


  CORRELATIONS Obtained were analyzed closely to identify the Statistical Significance and the multicollinearity factor involved to identify the most relevant/important column.
Based on Statistically Significant (99%-alpha) Correlation Metrics amongst the Reviews, it is concluded that “REVIEW AROMA” is the most important review with it affecting/correlated with most of the other columns too and thus having the power to represent the combined effect of all reviews to a greater strength.



4.	If you were to recommend 3 beers to your friends based on this data which ones will you recommend?

Aggregating the Top 3 Beer Ids Satisfying the Thresholds for ABV & Taste Reviews (80th Percentile Cutoff)
Amongst these aggregations, BEERS having most reviews as compared to others satisfying thresholds(to add credibility) were chosen.



Beers with the following beerid are recommended by me.

[645 , 19960 , 3833]



5.	Which Beer style seems to be the favorite based on reviews written by users? 

Based on Polarities of Reviews Written by Users, the most favorite beer is QUADRUPEL(QUAD). 
Used Vader Lexicon Based Sentiment Analysis to identify polarity measure and find normalized polarity scores for each beer style.



6.	How does written review compare to overall review score for the beer styles?

It closely resembles the overall_review score since there is a closeness and similarity in the favourite beer style classification by analyzing both the columns via separate methods.

MORE TO BE CHECKED:
More resemblance could be verified based on the T-SNE CLASSIFICATION OF CLUSTERS based on Averaged WORD2VEC embeddings for text reviews.
 Hypothesis: If the clusters in TSNE VISUALIZATION are equal to the segregation of ratings and are well defined, then the reviews written are similar in nature to the review stars given.
