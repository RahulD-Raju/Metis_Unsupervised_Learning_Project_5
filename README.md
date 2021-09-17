# Finance Use Cases for Natural Language Processing
Prepared by Rahul D. Raju

# Abstract
The stock market is a reflection of the complex interactions amongst humanity, nature and
technology. It is a forward looking mechanism that distills and discounts information in order to
make probability based investment and trading decisions. The list of dependent variables that
are inputed into these decisions are nearly infinite. Historically, the way financial investment
and trading companies have dealt with this was to create numerous sub-specialities and assign
analyst, traders and bankers to each of these. Due to the digital revolution, however, the size,
accessibility and delivery speed of information has grown to the point that even specialists
cannot practically assess data in a timely manner. In response to this, trading firms for
example, have been designing and implementing trading algorithms that quickly incorporate a
vast amount of information in order to make trading decisions far faster than any human. The
quantitative inputs into these algorithms are relatively easy to process, analyze and extrapolate
from. The challenge, however, has been how to effectively translate and incorporate
qualitative(textual) information into actionable trading schemes. The textual information can be
in the form of financial statements, earnings releases and general company specific or
macroeconomic news articles. Any tool that could quickly “decode” this information would
provide enormous advantages to competitive market participants who place a significant
premium on even a nano-second of trading time.

# Data

The data set used in this analysis was found on Kaggle.com. The data ranges in time from
2008 to 2016. It includes the daily top 25 news headlines from the Reddit WorldNews Channel
as ranked in importance by Reddit users. In terms of the target data, a “1” will represent the
daily closing price of the Dow Jones Index if it has risen or remained unchanged since the
previous day’s close. A “0” will represent a decrease in value from the previous day’s close.
Source: Sun, J. (2016, August). Daily News for Stock Market Prediction, Version 1. Retrieved
[September 8th,2021] from https://www.kaggle.com/aaron7sun/stocknews.

# Methodolgy and Algorithms
- Data was broken into training and test data for the supervised portion of the project
- A separate, undivided data set was maintained for the unsupervised portion of the project
- For each day the top 25 headlines, as voted on by Reddit users, were combined into one document
- Punctuation marks, numbers, stop words and capital letters were removed or altered
- Data was inputed into a Count Vectorizer which returned a document-term matrix
- Within Count Vectorizer data was tokenized and stemmed
- Principal Component Analysis was conducted in order to reduce dimensionality
- Data was standardized before PCA
- Supervised Learning:  Random Forest, XGboost, Logistic Regression
- Unsupervised Learning:  Topic Modeling

# Tools
- Pandas
- Sklearn
- Natural Language Toolkit

# Result Summary

- Supervised:  Random Forest produced best results with 0.55 accuracy score
- Unsupervised:  Words such as Georgia, Russia and War were related to the Georgio-Russian war of 2008.  
