# Chess Game Prediction

## Group Information
**Group No:** 09  
**CSE422 Lab Section:** 10  
**Semester:** Spring 2024

| ID        | Name         |
|-----------|--------------|
|   | MD ASIF HASAN |
|   | MD FAHIM      |

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Dataset Pre-processing](#dataset-pre-processing)
4. [Dataset Splitting](#dataset-splitting)
5. [Model Training](#model-training)
6. [Comparison Analysis](#comparison-analysis)
7. [Conclusion](#conclusion)
8. [References](#references)

## Introduction
This project aims to use machine learning techniques to predict the outcomes of chess games. By analyzing data from online chess platforms, the project addresses the challenge of predicting the outcomes of online chess games based on various factors such as player ratings, opening moves, and game duration. The project seeks to develop models that can accurately forecast whether a player will win, lose, or draw a game. The motivation behind the project arose from the increasing interest in online chess as both a recreational activity and a competitive sport. With millions of players engaging in online chess matches daily, there is a growing demand for tools and resources that can help players enhance their gameplay and achieve better results by applying machine learning techniques to analyze large datasets of online chess games.

## Dataset Description
- **Source:** The dataset represents a collection of online chess game records. The problem of predicting the winner of chess games can be framed as a classification problem because the outcome of the game can be categorized into discrete classes: win, lose, or draw. There are a total of 20,058 data points in the dataset and both quantitative and categorical features in the dataset. From the dataset, we can see that both numerical values and discrete categories or labels are present. After dataset preprocessing, there are a total of three features: turns, victory_status, and time_increment.

![Dataset Correlation](https://www.kaggle.com/datasets/ulrikthygepedersen/online-chess-games)

## Dataset Pre-processing
The dataset has null values in `opening_response` and `opening_variation`. Since these are not mandatory features for the task, we can delete these columns. Additionally, there are some unwanted features for the task, which can be deleted as well. The `time_increment` column is in the wrong format, so it is split and added using a lambda function to make the total time. Finally, categorical variables are converted to numerical format for the columns `victory_status` and `winner`.

## Dataset Splitting
For the features (X), we choose `turns`, `victory_status`, and `time_increment`, and for the label (y), we choose the `winner` column from the dataset. The test set is 30% of the dataset, and the remaining 70% is the training set.

## Model Training
For the model training, we chose three models: KNN, Decision Tree, and Logistic Regression. The training, testing, and accuracy scores of the models are given below.

## Comparison Analysis
The accuracy scores of the three models (KNN, Decision Tree, and Logistic Regression) are showcased using a bar chart. Additionally, the precision, recall, and f1 score of each model, along with the confusion matrix of each model, are provided.

Based on our analysis of three distinct models, it is clear that the Decision Tree model exhibits the highest level of accuracy. Therefore, we propose deploying the Decision Tree model to predict the winners using the dataset provided by the online chess game dataset platform. This selection is based on its demonstrated greater performance relative to alternative models evaluated during the testing process.

## Conclusion
This project aimed to develop machine learning models to predict the outcomes of chess games using data from online chess platforms. The problem was framed as a classification task, where the outcome of the game was categorized into discrete classes: win, lose, or draw. With a dataset comprising 20,058 data points, both quantitative and categorical features were present, including numerical values and discrete categories or labels.

During dataset preprocessing, null values in certain features were handled, and irrelevant columns such as `opening_response` and `opening_variation` were removed. Categorical variables were converted to numerical format for the features `victory_status` and `winner`.

After preprocessing, the dataset consisted of three features: `turns`, `victory_status`, and `time_increment`. For model training, KNN, Decision Tree, and Logistic Regression were selected. The dataset was split into a 70% training set and a 30% test set for model evaluation.

The project's goal was to create precise prediction models to anticipate chess game outcomes by experimenting with these models. The project's outcomes provided insight into the forecast accuracy of the data models. Players may find that the project's findings and insights can help them improve their gameplay techniques and perform better in online chess tournaments.

## References
1. Online Chess Games. (2023, March 23). Kaggle. [Online Chess Games Dataset](https://www.kaggle.com/datasets/ulrikthygepedersen/online-chess-games)


