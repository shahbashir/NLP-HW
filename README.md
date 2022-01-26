# NLP-HW
I will be uploading NLP homework in this section
Sentiment analysis is a process to determine emotional tone within a text. For this analysis, SentimentIntensityAnalyzer was imported from NLTK.Sentiment.Vader library.
# Technical Steps
An API key environment variable was read into the code to create a newsapi client that fetched the news articles with .get_everything() using key words Bitcoin and Ethereum. There were 4321 results returned for Bitcoin and 900 for Ethereum. Only the title and content of each article was extracted and saved, noting newspai truncates the content of free articles to the first 260 characters.

Sentiment scores were run on the content of each article applying sentiment = analyzer.polarity_scores(text) and analyzer.polarity_scores(). The sentiment scores, titles of articles, and content were saved to DataFrames.

The sentiment score results were then summarized .describe()

Bitcoin and Ethereum had similar mean positive scores, Bitcoin marginally higher. Bitcoin had the highest mean compound score, but Ethereum had the highest maximum compound score as well as the highest maximum positive score. Results overall were similar with both showing low negative scores and sentiment primarily neutral.
# Tokenizer
Tokenization is the process of segmenting text into words, sentences, or phrases to be used as inputs for further word or sentence processing.

Before tokenization, the content of text was cleaned to remove punctuation, non-alphabet characters, and stop words. All words were reduced to lowercase and returned in root form, a process known as lemmatization. Stopwords are common words that are present in the text but generally do not contribute to the meaning of a sentence. The NLTK package provides a pre-determined list of stopwords. Once the text was cleaned, the words in the content of each article were tokenized with word_tokenize.

Then the title and content of each article were run through the tokenizer function and outputs were added to the DataFrames.
# N-Grams and Frequency Analysis
N-Grams and Frequency analysis are performed at the word level. N-gram is a contiguous sequence of n items from a given sequence of text or speech. Frequency counts the number of times a word is used. Both are helpful in providing insight into words and phrases commonly associated with the text.

In this analysis, ngram of size 2 was used from the NLTK library, and Counter to perform Frequency analysis from the Collections module.
# Word Clouds
Word Clouds are used to visually represent text data, the size of each word indicates its frequency. A word cloud was generated for Bitcoin and Ethereum using the WordCloud library.
# Named Entity Recognition
Named entity recognition locates and classifies named entities in the text into pre-defined categories, definitions below.

A named entity recognition was generated for both coins and visualized using displacy from the SpaCy library.
# Conclusion

In conclusion, the sentiment scores were neutral for Bitcoin and Ethereum. The common phrases and words associated with Bitcoin and Ethereum significantly differed. Satoshi Nakamoto, the name used for the creator of Bitcoin, was the most used for Bitcoin. And for Ethereum, blockchain and Ethereum were most commonly used together. Surprisingly, Bitcoin was used more often in Ethereum's articles than Ethereum, which may illustrate Bitcoin's dominance in the cryptocurrency space. But Ethereum had a wider variety of words including blockchain, cryptocurrency, finance, digital, and may indicate a difference in perception of Ethereum's technology verse Bitcoin that could be used as a basis for further exploration.





