# Introduction
Tennis is one of the oldest sports which garners a huge number of spectators.
Professional Tennis players come from diverse backgrounds and have different playing styles and specialties.
Andy Murray’s historic defeat of Novak Djokovic was the most-watched broadcast of the year 2013.
In the 2017 Stuttgart Open, 18-time grand slam champion Roger Federer lost to the world No. 302 player Tommy Haas on a grass court, which hadn’t happened since 2002.
There are a huge number of variables which define a tennis match, making it an interesting problem for machine learning.

# Goals
 - Predicting the winner of the tournament based on the players' previous performance.
 - Predict if the rank of the player will increase, decrease or remain the same after the match. Also, determining the rank 
   of the player after the match.
 - Predict the form of the players in the tournament after the matches.
 
# Data Preprocessing
 - Considered data from 1991 to 2018.
 - Dropped some data files because of missing features and a lot of missing values.
 - Data was labeled as winner and loser – randomly assigned “Player 1” as either winner or loser and “Player 2” to be the other person.
 - Data cleaning to replace the missing values.
 - Data transformation using normalization.
 
 # Feature Engineering
 - Created a new “form” feature for the both the players in the match.
 - Updated the form for each player after the match.
 - Update rule was as follows:
 - After the player has played 5 matches, new form is the number of matches the player has won in previous 5 matches.
 - Finally we calculate the form of each player in the tournament.
 - Created subset from our data frames and applied models to them.
 - Scale of the form: 0 – Worst form and 5 – Best Form
 
 
# Machine Learning
 - After data processing and feature selection, we applied various models on the data.
 - Data that we have is more suitable for betting predictions, when we removed these features, the accuracy we got remained the same
    as when we had included those features. Thus, betting data had no influence on our model.
 - While checking the variations in the rank, the rank points of the player before the match were used for learning and the rank 
    points that we obtained after the match was our prediction. 
 - Rank point prediction without previous rank knowledge.
 - Rank point prediction with previous rank knowledge.
 - Loser Rank variation is more complicated compared to Winner Rank.




# Results

 - Result 1:
  - Player Name: Wayne Ferreira
  - Best Model is Logistic Regression 
  - Training Accuracy: 91.428571428571 
  - Test Accuracy: 82.6086956521739 
  - Predicted Form: 2 


 - Result 2
  - Player Name: Rafael Nadal
  - Best Model is Random Forest 
  - Training Accuracy: 100.0 
  - Test Accuracy: 95.67567567567568 
  - Predicted Form: 4

# Conclusion
 - For the dataset we are using the models did achieve a good accuracy and made interesting predictions. 
 - Other than the features that we have considered, if we have dataset which considers the number of tournaments/matches 
   for each player, the number of matches a player had the day before the match,  the fitness of the player, the number of
   matches played in a similar environment, schedule of the player, etc. then we can make better predictions about the game.
   
   







