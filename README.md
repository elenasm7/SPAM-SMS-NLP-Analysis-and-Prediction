# SPAM-SMS-NLP-Analysis-and-Prediction
Using supervised natural language processing to predict whether an SMS message is spam or ham (not-spam).

We use both logistic regression and random forest to classify outcomes. Due to the class imbalance of this problem, I will walk through multiple ways of dealing with this issue when it comes to predictions. I will also adress the other areas that it may affect.

# SMS Spam Classification

This project I will be looking into SMS text data from multiple sources all collected by the team [Tiago A. Almeida](http://dcomp.sor.ufscar.br/talmeida/) and [José María Gómez Hidalgo](http://www.esp.uem.es/jmgomez). For more information on how they collected this data check it out [here](http://www.dt.fee.unicamp.br/~tiago/smsspamcollection/).

Some notable sources used while performing this analysis and classification: 
- [Ultimate guide to deal with Text Data (using Python)](https://www.analyticsvidhya.com/blog/2018/02/the-different-methods-deal-text-data-predictive-python/)

The data here is a collection of 747 Spam texts along with 4,827 non-spam (HAM) texts. The file is formatted as a plain text file.

The first phase consisted of feature engineering, to help with a single logistic regression:

Before any of this I did a little bit of text exploring to see if I could see anything that may or may not help me--this was crucial for choosing __'flag words'__. Items like word count, char counts, number of numerics, number of upper case, etc. are pretty common practice, so they are great features to add to your data set before cleaning. 

1. word count
2. character count
3. Number of numerics
4. Number of upper case
5. Number of Exclamation Points (!)
6. Number of Flag Words
7. Links in message
8. Count of stop words
