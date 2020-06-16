# MLB Pitch Predictions

### By: Jeff Lindberg

## Executive Summary
The goal of this project was to predict pitches based on game situations using machine learning alogorithms. Pitch types were broken down into three classes; fastball, offspeed, and breaking. The best model was a Random Forest algorithm. This also allowed me to determine the most import features used to predict the pitches. These features can be used by teams when evaluating pitchers and creating scouting reports.

## Contents
1. [Introduction](#introduction)
    - [Problem Statement](#problem_statement)
    - [Dataset](#dataset)
2. [Analysis](#analysis)
    - [Data Cleaning](#data_cleaning)
    - [Exploratory Analysis](#exploratory_analysis)
    - [Modeling](#modeling)

## Introduction <a name="introduction"></a>

### Problem Statement <a name="problem_statement"></a>
Knowing which pitch is coming can give a hitter a massive advantage over a pitcher. Can we use data to accurately predict the next pitch and give hitter's the best chance to succeed?

### Dataset <a name="dataset"></a>
The analysis is based on data scraped from Statcast, (https://baseballsavant.mlb.com/), using the pybaseball scraper. It includes all pitches from 2018-2019. The observations include all the metrics recorded by Trackman for each pitch. The size of my initial dataset was (1474090, 91).

## Analysis <a name="analysis"></a>

### Data Cleaning <a name="data_cleaning"></a>
The inital data set was fairly clean but I still had to drop some outliers and null values. I dropped unnecessary columns and dropped a few pitch types that distorted the data. Then I binned the remaining pitches into three classes, offspeed, breaking, and fastball variations. After all the cleaning, the size of my dataset was (1424311, 38).

### Exploratory Analysis <a name="exploratory_analysis"></a>
I used exploratory analysis to see the relationship between my features and targets. This helped me drop some unnecessary features that were not continuous variables. I also created a few features that I believed more accurately described the game situation, such as ball/strike count, previous pitch type, and platoon effect. 

### Modeling <a name="modeling"></a>
The majority of the modeling in this project came from sklearn. I used Logistic Regression, Multinomial Naive Bayes, Random Forest, XG Boost, AdaBoost, and K-Nearest Neighbors.