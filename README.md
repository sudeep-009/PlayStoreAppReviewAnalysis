# Introduction
There is famous phrase which tell us that Data is the new oil of 21st century.Business growth involves garnering as many customers as you can. This requires knowing exactly what customers desire and what channels they use to find products and services.In today cut-throat competation taking business decision based on gut-feel could have negative impact. Therefore utilizing the potential of value store beneath the mountain of data would be very effective.
In the PlayStore App data analysis we generally tried to find some of the actionalble insight that would help our app developers to develop an app that would have huge customer base based on their previous experience. Digging out the value from data which would help the app making business to grow at huge volume is the main objective of this data analysis


## Exploratory Data Analysis:
Before starting we should first understand what actually Exploratory Data Analysis is ? Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns,to spot anomalies,to test hypothesis and to check assumptions with the help of summary statistics and graphical representations.It is a good practice to understand the data first and try to gather as many insights from it. EDA is all about making sense of data in hand,before getting them dirty with it. As we have understand what EDA actually is lets start our fun journey of playing around with the dataset.

## Data Collection: 
In this we have used two dataset:
1) App dataset which contains information about the rating, category, size and more.
2) User Review Dataset which contains information about user review.

App dataset contains the following features:

           1) App: Name of the App.
           2) App Category: Category of the app. Like Games, Fitness etc
           3) Rating: Rating of the app out of in scale of 1 to 5.
           4) Reviews: Number of reviews each app received.
           5) Size: The memory size needed to install the application.
           6) Installs: No. of install of particular app
           7) Type: Whether the app is free or a paid app.
           8) Price: The price of the app.
           9) Content Rating: This feature tell us about the intended audience for the app like teens, everyone etc .
           10)Genres: The sub-category for each app.
           11)Last Updated: date of the most recent update for the app.
           12)Current Ver: The app's current version.
           13)Android Ver: The oldest version of Android OS supported by the app.
           
UserReview Dataset contains the following features:

           1) App - It tells us about the name of the application.
           2) Translated_Review - It tells us about what the users feedback is about the application.
           3) Sentiment - It tells us about a view or opinion of the user w.r.t. the application.
           4) Sentiment_Polarity- Sentiment polarity for an element defines the orientation of the expressed sentiment, 
              i.e., it determines if the text expresses the positive, negative or neutral sentiment of the user about the application.
           5) Sentiment_Subjectivity - It refers to the text that contains text which is usually expressed by a human having typical moods, 
              emotions, and feelings. Mostly it is a public opinion and not a factual information.
              
 ## Problem Statement:
 Explore and analyze the data to discover key factors responsible for app engagement and success.
 
 Based on the features we came across the following Problem Statement
 
                  Q1.Which category have most number of Apps?
                  Q2.Categories with least number of Apps but Having High Rating and Installations?
                  Q3.Which Content Rating is preferred most?
                  Q4.Which Genres have most numbers of apps?
                  Q5.What is the average Ratings for Apps available? 
                  Q6.What is the effect of price on Ratings?
                  Q7.Is Rating is proportional to Reviews or Installation?
                  Q8.What Percentage of Apps are paid ?
                  Q9.What is the Ratio of free and paid apps in different categories?
                  Q10. Which are the most expensive Apps and their category?
                  Q11.Do people prefer to pay to for apps and which category have most paid apps?
                  Q12.Which categories have bulky apps and how people Rate them?
                  Q13.Paid Apps:-the Ratings & what are the sentiment of users towards them?
                  Q15.What are the user sentiments toward different categories?
                  Q14.Does frequent updates help in improving Ratings and User Base?

## Understanding Data:
                 Aap Dataset
                 a) Number of records present in the app dataset were 10841.
                 b) Number of features present in the dataset were 13.
                 c) All the attribute of the dataset is of object type except rating.
                 d) Duplicate Values present in the dataset were  1170.

                Review Dataset
                a) Number of records present in the app dataset were 64251.
                b) Number of features present in the dataset were 5.
                c) All the attribute of the dataset is of object type except sentiment polarity and sentiment objectivity.
                d) Duplicate Values present in the dataset were 0.



## Cleaning Data and Feature Engineering:
                 a) Handling Missing Values: 
                 
                (i)  Dropped all missing value present in the rating column.
                (ii) Other features were filled with their mode.
                
                b) Duplicate Values:
                
                All the duplicate values were dropped.
                
                c) Outlier Detection:
                
                (i) One significant outlier was found in the rating column with value 19 using boxplot which was removed.
                
                d) Transforming Features:
                
                Following features have been transformed
                (a) Review - Transformed from object to int datatype.
                (b) Installs - Removed the trailing + sign, commas present, and finally transformed into int datatype.
                (c) Price - Removed the dollar sign and convert it into float datatype.
                (d) Size - Removed commas, M, replaced string value into numpy nan, brought consistency by converting kb in mb, and
                    finally converted into float datatype.
                (e) Last Updated: Converted it into pandas datetime object.
                
 ## Exploratory Data Analysis
                Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
                 a) Bar Plot.
                 c) Histogram.
                 b) Stacked Bar Plot.
                 d) Pie Chart.
                 f) Pair Plot.
                 g) Box Plot.
                 
                (I) Univariate Analysis:
                      a) Price: Most of the apps were found free.
                      b) Rating: Most of the apps were found to have average rating of 4.
                      c) Most of the apps were lightweighted.
                      d) Size: Bulky apps mostly belongs to two category:
                               (i) Family.
                               (ii) Game.
                      e) Price: Most of the paid apps were found to be cost less than 3 dollar.
                      f) Category: Most of the apps were found to be in the category of Family.
                      g) Sentiment: Most of the apps were found to have positive sentiment.
                      
                 (II) Bivariate Analysis:
                      a) Size Vs Rating: Despite being bulky some apps were found to very popular among users.
                      b) Price Vs Category: Most of the paid apps were found to be in  category of Family, Game, Medical, 
                                            Tools, Personalization.
                      c) Price Vs Category: Found that users could pay high amount for apps developed in the category of Lifestyle or Finance.
                      d) Price Vs Size: Most of the paid app apps were found to be made lighter by weight so as to garner specific user community.
                      e) Category Vs Rating: Most of highly rated apps were found to be in the category of Family, Game, Tools.
                      f) Price Vs Rating: Found that as the price of the apps increases the rating decreases even below the Average Rating.
                      g) Sentiment Vs Price: Found that users are more harsher towards free apps than free apps.
                      h) Last Update Vs Years: After 2017 apps were getting frequently updated.
                      i) Last Update Vs Rating: Found that frequently updated apps have more chances of being rated well.
                      
                      
                      
  ## Conclusion: 
               In the project we took lots of time to explore the data and then perform operations on it. Here is what we concluded from our datasets.
               
                     i) Most of the apps are free so developers should focus on creating free apps to have a huge customer base.
                     ii) If developing paid apps then apps size should not be greater than 40mb.
                     iii) More Apps should be in the category like Events,Beauty,Parenting as they have not been explored much but 
                          still quite popular with huge installations.
                     iv) In order to retain the customer base apps should be updated regularly
                      v) Developers should develop apps such that their content is available for everyone.
                     vi) Bulky apps should be developed in the category like Game, Family.
                     v)  If developing paid apps then its price should not be high and size should be less than 20mb.
                     vi) Apps belonging to Game and Family Category have high negative reviews therefore they should be developed carefully. 
                     
               Like this there can be alot of conclusions but we have tried to cover the most important ones.
               
               
  ## Challenges Faced: 
                    i)  Most of the data were in string type which should be in int or in float type in general. 
                    ii) There were few special characters like “+”,”$” “M” ”k” which were replaced and removed out 
                        with special operation on them.
                    iii)Some nulls which we generated during our data manipulation which were get dropped using simple 
                        operation and logic.
                    iv) We have faced lots of duplicates which we dropped which could have really messed up our exploratory part.
                    v)  It was difficult for us to choose between which tool we should use for data visualization. We preferred the most 
                        challenging one “seaborn” worked upon it implemented it in our code and even helped each in understanding the codes 
                        and operations like an ideal team should do.
                      
                      
                
                
                

              
              
              
              



