# spam-detection

This is a spam detection project based on dataset from Applied Text Mining in Python - University of Michigan - Coursera

The dataset contains 5572 messages, among them 13.4% are spam.

The metric used from the scoring is Area Under Curve (AUC)

AUC is a performance measurement for classification problem and represents degree or measure of separability. It tells how much model is capable of distinguishing between classes. Higher the AUC, better the model is at predicting spam messages as spam and non spam messages as non spam. For example if AUC is 80% it means there is 80% chance that model will be able to distinguish between positive class and negative class.

Text representation was performed with CountVectorizer and TfidfVectorizer from Scikit Learn Library.  

We add some additional features :  
* number of digits
* document length
* number non words in the test

Different machine learning algorithms has been tested :  

* Logistic Regression
* Naive Bayes
* Support Vector Classifier

The results are as follow : 

|Model   | AUC Score on test Set  |
|---|---|
|Logistic Regression classifier with CountVectorizer and additional features|0.979
|Naive Bayes classifier with CounterVectorizer|0.972
|Logistic Regression classifier with TfidfVectorizer and additional features|0.965
|Support Vector classifier with TfidfVectorizer and additional feature|0.958
|Naive Bayes classifier with TfidfVectorizer|0.942

The best algorithm is found to be logistic regrssion classifier with CountVectorizer and adding new features.