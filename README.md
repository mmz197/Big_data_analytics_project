# Big_data_analytics_project
The project analyzes 27,481 Twitter posts using Pandas and PySpark. It includes dataset loading from Kaggle, sentiment distribution analysis, text cleaning with regex and tokenization, and keyword extraction. Finally, Matplotlib visualizations highlight the top frequent words, revealing trends in positive, negative, and neutral sentiments.

# **PERFORMED BY :**

**MUHAMMAD MUNEEB 23-ag-9627**

**MUHAMMAD AHTISHAM JAVAD 23-ag-9637**

## **THE FOLLOWING ARE THE DETAILS OF ALL THE TASKS PERFORMED IN THIS PROJECT :**

## 1. Data Acquisition & Environment Setup:
The process begins by setting up the necessary tools and gathering the raw data.
**Dataset Retrieval:** The notebook uses kagglehub to programmatically download the "Twitter Tweets Sentiment Dataset" directly from Kaggle.
**Library Imports:** It imports essential data manipulation libraries like pandas and os to navigate the file system and load the downloaded CSV file.

**Initial Inspection:** The code automatically detects the Tweets.csv file within the downloaded directory and loads it into a Pandas DataFrame to get a first look at the data.

## 2. Exploratory Data Analysis (Pandas):
Before diving into heavy processing, the notebook performs a preliminary check of the dataset structure.
**Data Preview:** Using head() and tail(), it examines the first and last few rows of the dataset.

Understanding the Content: 
The dataset consists of 27,481 records with four main columns:
      **textID:** A unique identifier for each tweet.
      **text:** The full original tweet.
      **selected_text:** The specific segment of text that indicates the sentiment.
      **sentiment:** The manual label (positive, negative, or neutral).

## 3. Transitioning to Big Data (PySpark):
A significant portion of the notebook is dedicated to scaling the analysis using PySpark, which is designed to handle much larger datasets than standard Pandas.

**Spark Installation:**The notebook ensures pyspark is installed in the environment.

**Session Creation:** It initializes a SparkSession named "SocialMediaSentimentAnalysis" to manage the distributed computing tasks.

**Schema Definition:** The CSV is re-loaded into a Spark DataFrame, where the system infers the data types (Schema) for each column.

## 4. Deep-Dive Sentiment Statistics
Once the data is in Spark, the notebook calculates specific metrics to understand the distribution of emotions:

**Class Distribution:** It groups the tweets by sentiment and counts them:
    **Neutral:** 11,118 tweets.
    **Positive:** 8,582 tweets.
    **Negative:** 7,779 tweets.

**Filtering:** The notebook creates specific subsets of data to isolate only positive or negative posts for closer inspection.

## 5. Text Cleaning & Keyword Analysis
To extract meaningful insights, the raw tweet text is "cleaned" to remove noise.

**Normalization:** It converts all text to lowercase and uses Regular Expressions (Regex) to strip out special characters, numbers, and punctuation, leaving only alphabetic words.

**Word Tokenization:** The cleaned sentences are "exploded" into individual words.

**Frequency Mapping:** It counts how many times each word appears across the entire dataset. The analysis shows that common "stop words" (like "i", "to", "the", "a") are the most frequent.

## 6. Data Visualization
Finally, the notebook translates the raw counts into a visual format.

**Keyword Plotting:** Using matplotlib, it generates a bar chart showing the Top 20 Most Frequent Keywords found in the tweets, providing a clear visual representation of the most common language used in the dataset.
