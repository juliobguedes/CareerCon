# CareerCon

CareerCon is a Kaggle competition that happens every year with recruitment purposes. I've participated in CareerCon 2019, and this repository contains my code for the submissions. For more information about it, please check the [official competition page](https://www.kaggle.com/c/career-con-2019/overview).

During the competition I had around 69% of accuracy, being placed at 753 in the Public Leaderboard. At the end of the competition, I had around 64% of accuracy, being placed at 108 in the Private Leaderboard - Top 8%.

## The Problem

The problem to be solved in 2019 was "How to identify which kind of floor surface is a small robot driving over?".

## The Data

The data was collected from IMU Sensors, generating a tabular dataset with acceleration, orientation and velocity in all 3 axis. To understand more about the specifics of the problem, knowledge about accelerometers and gyroscopes was needed.

The data a time series of measurements for each small robot, and for each robot we had to predict the floor surface it was passing over. An important thing to mention was that the data was imbalanced, and not everyone was well aware about that.

## My Solutions

My solutions were very simple: I grouped the data based on the robots id, generating another dataset over which I was going to predict the floor surface, using the mean, amplitude and other variables like those, that could be generated from the series. After that, I balanced the dataset, and then trained my models.

Overall, I've used Machine Learning algorithms such as Decision Trees and boosting algorithms (AdaBoost and XGBoost). When I saw the other competitors using Random forests, I tried using it and one of the submissions got me my public leaderboard score. Even getting that high score with Random Forests, I did not trust enough to select them as my models for the private leaderboard scoring, keeping a XGBoost and a Decision Tree selected.

After the results were released, I had almost the same accuracy in the private leaderboard as in the public leaderboard, but I had gone more than 600 positions up, reaching 108 (Top 8%).

&copy; Júlio Guedes