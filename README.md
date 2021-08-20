# 1. Business Problem 
## 1.1 Problem Description 
Netflix is all about connecting people to the movies they love. To help customers find those movies, they developed world-class movie recommendation system: CinematchSM. Its job is to predict whether someone will enjoy a movie based on how much they liked or disliked other movies. Netflix use those predictions to make personal movie recommendations based on each customer’s unique tastes. And while Cinematch is doing pretty well, it can always be made better.

Now there are a lot of interesting alternative approaches to how Cinematch works that netflix haven’t tried. Some are described in the literature, some aren’t. We’re curious whether any of these can beat Cinematch by making better predictions. Because, frankly, if there is a much better approach it could make a big difference to our customers and our business.

## 1.2 Problem Statement 
Netflix provided a lot of anonymous rating data, and a prediction accuracy bar that is 10% better than what Cinematch can do on the same training data set. (Accuracy is a measurement of how closely predicted ratings of movies match subsequent actual ratings.)

## 1.3 Sources 
https://www.kaggle.com/netflix-inc/netflix-prize-data
## 1.4 Real world/Business Objectives and constraints 
Objectives:

Predict the rating that a user would give to a movie that he ahs not yet rated.
Minimize the difference between predicted and actual rating (RMSE and MAPE)
Constraints:

Some form of interpretability.
# 2. Machine Learning Problem 
## 2.1 Data 
### 2.1.1 Data Overview 
Data files :

combined_data_1.txt
combined_data_2.txt
combined_data_3.txt
combined_data_4.txt
movie_titles.csv
  
The first line of each file [combined_data_1.txt, combined_data_2.txt, combined_data_3.txt, combined_data_4.txt] contains the movie id followed by a colon. Each subsequent line in the file corresponds to a rating from a customer and its date in the following format:

CustomerID,Rating,Date


MovieIDs range from 1 to 17770 sequentially.
CustomerIDs range from 1 to 2649429, with gaps. There are 480189 users.
Ratings are on a five star (integral) scale from 1 to 5.
Dates have the format YYYY-MM-DD.

## 2.2 Mapping the real world problem to a Machine Learning Problem 
### 2.2.1 Type of Machine Learning Problem 
For a given movie and user we need to predict the rating would be given by him/her to the movie. 
The given problem is a Recommendation problem 
It can also seen as a Regression problem 
### 2.2.2 Performance metric 
Mean Absolute Percentage Error: https://en.wikipedia.org/wiki/Mean_absolute_percentage_error
Root Mean Square Error: https://en.wikipedia.org/wiki/Root-mean-square_deviation
### 2.2.3 Machine Learning Objective and Constraints 
Minimize RMSE.
Try to provide some interpretability.

# 3 Final Results
<p style = 'color: black'> Root Mean Squared Error </p>
<pre>
svd               1.0726046873826458
knn_bsl_u         1.0726493739667242
knn_bsl_m          1.072758832653683
svdpp             1.0728491944183447
bsl_algo          1.0730330260516174
xgb_knn_bsl_mu    1.0753229281412784
xgb_all_models     1.075480663561971
first_algo        1.0761851474385373
xgb_bsl           1.0763419061709816
xgb_final         1.0763580984894978
xgb_knn_bsl       1.0763602465199797

</pre>
