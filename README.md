# Cricket-Player-Performance-Prediction
<img src="https://github.com/Vaibhavnaudiyal92/Cricket-Player-Performance-Prediction/blob/master/wp1862738.jpg?raw=true"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" />
# Introduction
Cricket is a sport played by two teams with each side having eleven players. Each team is a right blend of batsmen, bowlers and allrounders. The batsmen’s role is to score maximum runs possible and the bowlers have to take maximum wickets and restrict the other team from scoring runs at the same time. Allrounders are the players who can both bat and bowl and they contribute by scoring runs and taking wickets. Each player contributes towards the overall performance of the team by giving his best performance in each match. Each player’s performance varies with factors like the team he is playing against and the ground at which the match is being played. It is important to select the right players that can perform the best in each match. The performance of a player also depends on several factors like his current form, his performance against a particular team, his performance at a particular venue etc. The team management, the coach and the captain analyze each player’s characteristics, abilities and past stats to select the best playing XI for a given match. In other words, they try to predict the players’ performance for each match. In this project, we predict the players’ performance in One Day International (ODI) matches by analyzing their characteristics and stats using supervised machine learning techniques. For this, we predict batsmen’s and bowlers’ performance separately as how many runs will a batsman score and how many wickets will a bowler take in a particular match.
# Overview
This project has 4 main parts:
1. Batsman Data Engineering
2. Bowler Data Engineering
3. Batsman Prediction
4. Bowler Prediction

Each of the part has been implemented in seperate notebooks. First two are for data engineering and other two are for model implementation and predictions.

# Acknowledgements
* The following project is based on a research paper contributed by **Kalpdrum Passi and Niravkumar Pandey**
**Department of Mathematics and Computer Science**
**Laurentian University, Sudbury, Canada**

* The following dataset in scraped from espncricinfo.com

# Approach
The stats of the players such as average, strike rate etc. are
not available directly for each game, we calculated these attributes from the innings by innings
list using aggregate functions and mathematical formulae. The formulaes and values are referenced from the research paper. These attributes are generally used to
measure a player’s performance. They are as follows: 
### Batting Attributes
1. No. of Innings: 
The number of innings in which the batsman has batted till the day of the match.
This attribute signifies the experience of the batsman. The more innings the batsman has played,
the more experienced the player is.

2. Batting Average: 
Batting average commonly referred to as average is the average number of runs
scored per innings. This attribute indicates the run scoring capability of the player.
**Average = Runs Scored / Number of times dismissed**

3. Strike Rate (SR): 
Strike rate is the average number of runs scored per 100 balls faced. In limited
overs cricket, it is important to score runs at a fast pace. More runs scored at a slow pace is rather
harmful to the team as they have a limited number of overs. This attribute indicates how quickly
the batsman can score runs.
**Strike Rate: (Runs Scored / Balls Faced) * 100**

4. Centuries: 
Number of innings in which the batsman scored more than 100 runs. This attribute
indicates the capability of the player to play longer innings and score more runs.

5. Fifties: 
Number of innings in which the batsman scored more than 50 (and less than 100)
runs.This attribute indicates the capability of the player to play longer innings and score more runs.

6. Zeros: 
Number of innings in which the batsman was dismissed without scoring a single run. This
attribute shows how many times the batsman failed to score runs, hence this being a negative
factor, was impacts the batsman’s prediction negatively. 


### Bowling Attributes
1. No. of Innings:
The number of innings in which the bowler bowled at least one ball. It represents
the bowling experience of a player. The more innings the player has played, the more experienced
the player is.
Overs: The number of overs bowled by a bowler.This attribute also indicates the experience
of the bowler. The more overs the bowler has bowled, the more experienced the bowler
is.
2. Bowling Average:
Bowling average is the number of runs conceded by a bowler per
wicket taken. This attribute indicates the capabilities of the bowler to restrict the batsmen
from scoring runs and taking wickets at the same time. Lower values of bowling average
indicate more capabilities.
3. Bowling Average:
**Number of runs conceded / Number of wickets taken**
4. Bowling Strike Rate:
Bowling strike rate is the number of balls bowled per wicket taken.
This attribute indicates the wicket taking capability of the bowler. Lower values mean
that the bowler is capable of taking wickets quickly.
5. Strike Rate:
**Number of balls bowled / Number of wickets taken**
6. Four/Five Wicket Haul:
Number of innings in which the bowler has taken more than four
wickets. This attribute indicates the capability of the bowler to take more wickets in an
innings. Higher the value, more capable the player. 

# Tasks Done:
### 1. Data Pre-processing
* Removing unnecessary features
* Feature Engineering
* Encoding categorical features
* Filling missing values

### 2. Model implementations
* Implementing supervised machine learning models
* Calculating Accuracy score, Precision score, F1-score and Recall score of the implemented models

### NOTE
We have also used SMOTE for oversampling

# Conclusion
## Batsman Predictions
We were achieved highest accuracy of 0.99 with Random Forest and lowest of 0.44 with Naive Baye's 

## Bowlers Predictions
We were achieved highest accuracy of 0.99 with Random Forest and lowest of 0.68 with Naive Baye's
