
# Coronavirus-Tweet-Sentiment-Prediction

Index
1. Introduction
2. Exploratory Data Analysis./Reviwing Our Dataset
3. Data Preprocessing.
4. Model Training- MULTICLASS AND BINARY.
5. Evaluation.
6. Conclusion

# 1.  Introduction
Our objective is to build a classification model to predict the sentiment of COVID-19 tweets.The tweets have been pulled from Twitter and manual tagging has been done then. The names and usernames have been given codes to avoid any privacy concerns.


![App Screenshot](https://user-images.githubusercontent.com/83903018/124346241-60aa9b80-dbfb-11eb-97a3-a9251066302c.png)
We are given the following information:

1.Username: Unique user-IDs of the users

2.Location: Location of the user

3.Tweet At: Date at which the tweet was made

4.Original Tweet: The exact tweet

5.Sentiment: Sentiment of the tweet

# Workflow in this Project
![App Screenshot](https://user-images.githubusercontent.com/82259772/130586521-be05913c-1b2f-4a20-85f2-1982a833daeb.PNG)

# 2. Exploratory Data Analysis
The original dataset has 6 columns and 41157 rows.

There are five types of sentiments- Extremely Negative, Negative, Neutral, Positive and Extremely Positive.

![App Screenshot](https://user-images.githubusercontent.com/82259772/130582963-6cb693e3-56f2-4be1-a955-ac31b989031a.PNG)

All tweets data collected from the months of March and April 2020. Bar plot shows us the number of unique values in each column.

![App Screenshot](https://user-images.githubusercontent.com/82259772/130583054-5a72da4c-329e-4dc8-9fd7-b5872b328322.PNG)

The columns such as “UserName” and “ScreenName” does not give any meaningful insights for our analysis.


There are 20.87%(8567) null values in various places of location column.

Most of the tweets came from London followed by U.S.

![App Screenshot](https://user-images.githubusercontent.com/82259772/130583140-b8b4d2fb-62e5-44fa-8fbe-8d882d1de497.PNG)


# 3. Data Preprocessing
1. The preprocessing of the text data is an essential step as it makes the raw text ready for mining.


2. The objective of this step is to clean noise those are less relevant to find the sentiment of tweets such as punctuation, special characters, numbers, and terms which don’t carry much weightage in context to the text.


3. Stop words are those words in natural language that have a very little meaning, such as "is", "an", "the", etc.To remove stop words from a sentence, you can divide your text into words and then remove the word if it exits in the list of stop words provided by NLTK.

4. Stemming is a rule-based process of stripping the suffixes (“ing”, “ly”, “es”, “ed”, “s” etc) from a word. For example – “play”, “player”, “played”, “plays” and “playing” are the different variations of the word – “play”.


5. Lemmatization is a more powerful operation, and it takes into consideration morphological analysis of the words. It returns the lemma which is the base form of all its inflectional forms.

6. In tokenization we convert group of sentence into token . It is also called text segmentation or lexical analysis. It is basically splitting data into small chunk of words. Tokenization in python can be done by python NLTK library’s word_tokenize() function

After cleaning text we also create wordblog

![App Screenshot](https://user-images.githubusercontent.com/82259772/130586193-9eea8926-321f-452f-9af0-118f1276e9aa.PNG)


# 4. Model Training- MULTICLASS AND BINARY.
Trained Naive Bayes algorithms for each Multiclass and Binary classification. In Multiclass we have 5 different classes but in binary we have only two class i.e. Positive and Negative. Reason to choose Naive Bayes algorithm because it is a simple classification algorithm which uses probability of the events for its purpose. It is based on the Bayes Theorem which assumes that there is no interdependence amongst the variables.

The Naive Bayesian classifier consists of performing the below steps –

1. Create a frequency table based on the words
2. Calculate the likelihood for each of the classes based on the frequency table
3. Calculate the posterior probability for each class
4. The highest posterior probability is the outcome of the prediction experiment
#
All these probabilities are calculated by using the Bayes Theorem. As the Naive Bayes algorithm has the assumption of the “Naive” features it performs much better than other algorithms like Logistic Regression, Tree based algorithms etc. The Naive Bayes classifier is much faster with its probability calculations.

# 5. Evaluation
For Multiclass Classification we got accuracy as -

![App Screenshot](https://user-images.githubusercontent.com/82259772/130586271-af765d82-84b0-4a7b-a452-39dee1316a84.PNG)


For Binary Classification we got accuracy as -

![App Screenshot](https://user-images.githubusercontent.com/82259772/130586375-af9dc8f2-686d-482c-ad1e-927932ef1413.PNG)

Also Confusion Matrix for Binary Classification -

![App Screenshot](https://user-images.githubusercontent.com/82259772/130586321-6712b4c3-f4f1-4123-989a-be75735076cb.PNG)


# 6. Conclusion
1. For multiclass classification, the best model for this dataset would be CatBoost
2. For binary classification, the best model for this dataset would be Stochastic Gradient Descent

![App Screenshot](https://user-images.githubusercontent.com/82259772/130586434-d070da2a-18df-4d34-aa76-3d38a1e77a7c.PNG)




