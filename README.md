COMPANY: CODTECH IT SOLUTIONS

NAME: SARAVANNAN S G

INTERN ID : CT04WUC

DOMAIN : PYTHON PROGRAMMING

DURATION : 4 WEEKS

MENTOR : NEELA SANTOSH

#DESCRIPTION

This Python script implements sentiment analysis using machine learning models to classify user reviews as positive or negative. It leverages the pandas library for data manipulation, scikit-learn for machine learning models, and CountVectorizer for transforming text into numerical features. The dataset used is a tab-separated values (TSV) file named opinions.tsv, which contains two columns: Sentiment (binary labels: 0 for negative, 1 for positive) and Review (textual data). The script begins by reading the dataset into a pandas DataFrame and splitting it into training and testing sets using an 80-20 ratio. The CountVectorizer is applied to convert text into numerical feature representations, ignoring English stopwords and filtering out rare and overly common words. The text data is then transformed into document-term matrices (DTM) for training and testing.

The script evaluates four different classification models: Naïve Bayes (MultinomialNB), Logistic Regression, Support Vector Machine (LinearSVC), and K-Nearest Neighbors (KNN). Each model is trained on the training data, and its accuracy is measured on the test set using accuracy_score and a confusion matrix to analyze prediction errors. Among the models, Logistic Regression is identified as the best-performing model based on accuracy. Additionally, the script provides Naïve Bayes-based analysis, extracting feature counts for positive and negative reviews, determining the number of positive and negative tokens, and allowing users to check sentiment weights for specific words. It also identifies false negatives (actual positive but predicted negative) and false positives (actual negative but predicted positive) for further error analysis.

The final part of the script allows users to input a custom review for sentiment analysis. A new CountVectorizer is fitted on the complete dataset, and a Logistic Regression model is retrained using the full data. The user provides a review, which is vectorized and classified as positive or negative based on the trained model. This interactive functionality enhances the practicality of the sentiment analysis tool. Overall, the script effectively demonstrates natural language processing (NLP) techniques and machine learning classifiers to analyze textual sentiment, offering both automated classification and interpretability through token analysis and model evaluation.

#OUTPUT
Naive Bayes
Accuracy Score: 98.91618497109826%
Confusion Matrix: 
[[586  12]
 [  3 783]]

Logistic Regression
Accuracy Score: 99.34971098265896%
Confusion Matrix: 
[[593   5]
 [  4 782]]

Support Vector Machine
Accuracy Score: 99.0606936416185%
Confusion Matrix: 
[[592   6]
 [  7 779]]

K Nearest Neighbors (NN = 3)
Accuracy Score: 98.69942196531792%
Confusion Matrix: 
[[589   9]
 [  9 777]]

Analysis
No. of tokens:  294
No. of positive tokens:  143
No. of negative tokens:  151

Search Results for token/s: ['awesome']
      Token  Positive  Negative
11  awesome     896.0       1.0
3001    yeah i know the two movies are of different ge...
1172     today was so cool and mission impossible rocked.
1185    Think Mission Impossible, think Bond Girls, th...
1162    mission impossible did kick ass and yes jessic...
1122    Mission impossible was pretty cool, though I w...
2998        I did kinda like Brokeback Mountain though...
2992    no, I hope this doesn't end up like Brokeback ...
2991    and i wanna shout out a big fat thank you to e...
2993        gosh i miss telling Brokeback Mountain news!.
Name: Review, dtype: object
5032                     And Harry Potter looks stupid:..
5107     I could hate Harry Potter, but love his scent...
4038    i hated the da vinci code, the movie witha pas...
3953    If Jesus is fabricated a la the Da Vinci Code ...
5109    I loathe Harry Potter, Lord of the Rings and a...
5035    I am SOOOOOO sick of people claiming that Harr...
3945    i thought the da vinci code movie was really b...
5038    Wiccans react to possible Harry Potter book ba...
5050    Marcia Gaither, who teaches classes in Wiccani...
Name: Review, dtype: object

Test a custom review message
Enter review to be analysed:  
 12
The review is predicted Positive
