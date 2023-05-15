

This project is a text classification task that aims to classify Reddit posts into one of five categories: Telegram, Facebook, Instagram, Linkedin, and Viber. This project uses the Bernoulli Naive Bayes algorithm to perform the classification task. The project is written in Python.

# Data

The project uses two datasets: train.csv and test.csv. Both datasets contain Reddit posts with the following columns:

id: A unique identifier for each post.
body: The text content of the post.
subreddit: The subreddit where the post was published.
created_utc: The timestamp of the post.
The train.csv dataset is used to train the model, while the test.csv dataset is used to evaluate the performance of the model.

# Data Cleaning

Before training the model, the text content of the posts is preprocessed. The following steps are taken:

URLs and HTML tags are removed from the text.
Non-alphabetic characters are removed from the text.
Stop words are removed from the text.

# Model

The Bernoulli Naive Bayes algorithm is used to classify the text data. The algorithm calculates the probability of a post belonging to a particular category based on the presence or absence of each word in the post.

To apply the algorithm, the text data is first tokenized and transformed into a binary bag-of-words representation. Two different tokenizers are used for this project: StemTokenizer and New_LemmaTokenizer. The StemTokenizer stems each word in the text using the Porter Stemmer, while the New_LemmaTokenizer lemmatizes each word in the text using the WordNetLemmatizer. The New_LemmaTokenizer also maps the part-of-speech tags to the WordNet POS tags.

The cal_theta method is used to calculate the prior probability of each class and the likelihood of each feature given the class. The class_prob method is used to calculate the posterior probability of each class given the sample.

The accuracy_rate method is used to calculate the accuracy of the model.

Finally, the predict method is used to predict the class labels of the test data.
