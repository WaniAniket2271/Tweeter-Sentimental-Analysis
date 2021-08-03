# Pattern Recognition and Machine Learning 
## Project: Twitter Sentiment analysis

### Install

This project requires **Python 3.6** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [nltk](https://www.nltk.org/)
- [re](https://docs.python.org/3/library/re.html)
- [wordcloud](https://pypi.org/project/wordcloud/)
- [collections](https://docs.python.org/3/library/collections.html)
- [string](https://docs.python.org/3/library/string.html)

You will also need to have software installed to run and execute a [Jupyter Notebook](http://jupyter.org/index.html) or you can use [colab notebook](https://colab.research.google.com/).

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. Make sure that you select the Python 3.x installer. Other wise you can simply download and upload `B19EE009_B19EE001_B19CSE107.ipynb` on colab. There almost all above dependencies are already installed except `nltk`. For that in the begining itself we have added commands to install it. So you don't need do any special setup tasks to run this file.

### Data

This is the sentiment140 dataset. It contains 1,600,000 tweets extracted using the twitter api. The tweets have been annotated (0 = negative, 4 = positive) and they can be used to detect sentiment. [Dataset link](https://www.kaggle.com/kazanova/sentiment140).

**Content** <br />
It contains the following 6 fields:
1. `target`: the polarity of the tweet (0 = negative, 2 = neutral, 4 = positive)
2. `ids`: The id of the tweet (2087)
3. `date`: the date of the tweet (Sat May 16 23:58:44 UTC 2009)
4. `flag`: The query (lyx). If there is no query, then this value is NO_QUERY.
5. `user`: the user that tweeted (robotickilldozr)
6. `text`: the text of the tweet (Lyx is cool)

### Code

Template code is provided in the `B19EE009_B19EE001_B19CSE107.ipynb` notebook file. You will also be required to use `training.1600000.processed.noemoticon.csv` dataset file to complete your work. You can upload this file on the notebook you are using and just edit dataset filr path inside `pd.read_csv`.
 
**`B19EE009_B19EE001_B19CSE107.ipynb` file structure**
1. Load and explore dataset
   - Null values check
   - Target distribution
   - Tweet label v/s length and word count
   - Word count v/s density plots

2. Preprocessing
   - Remove extra spaces
   - Convert text into lowercase
   - HTMLParser
   - Handle apostrophe
   - Handle short words
   - Remove stopwords
   - Remove URL
   - Remove emojis and emoticons
   - Remove Punctuations
   - Remove any other non english or special symbol
   - Replace wrong spellings with correct spellings
   - Lemmatization with POS = verb
 
 3. Data visualization
     - Word cloud of negative class
     - Word cloud of positive class
     - Plot of top frequent 15 words V/S their count
        - Plot of top frequent 15 words V/S their count for class 0
        - Plot of top frequent 15 words V/S their count for class 1
     - Plot of n-grams (bi-gram and tri-gram) using count vectorizer
        - bi-Gram and tri-gram for document with target 0
        - bi-Gram and tri-gram for document with target 1
 
 4. Data preparation for training
     - Feature Extraction using TF-IDF
     - Train test split
 
5. Train and evaluate models
     - Naive Bayes model 
     - Logistics Regression model
     - Naive Bayes model with (2-gram and 3-gram)
     - Logistics Regression model (2-gram and 3-gram)
     - Naive Bayes model with ((1,2) gram)
     - Logistics Regression model ((1,2) gram)