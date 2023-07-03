# Predicting Formula 1 Tracks using Machine Learning Algorithms only by telemetry

## Introduction
One day I was watching a Formula 1 race and I thought if I can predict which track is just by telemetry, ignoring car speed, track length and lap time. And that's what this project is about.

## Data
The data was collected from the [Ergast Developer API](http://ergast.com/mrd/) and [Fast F1](https://docs.fastf1.dev/) that is a Python Lib. With this lib we can get some telemetry from the car, but only trivial ones like speed, rpm, throttle, lap time, etc. But I used only the percentage of throttle and the gear. But even with that, I still have a problem. The data is a time series for each feature and I want to eliminate that to remove the time variable. So I just used the mean of each feature for each sector of the track. So I have 3 sectors for each track and 2 features(throttle percentage and gear) for each sector. So I have __6 features__ for each track. On *__get_info.ipynb__* you can see the process to extract the data from the lib and make it to a csv file.

## EDA

Before go straight to the models and see the results, is good to make an Exploratory Data Analysis and I made a simple one on *__EDA.ipynb__*.

## Models
I used __Decision Tree__ and __SVM__ to predict the tracks. I used the Decision Tree because it's a simple model and it's easy to interpret. And I used SVM because it's a powerful model and it's good to compare with the Decision Tree. I used the GridSearchCV to find the best parameters for each model. The results are on *__formula.ipynb__*. I didn't use Neural Network because I found a particularity on the data that I understand there is no need to use.


Hope you enjoy this!

