# frequency-of-suffixes
In this project, it is aimed to find the frequency of positive, neutral and negative meaning according to the usage rates of the suffixes brought to the end of Turkish words. Thus, we will be able to rate the negative, positive and neutral meanings of the Turkish suffixes. This can contribute to NLP(Natural Language Processing) studies for Turkish Language.
# prerequests
-> Zemberek packages if you want derive yoru own data
-> Jupyter Notebook
-> python 3
-> pandas and sklearn packages
# preparing data
I made my own data. With the help of the word generation code of the Zemberek library, I produced about 240000 derived Turkish words out of 10000 Turkish word roots. Then I threw them into csv.
*Thanks to
https://github.com/ahmetaa/zemberek-nlp/blob/master/examples/src/main/java/zemberek/examples/morphology/GenerateWords.java
https://github.com/ozturkberkay/Zemberek-Python-Examples/blob/master/examples/morphology/word_generation.py

Firstly, I tagged the words that suffixes have been as positive, negative and neutral according to their meaning. We then separated the suffixes from the roots using the stem and lemmatize code of the Zemberek library. Then we kept these suffixes and tags in the csv file, Suffixes and Labels, respectively.
# writing code and training model
I created a dataframe from the data (Suffixes, Labels) using the pandas library.

I vectorized the data in the dataframe for the model to understand. So I converted it to numerical values.

I used Multinominal Naive Bayes Model from Sklearn library for my training process. I think it is good classifier for sentiment analysis.

The number of suffixes in each of the categories was calculated.

Thanks to Naive Bayes, the frequency of each suffix in negative, positive and neutral categories was calculated.

Finally, I used Metrics from Sklearn library to find accuracy rate of my model.
