# Spotify Popularity Prediction 
## Introduction 

For our final project we worked on the [Spotify dataset](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks) from **Kaggle**. Our objective was to be able to predict the popularity of a song based on certain features from within the dataset. 

# Selection of Data

To start, we use the data.csv file which has **174389 samples** and **19 different features**. Our plan is to work on the features, acousticness, danceability, energy, instrumentalness, energy, liveness, loudness, speechiness, tempo, and valence listed from the dataset as predictors.

We decided to drop **non-numeric columns**: artists, id, name, and release date.  We have also cut down the original dataset to include only recent years (2016-2020), due to the observed difference in influence of features over time.
 
# Methods
**Tools**:
- Numpy, Pandas, Matplotlib, Seaborn 
- Scikit-learn
    - Models: KNeighborsClassifer, Logistic Regression, RandomForestClassifier, XGBRegressor, SVR
- Jupyter Notebook, Collab
# Results

Our team explored various different methods of classification algorithms and had varying results in the accuracy of predictions. 

With **KNNeighborsRegressor**, we achieved an **accuracy of 49.3 percent**. With Linear Regression, we achieved an accuracy of 44 percent. 

With **XGBRegressor**, we achieved an **accuracy of 55.26 percent**. 

With **SVR**, we achieved an **accuracy of 30 percent**. 

The best resulting accuracy that we achieved was **61 percent**. **59 percent** with the **RandomForestRegressor algorithm**, which is considered good by the general standard.

# Discussion
    
Our results indicate that our models do not sufficiently predict the popularity of a song based upon the predictor features. All of the models were below the recommended 60 percent threshold as discussed in our class, except for the **RandomForestRegressor algorithm** that gave us **61.59 percent**. This might imply that there is a difficulty in predicting the popularity of songs based simply upon the features in the dataset. 

One could deduce that there are other possible reasons for a song to become a hit than what the dataset contains. It could also be difficult in general to make that type of prediction, perhaps due to randomness. One thing we noticed was that certain features in the dataset seemed to vary significantly over time. For example, Energy seemed to increase over the years, while Acousticness seemed to decrease over the years. It is possible that these variations played some role in why our prediction accuracy was so low, but that is just our speculation. 

Another reason that could play into this was the lack of information about the artist. It is possible that the popularity of the artist performing a song could play a large role in how popular a song is, and this type of feature is outside the scope of our dataset. This is again pure speculation, but intuitively one can assume a correlation between artist popularity and song popularity.

# Summary

Our project was on projecting song popularity using the **Spotify Dataset 1921-2020, 160k+ Tracks** dataset from **Kaggle**. In this project we trained Machine Learning algorithms on features in the dataset: acousticness, danceability, energy, instrumentalness, energy, liveness, loudness, speechiness, tempo, and valence we our predictors. We trained 5 different algorithms, but we were not able to achieve a particularly accurate algorithm for making predictions. 

We speculate that this is because the dataset we used isn’t the best data to train off of in regards to popularity. Alternatively, song popularity could just be a difficult thing to predict.