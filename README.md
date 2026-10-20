# Project 34 Sentiment Analysis on Tweets with Transformer Models
The goal of this project is to perform sentiment analysis on a dataset of tweets with additional
demographic and global context features, including user age, country, and population statistics. This
project will explore the use of state-of-the-art transformer-based models to analyze sentiment while
incorporating metadata such as tweet time, user demographics, and country data to provide a more
holistic sentiment analysis. Sentiment Analysis Dataset Sentiment Analysis Dataset contains the
following fields: textID, text, selected_text, sentiment, Time of Tweet, Age of User, Country,
Population 2020, Land Area (Km²), and Density (P/Km²).

### 1. Data Exploration and Preprocessing: 
Explore the distribution of tweets by sentiment, Age of User, Country, and Time of Tweet. Visualize the data using appropriate charts such as bar charts, histograms,
and heatmaps.

### 2. Exploratory Analysis of Demographics: 
Analyze the correlation between demographic
information (e.g., Age of User, Country) and the sentiment of the tweets. Identify if certain age groups
or countries tend to express more positive, negative, or neutral sentiments. Also. analyze how density
affects sentiment patterns.

### 3. Time of Tweet and Sentiment Trends: 
Investigate how the time of tweet (morning, noon, night)
correlates with sentiment. Do people tend to tweet more positively or negatively at certain times of the
day? Visualize sentiment trends over time to identify any patterns (e.g., higher negativity during late
hours or weekends).

### 4. Topic Modeling with LDA on Tweets: 
The main aim of this task is to use LDA (Latent Dirichlet
Allocation) to discover hidden topics within the tweet dataset and analyze how these topics correlate
with different sentiment classes (positive, neutral, negative). Apply LDA to the text or selected_text
field to identify the most common topics discussed in the tweets. After extracting the topics, categorize
tweets based on the most likely topic and analyze the distribution of sentiment across different topics.
Visualize the topics using word clouds or bar charts to interpret the most frequent words associated
with each topic.

### 5. Coherence-Based Topic Model Tuning: 
The purpose of the task is to optimize LDA’s performance
by tuning the number of topics based on topic coherence. Experiment with different numbers of topics
for LDA (e.g., 5, 10, 15, 20) and use a coherence score (e.g., CV coherence) to evaluate the quality of
the topics. Fine-tune the number of topics based on coherence score to identify the most meaningful
number of topics for the dataset.

### 6. Word Embeddings for Topic Similarity: 
The aim of this task is to use Word2Vec or BERT-based
embeddings to analyze the similarity between different topics extracted via LDA (Task 4). Generate
word embeddings for the most frequent words in each LDA topic using Word2Vec or BERT. Calculate
the cosine similarity between different topics based on their word embeddings to see which topics are
semantically similar. Visualize the similarity between topics using heatmaps or dendrograms.

### 7. Topic Sentiment Evolution with Transformer Embeddings: 
In this task we want to combine
transformer-generated embeddings (e.g., BERT embeddings) with LDA to improve topic extraction
and sentiment analysis. Generate sentence embeddings for each tweet using a transformer model like
BERT. Use these embeddings as input for an LDA variant that works with dense vectors (e.g.,
BERTopic). Analyze the resulting topics and their sentiment evolution, paying close attention to how
transformer embeddings impact the quality and coherence of topics.

### 8. Sentiment Analysis Using Transformers: 
Leverage pre-trained transformer models such as BERT,
RoBERTa, and DistilBERT for sentiment classification (positive, neutral, or negative). Fine-tune these
models on the train dataset using the text and selected_text (which represents the portion of the tweet
most relevant to the sentiment) columns separately. Then, conduct fine-tuning by training on the
labeled sentiment data on train data and test the result on Test data. Additionally, experiment with
different variants of BERT (e.g., BERT-large vs. BERT-base) to improve accuracy. Compare the
performance of transformer models (BERT, RoBERTa) against other NLP techniques, such as TF-IDF
+ Logistic Regression, to demonstrate the advantage of transformers in this sentiment classification
task.

### 9. Multi-modal Analysis with Metadata: 
Incorporate user demographic features (Age of User,
Country, Population 2020, Density (P/Km²)) along with tweet text in the model. Train a multi-input
model where one branch processes the textual content (using transformers) and another branch
processes demographic and geographical features of the users. Combine the results to make a final
sentiment prediction. Evaluate the importance of each feature using SHAP values or feature importance
analysis to understand the contribution of text versus demographic data to the overall sentiment
prediction.

### 10. Sentiment Prediction Using Pre-trained LLMs:
 Apply LLMs like GPT to classify tweet
sentiment by fine-tuning them on this dataset. These models, with their ability to capture nuanced
contextual relationships, could outperform smaller transformer models on more complex sentiment
tasks. For models like GPT, experiment with prompt engineering to extract sentiment in a zero-shot or
few-shot learning setting, where the model makes predictions based on minimal examples. Finally.
compare the sentiment classification performance of fine-tuned BERT,and LLM using accuracy
measures.

### 11. Error Analysis and Improvements:
Perform error analysis by inspecting tweets where the
sentiment prediction was incorrect. Look for patterns in errors, such as sarcasm, complex language, or
ambiguity. Optionally experiment with LLMs such as GPT for more advanced contextual
understanding and sentiment classification. Compare their performance with transformer-based models
like BERT or RoBERTa.

### 12. Advanced Transformer and LLM techniques and Suggestions: 
Feel free to analysis and explore
additional Transformer and LLM techniques or state-of-the-art models to improve the sentiment
analysis task. You can experiment with other state of the art models, comparing their performance to
the previously used methods.

### 13. Identify appropriate literature to discuss the findings and comment on the strength and weakness of the data processing pipeline.