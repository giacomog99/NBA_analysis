# NBA_analysis

In this repository there are 2 projects I’ve been worked for on in recent months:


DASHOBARD
This project involves the visualization of the team stats about NBA regular season 2021-2022, focusing on points and field goals, with additional insights into other statistics.

Data Collection:
	1. Shot Information: Initially, I scraped all shot data using Python and the nba.api.

	2. Additional Stats: To gather additional statistics, I utilized a dataset from Kaggle (https://www.kaggle.com/datasets/nathanlauga/nba-games?resource=download&select=games_details.csv). 
 However, this dataset was incomplete as it lacked information about wins/losses and there wasn’t an "opponent" field. To address this, I scraped another dataset from nba.api, which provided complete stats. I merged this dataset with the Kaggle 	dataset using Microsoft Excel.
 
	3. Lookup Table: The last data that I needed is a lookup table containing team’s record and the info about if a team achieved the playoffs. I created this table by extracting data from the basketball-reference.com website (https://www.basketball-reference.com/leagues/NBA_2022.html).


Visualization:
I created a dashboard using Tableau Public, which can be accessed through the following link: https://public.tableau.com/views/NBA_stats_202122/Dashboard?:language=it-IT&:display_count=n&:origin=viz_share_link.

Note:
This is my first Tableau dashboard, as I typically work with Power BI. Any advice you may have would be greatly appreciated.



WIN PREDICTION AND INTERPRETATION WITH XAI
This project involves the win prediction using AI models and studying the behavior of predictors. Detailed information can be found in the document “NBA_win_pred_summary” in which I describe the AI model that I’ve chosen, the importance of using Explainable AI visualizations and the obtained results.

For this project I’ve created a new dataset “NBA_data_XAI.csv” based on the Kaggle’s dataset “games_details.csv”, but for each game I’ve grouped information by team rather than by player and I’ve added some advanced analytic including 2 customized by me:

SpeedRATING: This stat classified way of play for each team. I’ve taken 4 variables which are indices of high speed way of play (POSS, FGA, STL and TO) and 3 variables which are indices of low speed way of play (REB, %FGM, BLK). I’ve ordered those variables into quartiles and then I’ve subtracted the sum of the quartiles about the high speed variables with sum of the quartiles about the slow speed variables. So if a team has a high SpeedRATING means that it’s a high offensive intensity team, with lots of possession and lots of shots taken. On the contrary, if a team has a low SpeedRATING means that it’s a high defensive intensity team, with lots of rebounds and block and with a few but well organized shots.

LEADERSHIP: This stat is the difference between avgPTS and MEDIAN by team for each game. This is useful in order to understand if mostly points are made by the team’s best players, so avgPTS is higher than MEDIAN (in this case there is a Star-leaded team), or if the points are better distributed among the players, so avgPTS is the same or lower than MEDIAN (in this case there is a Team-leaded team).
