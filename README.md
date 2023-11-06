# Document-Search-Engine
## Introduction
The Document Search Engine is a semantic search engine that allows users to search for
documents based on their content. It utilizes the 20newsgroup open-source dataset for building
the search engine.
## Prerequisites
To use the Document Search Engine, you need to have the following prerequisites:
● Python 3.x installed
● Required Python libraries (Sklearn, Numpy, Pandas, nltk.)
Data Collection
The data collection process involves gathering the necessary documents for the search engine.
In this project, the 20newsgroup dataset is used as the source of documents.
The 20newsgroup dataset consists of approximately 20,000 newsgroup documents, partitioned
(nearly) evenly across 20 different newsgroups.
Dataset link: http://qwone.com/~jason/20Newsgroups/
## Data Cleaning
The collected data contain noise, irrelevant information, or special characters. The data cleaning
step aims to preprocess the documents and remove any unwanted elements.
● Document Subject Retrieval from Data.
● Data Cleaning and Preprocessing (Remove new line, white space ,E-mail , from, etc).
Data Preprocessing
To prepare the data for use in the search engine, several preprocessing steps are performed,
including:
● Lowercasing the text
● Word tokenization
● Stop word removal
● Word lemmatization
After preprocessing, the data is ready to be used in the search engine.Document Search Engine
The Document Search Engine utilizes various techniques to calculate the similarity between
documents and user queries. Two different approaches are implemented in this project:
### 1. Document Search Engine with TF-IDF
This approach uses the Term Frequency-Inverse Document Frequency (TF-IDF) technique to
rank the documents based on their relevance to the user query. The following steps are
involved:
● Calculating the Term Frequency (TF) for each word in the documents
● Calculating the Inverse Document Frequency (IDF) for each word in the corpus
● Generating the TF-IDF matrix using the TfidfVectorizer from Sklearn
● Creating a vector representation for the query/search keywords
● Calculating the cosine similarity between documents and the query
● Ranking the documents based on their cosine similarity scores
● Testing the search function
### 2. Document Search Engine with Google Universal Sentence Encoder
In this approach, the Google Universal Sentence Encoder (USE) is used to encode the
documents and queries into fixed-length vectors. This allows for semantic similarity comparison
between sentences. The following use cases are covered: Use Case 1: Word semantic
similarity. And Use Case 2: Sentence semantic similarity.
The following steps are involved:
  Loading the model from TF hub.  
  Understanding the use case of Google USE.
  Training the Google USE model in batches, with a chunk size of 1000 rows.
  Obtaining top similar documents by inputting keywords or sentences.
  Training the Google USE model in batches, with a chunk size of 1000 rows.
  Obtaining top similar documents by inputting keywords or sentences.
