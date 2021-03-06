# Twitter Financial disambiguation-Financial User Relevance
This repository holds three csv files used for the TFD-FUR (Twitter Financial disambiguation-Financial User Relevance) task. 

The file named steel_news_titles.csv contains the downloaded titles from steel authorative sources (Kallanish Commodities and SteelOrbis) with the pubblication date while the file generic_news_titles.csv holds the generic titles from Reuters, The New York Times and a sample of 44,182 titles from the dataset available at https://www.kaggle.com/therohk/million-headlines/home. 

The third file, called sample_3000_labeled_tweets.csv holds 3,000 labeled tweets randomly selected from a dataset of 533,759 tweets downloaded in the period between March 2017 and October 2018 using the keywords: steel price, steel production, steel industry. The dataset is used as further example for the Twitter Financial disambiguation (TFD) task in which the target is to identify tweets strictly related to the alloy steel domain (manually labeled as 1) discarding the out-of-topic ones (manually labeled as 0). 

The file is composed by 46 columns as follows:
1) id: it is the ID number of each tweet,
2) Date: the date in which the tweet has been written,
3) Text: the text of the original tweet,
4) Cleaned Text: the original tweet is preprocessed applying stopwords and punctuation removal,
5) tfidfC_binary__score: the score achieved applying the TF-IDFC binary method,
6) IG__score: the score achieved applying the IG statistical measure,
7) PMI__score: the score achieved applying the PMI statistical measure,
8) LDAk (columns 8-25): the k LDA features (k=17) used in the Supervised Machine Learning algorithms,
9) BTMk (columns 26-43): the k BTM features (k=17) used in the Supervised Machine Learning algorithms,
10) tfidfC_unary__score: the score achieved applying the TF-IDFC unary method,
11) svmLinear_prob__1: the proabability of linar SVM classification (probability to belong to the class 1) with C value set to 0.001),
12) Manual label (Ground Truth): the manualy labeled class which are 1 for the alloy steel tweet and 0 otherwise.
