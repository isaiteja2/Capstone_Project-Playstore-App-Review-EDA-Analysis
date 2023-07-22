# Capstone_Project-Playstore-App-Review-EDA-Analysis
## Verified Project: [Credentials](https://certificates.almabetter.com/en/verify/72318421398252)
## Project Type - EDA(Exploratory Data Analysis)
## Contribution - Team
## Team Member 1 - Vadlamani Shivani
## Team Member 2 - Saiteja Ch
## Project summary
The Google Play Store and formerly the Android Market, is a digital distribution service operated and developed by Google. It serves as the official app store for certified devices running on the Android operating system and its derivatives, as well as ChromeOS, allowing users to browse and download applications developed with the Android software development kit (SDK) and published through Google. Google Play has also served as a digital media store, offering games, music, books, movies, and television programs.

We were given with two datasets i.e., Play Store & User Reviews. Let's take a look at the data, which consists of two files:

1. playstore data.csv: contains all the details of the applications on Google Play. There are 13 features that describe a given app.
1. user reviews.csv: contains 100 reviews for each app, most helpful first. The text in each review has been pre-processed and attributed with three new features: Sentiment (Positive, Negative or Neutral), Sentiment Polarity and Sentiment Subjectivity.

Before jumping into the data's provided, let me first explain you about the EDA analysis.

EDA involves generating summary statistics for numerical data in the dataset and creating various graphical representations to understand the data better and make it more attractive and appealing.

The following are the various steps involved in the EDA process:

1. Problem Statement - We shall brainstorm and understand the given data set. We shall study the attributes present in it and try to do a philosophical analysis about their meaning and importance for this problem.
2. Hypothesis - Upon studying the attributes present in the data base, we shall develop some basic hypothesis on which we can work and play with the data to look for the varied results which we can get out of it.
3. Univariate Analysis - It is the simplest form of analyzing the data. In this we would initially pick up a single attribute and study it in and out. It doesn't deal with any sort of co-relation and it's major purpose is to describe. It takes data, summarizes that data and finds patterns in the data.
4. Bivariate Analysis - This analysis is related to cause and the relationship between the two attributes. We will try to understand the dependency of attributes on each other.
5. Multivariate Analysis - This is done when more than two variables have to be analyzed simultaneously.
6. Data Cleaning - We shall clean the dataset and handle the missing data, outliers and categorical variables.
7. Testing Hypothesis - We shall check if our data meets the assumptions required by most of the multivariate techniques.

## GitHub Link -
Vadlamani Shivani -- https://github.com/shivanivadlamani/Play_store-App-Review-EDA-analysis.git

Saiteja Ch -- https://github.com/isaiteja2/Capstone_Project-Playstore-App-Review-EDA-Analysis.git

## Problem statement
1. What are the top categories on Play Store?
2. Are majority of the apps Paid or Free?
3. How importance is the rating of the application?
4. Which categories from the audience should the app be based on?
5. Which category has the most no. of installations?
6. How does the count of apps varies by Genres?
7. How does the last update has an effect on the rating?
8. How are ratings affected when the app is a paid one?
9. How are reviews and ratings co-related?
10. Lets us discuss the sentiment subjectivity.
11. Is subjectivity and polarity proportional to each other?
12. What is the percentage of review sentiments?
13. How is sentiment polarity varying for paid and free apps?
14. How Content Rating affect over the App?

### Q)Define your business objective?
The Play Store apps data has enormous potential to drive app-making businesses to success. Actionable insights can be drawn for developers to work on and capture the Android market. Each app (row) has values for category, rating, size, and more. Another dataset contains customer reviews of the android apps. Explore and analyse the data to discover key factors responsible for app engagement and success.

## General guidlines
1.   Well-structured, formatted, and commented code is required. 
2.   Exception Handling, Production Grade Code & Deployment Ready Code will be a plus. Those students will be awarded some additional credits. 
     
     The additional credits will have advantages over other students during Star Student selection.
       
             [ Note: - Deployment Ready Code is defined as, the whole .ipynb notebook should be executable in one go
                       without a single error logged. ]

3.   Each and every logic should have proper comments.
4. You may add as many number of charts you want. Make Sure for each and every chart the following format should be answered.
        

```
# Chart visualization code
```
            

*   Why did you pick the specific chart?
*   What is/are the insight(s) found from the chart?
* Will the gained insights help creating a positive business impact? 
Are there any insights that lead to negative growth? Justify with specific reason.

5. You have to create at least 20 logical & meaningful charts having important insights.


[ Hints : - Do the Vizualization in  a structured way while following "UBM" Rule. 

U - Univariate Analysis,

B - Bivariate Analysis (Numerical - Categorical, Numerical - Numerical, Categorical - Categorical)

M - Multivariate Analysis
 ]

## Dataset information

### Q)What do you know about the dataset
The PlayStore dataframe has a shape of (10841, 13), which means it has '10841' rows and '13' columns. The UserReview dataframe has a shape of (64295, 5), which means it has '64295' rows and '5' columns.

There are several null values present in both dataframes. In the PlayStore dataframe, there are '1474' null values in the Rating column, '1' null value in the Type column, '1' null value in the Content Rating column, '8' null values in the Current Ver column, and '3' null values in the Android Ver column. There are also '483' duplicate rows in this dataframe.

In the UserReview dataframe, there are '26868' null values in the Translated_Review column, '26863' null values in the Sentiment column, '26863' null values in the Sentiment_Polarity column, and '26863' null values in the Sentiment_Subjectivity column. There are also '33616' duplicate rows in this dataframe.
## Variable description
### Play store variables
1.**App** - It tells us about the name of the application.

2.**Category** - It tells us about the category to which an application belongs.

3.**Rating** - It tells us about the ratings given by the users for a specific application.

4.**Reviews** - It tells us about the total number of users who have given a review for the application.

5.**Size** - It tells us about the size being occupied the application on the mobile phone.

6.**Installs** - It tells us about the total number of installs/downloads for an application.

7.**Type** - It tells us whether the application is free or a paid one.

8.**Price** - It tells us about the price of the application.

9.**Content_Rating** - It tells us about the target audience for the application.

10.**Genres** - It tells us about the various other categories to which an application can belong.

11.**Last_Updated** - It tells us about the when the application was updated.

12.**Current_Ver** - It tells us about the current version of the application.

13.**Android_Ver** - It tells us about the android version which can support the application on its platform.Answer Here
## Data cleaning
### User Review variable
1. **App** - It contains the name or identifier of the app.
2. **Translated_Review** - It contains the text of the review
3. **Sentiment** - It contains the overall sentiment of the review (e.g. positive or negative)
4. **Sentiment_Polarity** - Itcontains a measure of the positivity or negativity of the review
5. **Sentiment_Subjectivity** - It contains a measure of the subjectivity or objectivity of the review. These columns could be useful for analyzing the sentiment of app reviews and understanding how users feel about different apps.

## Exploring all the NaN values
### Null/Nan/empty values in Play store
The number of null values are:

1.Rating has 1474 null values which contributes 13.60% of the data.

2.Type has 1 null value which contributes 0.01% of the data.

3.Content_Rating has 1 null value which contributes 0.01% of the data.

4.Current_Ver has 8 null values which contributes 0.07% of the data.

5.Android_Ver has 3 null values which contributes 0.03% of the data.

### Null/Nan/empty values in User review
The number of null values are:

1.Translated_Review has 26868 null values which contributes 41.79% of the data.

2.Sentiment has 26863 null values which contributes 41.78% of the data.

3.Sentiment_Polarity has 26863 null values which contributes 41.78% of the data.

4.Sentiment_Subjectivity has 26863 null values which contributes 41.78% of the data.

## Manipulations and insights found
● Our major challenge was data cleaning.
13.60% of reviews were NaN values, and even after merging both the dataframes.

● Many rows and columns anve insufficient data, so we have to drop them as well.

● Free apps are more preferred.

● Because of the null and NaN values the analysis was not so accurate

● Cleaning the unwanted charactors and converting the required column values into valid numeric type for easy analysis

## Solutions to business objectives
### **What do you suggest the client to acheive buisness objective:**
In this project we analysed play store based on the data provided. The analysis done on given parameters would help client to enhance the properties of apps while launching , Most importantly provide a common ground to work on apps of different categories which need common updation.
Initially me and my teammate focused more on cleaning and preparing the data for easy analysis that would help us get clear insights of playstore apps.
After the analysis and plotting and working with data we would summarize our analysis to provide better and best results out of our work:


1.   Focusing on more updated and useful free apps becausee they are the most commonly used
2.  Regular updatation of existing apps, to attract more new users.
3.  There are some unexplored categories like event, beauty , art etc. Developing apps in these categories would be helpful foor users who have intrest in these areas.
4.  Providing good content in apps that would be a factor in increasing the app market.
5. Users are more likely to have varying sentiments while using the app in each phase. So keeping the features that would be in favour of the majority of users is a factor that should have the focus.

## Conclution:
Through exploratory data analysis we have observed some trends and have made some assumptions that might lead to app success among the users in the play store.

•	Percentage of free apps is ~92%

•	Percentage of apps with no age restrictions is ~82%

•	Most competitive category in paid and free: Family and Games

•	Family, Game and Tools are top three categories having 1906, 926 and 829 app count.

•	Apps having size less than 50 MB are 8783. 7749 Apps are having rating more than 4.0 including both type of apps.

•	Category with the highest average app installs: Game

•	Percentage of apps that are top rated is ~80%

•	There are 20 free apps that have been installed over a billion time

•	Category in which the paid apps have the highest average installation fee: Finance

•	The median size of all apps in the play store is 12 MB.

•	The apps whose size varies with device has the highest number average app installs.

•	The apps whose size is greater than 90 MB has the highest number of average user reviews, ie, they are more popular than the rest. 

•	Overall sentiment count of merged dataset in which Positive sentiment count is 64%, Negative 22% and Neutral 13%.

•	Sentiment Polarity is not highly correlated with Sentiment Subjectivity
