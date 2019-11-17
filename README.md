# Quora Question Pair Similarity

Quora is a place to gain and share knowledge—about anything. It’s a platform to ask questions and connect with people who contribute unique insights and quality answers. This empowers people to learn from each other and to better understand the world.

Over 100 million people visit Quora every month, so it's no surprise that many people ask similarly worded questions. Multiple questions with the same intent can cause seekers to spend more time finding the best answer to their question, and make writers feel they need to answer multiple versions of the same question. Quora values canonical questions because they provide a better experience to active seekers and writers, and offer more value to both of these groups in the long term.
Problem Statement

    Identify which questions asked on Quora are duplicates of questions that have already been asked.
    This could be useful to instantly provide answers to questions that have already been answered.
    We are tasked with predicting whether a pair of questions are duplicates or not.

Data Overview

    Data will be in a file Train.csv
    Train.csv contains 5 columns : qid1, qid2, question1, question2, is_duplicate
    Size of Train.csv - 60MB
    Number of rows in Train.csv = 404,290
   
Additional features

    1. common word ratio 
    2. common first word
    3. common token ratio
    4. common stop-word ratio
    5. absolute difference b/w length of string
    
To get advance features form texts we used Fuzzywuuzy. FuzzyWuzzy is a library of Python which is used for string matching. Fuzzy string matching is the process of finding strings that match a given pattern. Basically it uses Levenshtein Distance to calculate the differences between sequences.

    1. fuzzy ratio
    2. token sort ratio
    3. token set ratio
    4. partial ratio

To vectorize text data two text vetorization methods are used

    1. TFIDF
    2. TFIDF-Word2vec
 
models we used for case study

    Logistic Regression
    Linear SVM
    XGboost
    
Metric used for the evaluation of model is Log-loss


