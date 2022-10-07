# Metis_NLP_Unsupervised

## Analyze reviews of Bumble application on Google Play Store

### Abstract
The goal of this project is to do topic modeling using K-Means and NMF ( Non Negative Matrix Factorization ). Bumble is a dating application. Profiles of potential matches are displayed to users, who can "swipe left" to reject a candidate or "swipe right" to indicate interest. In heterosexual matches, only female users can make the first contact with matched male users, while in same-sex matches either person can send a message first. The app is a product of Bumble Inc.
Users can sign up using their phone number or Facebook profile, and have options of searching for romantic matches or, in "BFF mode", friends. Bumble Bizz facilitates business communications. Bumble was founded by Whitney Wolfe Herd shortly after she left Tinder, a dating app she says she co-founded, due to growing tensions with other company executives. Wolfe Herd has described Bumble as a "feminist dating app". As of January 2021, with a monthly user base of 42 million, Bumble is the second-most popular dating app in the U.S. after Tinder. According to a June 2016 survey, 46.2% of its users are female. According to Forbes, by 2017 the company was valued at more than $1 billion, and the company reports having over 55 million users in 150 countries as of 2019. [Source: Wikipedia]

### Design
The data for this project was obtained from Kaggle - https://www.kaggle.com/datasets/shivkumarganesh/bumble-dating-app-google-play-store-review/code. The reviews data was transformed into a matrix which represents the weights of each word. This matrix is used to train a model with 5 clusters using K-Means algorithm and NMF. The number of clusters was decided using the popular elbow method. The model was also trained using NMF ( Non Negative Matrix Factorization ). The topics were decided depending on the most used words in each cluster. Also, the percentage of each cluster was calculated. Sentiment score was calculated using VaderSentiment, which gives the best and worst review.
The models were also trained using Gaussian NaïveBayes and Multinomial NaïveBayes.

### Data
The data consists of 110031 entries and 10 columns. The features mostly were reviews, ratings (1 to 5), date and time, etc.
The feature of interest was “content” which had reviews by various users in English and non-english languages (Script in English and non-english both). After separating the English and non-english reviews, the reviews in English were 89472. The column “content” was cleaned for null values, numbers and punctuation and lemmatized using wordnetlemmatizer. Also, custom stop words were added to the stopwords set. 

### Algorithms
•	K-Means – 5 clusters
•	Non Negative Matrix Factorization (NMF) – 5 topics
•	Naïve Bayes 
#### Results -
•	Five different topics were discovered –
o	Bad Reviews For Paid Subscriptions
o	Profile Match
o	Good Reviews About The App
o	Good Reviews About People On The App
o	Easy To Use
•	Naïve Bayes 
o	Gaussian NB Score – 0.503
o	Multinomial NB Score – 0.855
o	Target is sentiment (Positive or Negative)



### Tools
Pandas – Clean, Explore and Feature Engineering

Scikit-Learn – Build different Classification models and perform cross validation, variable selection and regularization

Matplotlib/ Seaborn – Visualizing data exploration, modeling and results

Python 3.8.5 – to run all of the above

nltk -  Natural language toolkit, to work with human language data.
![image](https://user-images.githubusercontent.com/19984340/194583562-c60d5e1f-9f3e-4d26-b3f2-72e9eef2463b.png)
