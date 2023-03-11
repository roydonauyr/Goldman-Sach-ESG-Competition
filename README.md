# Goldman-Sach-ESG-Comp
![GitHub](https://img.shields.io/github/license/roydonauyr/Goldman-Sach-ESG-Competition)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/roydonauyr/Goldman-Sach-ESG-Competition)
![GitHub repo size](https://img.shields.io/github/repo-size/roydonauyr/Goldman-Sach-ESG-Competition)
![GitHub language count](https://img.shields.io/github/languages/count/roydonauyr/Goldman-Sach-ESG-Competition)
![GitHub last commit](https://img.shields.io/github/last-commit/roydonauyr/Goldman-Sach-ESG-Competition)

Competition on ESG data modelling and predictions

We were tasked with designing a solution for ESG investing and transforming unstructured data into structured data.

# Our Solution
Using LDA and light gradient boosting we extracted ESG data from public sources and transformed unstructured data to well-curated data.

![image](https://user-images.githubusercontent.com/44868878/178102056-687b7836-18ce-466a-b00a-87553a199077.png)

Process flow for text lemmatisation :
1.Use a regular expression to remove any punctuations and lowercase text.
2.Visualise with WordCloud
3.Transform the textual data in a format to serve as an input for training a Latent
Dirichlet Allocation (LDA) model.
• Tokenising the text and removing ‘stopwords’
• Convert the tokenised object into a corpus and dictionary
4.Construct Bigram and Trigram Models
• Bigrams and Trigrams with two important arguments to Phrases model
(min_count and threshold)
5.Perform text lemmatisation keeping only nouns, adjectives, verbs, adverbs
6. Data transformation
• Create Dictionary with gensim corpora library with optional filtering of tokens
• Create Corpus with lemmatised text by converting document (a list of words)
into the bag-of-words format = list of (token_id, token_count) 2-tuples. Each
word is assumed to be a tokenised and normalised string

![image](https://user-images.githubusercontent.com/44868878/178102829-f9b63536-ecc9-4a2a-b1d8-f5dc1550e084.png)

After LDA has been performed, topics can be classified by investors so as to study important key words or phrases regarding company related ESG reports to help investors decide if the company would be a good investment

![image](https://user-images.githubusercontent.com/44868878/178103253-b968666a-2069-400a-b9e3-f734773c1032.png)

Step 2: Using Light Gradient Booster, investors can add in additional features to decide if the company has a category that investors are looking for. These categories can be set by investors and can be used to predict a companies report. Once all reports has been predicted, investors would be able to view which category the company is leaning towards and decide if the company would be a good investment.

![image](https://user-images.githubusercontent.com/44868878/178103014-a09033a5-fa41-4651-8773-74ec6ac42f58.png)

# Further Improvements:
1. Preprocessing texts by removing unnecessary characters, unicode
characters, headers and footers (definable by user).
2. Perform structured analysis on the suggested words to extend stop
words for removal (depending on the domain area).
3. Continuous improvement on the topic model with updates to minimise
data drifts, maintain model relevancy.
4. Explore other models (Probabilistic Latent Semantic Analysis,
Probabilistic Latent Semantic Analysis or lda2vec) and used them for
comparisons with LDA via gensim libraries.
5. Analyse and filter words before storing from derived topics
6. Compute distances (Hellinger, Kullback-Leibler, Jaccard) between
each topic clusters and group based on distances (centroids).
7. Improve on the ESG word data bank with more relevant documents.
8. Perform feature engineering to improve ESG predictions.
9. Optimal hyperparameters for the Multi-class Classifier.
