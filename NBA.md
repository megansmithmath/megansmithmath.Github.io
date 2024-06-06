  <img src="images/LinkedIn Banner.png?raw=true"/>

---

<h1 align="center">S Q L&nbsp;&nbsp;&nbsp;P R O J E C T</h1>

---
#### []()
[<img src="images/NBA0.png?raw=true"/>](https://public.tableau.com/views/NBA2023-24Season/Story1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link){:target="_blank"}
<br>
#### INTRODUCTION
Analytics is woven into nearly every industry but has always been deeply rooted in sports. In basketball, basic data collection, such as points, rebounds, and assists, dates back to the early 1900s. However, its influence rose with the emergence of advanced metrics by visionaries like coach Dean Oliver and basketball operations president Daryl Morey of the Philadelphia 76ers. Today, these sophisticated metrics and models not only optimize player performance but also shape game strategies and play a vital role in decision-making during critical moments of play. 

#### OBJECTIVE
I’m assuming a data analyst role for the National Basketball Association (NBA) for this project and have been tasked with the following main objectives:
1. Determine what position is the most efficient at shooting 3-pointers for each team.
2. Evaluate the potential for free-agent signings by examining total points, assists, and rebounds.
3. Identify players and positions that have the highest number of assists.
4. Identify general trends in the distribution of total points made by each player and position.

#### KEY FINDINGS
1. The Boston Celtics and Minnesota Timberwolves' centers had the highest 3-point percentages (40%), while those for the Charlotte Hornets and Cleveland Cavaliers had the lowest. 
2. A strong positive correlation exists between total points and assists, with point guards typically having more assists than centers. 
3. Domantas Sabonis, Nikola Jokić, and Luka Dončić excelled in points, assists, and rebounds, significantly outperforming peers in their positions.
4. The Atlanta Hawk’s power forwards scored only 24 points all season, compared to the median of 1,839, while their shooting guards scored 3,685 points, highlighting a need for better scoring balance.

#### THE DATA
The data for this project can be found on [Basketball Reference](https://www.basketball-reference.com/leagues/NBA_2024_totals.html){:target="_blank"}, a website housing current and historical NBA statistics. This dataset contains information on 573 players from 31 teams from the 2023-2024 season. It includes each player's position, the number of games started and played, the number of shots attempted and made, and the number of assists, steals, blocks, turnovers, etc. 

The data was downloaded using the “Get Table as CSV (for Excel)” option, which embedded the Comma Separated Values (CSV) file directly into the webpage. Then, I copied, pasted, and saved the data into a Microsoft Notepad file, which allowed me to seamlessly open the file in Microsoft Excel to avoid data loss. Then, I was able to upload the file into Tableau. The interactive components of this data story are posted on Tableau Public [here](https://public.tableau.com/views/NBA2023-24Season/Story1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link){:target="_blank"}.

#### DATA CLEANING
In the dataset, each NBA player had at least one row of statistics for the 2023-2024 season. However, 78 players were traded during the season and had multiple rows of statistics representing each team they played for. These players also had an additional row totaling their statistics for the season. Thirteen of these traded players started off playing one position and, once traded, switched positions. As a result, depending on the visualization, I filtered the rows differently to represent the data accurately. For example, when creating team visualizations, I filtered out the total statistic columns for traded players.

#### ANALYSIS: 3-POINT PERCENTAGES
Once the data was cleaned, the first task was to create a data visualization to determine the teams with the highest percentage of successful 3-point shots per position. Below is a heatmap displaying this data in Tableau. 
<img src="images/NBA1.png?raw=true"/>

The Charlotte Hornets (CHO) and the Cleveland Cavaliers (CLE) centers are highlighted in shades of orange. This indicates that the centers for these teams have very low 3-point percentages compared to other players and teams. While this is alarming, the centers on the team often play a significant role in defending against the opposing team’s larger players and typically play near the basket, thus having fewer opportunities for 3-point attempts. It is interesting to note that the centers for the Boston Celtics (BOS) and the Minnesota Timberwolves (MIN) have the highest 3-point percentages (40%), and these are two teams that made it to the final four in the playoffs. More analysis must be conducted to determine other factors contributing to these team's success.

#### ANALYSIS: POINTS, ASSISTS, AND REBOUNDS BY POSITION
Next, the NBA would like to know how different players performed this season to evaluate for potential free-agent signings. As a result, I examined all players' total points, total assists, and total rebounds using a bubble plot, as shown below. 
<img src="images/NBA2.png?raw=true"/>

To visually represent players’ roles on the court, the inner positions (centers and power forwards) are depicted in shades of orange, while the three remaining outer positions are in shades of blue and grey. The dashed linear regression line shows a strong positive correlation with a coefficient of determination, or R-squared value, of 0.725. This indicates that as the number of points scored increases, so does the number of assists. 

Looking deeper into this correlation reveals more insights about each position. The centers tend to remain below the dashed trend line, indicative of fewer assists, while point guards typically surpass the line, suggesting a higher number of assists. Additionally, the point guards tend to catch fewer rebounds, as indicated by their smaller dots compared to other players. This is expected since point guards set up plays and distribute the ball, whereas the centers focus on scoring close to the basket. 

Two centers are outliers: Domantas Sabonis of the Sacramento Kings and Nikola Jokić of the Denver Nuggets. These two centers are displayed high above the trendline in dark orange. Of all the centers this season, they have the highest number of assists and total points scored. Their respective circles are also larger, indicating they had more rebounds than other players. Also, Luka Dončić of the Dallas Mavericks stands out as the highest-scoring point guard with the highest number of assists in the NBA. This season, in early April, all three of these players made history by each recording 20+ triple-doubles in a single season, the first time this has happened among three players in one season. What an achievement! Tyrese Haliburton also stands out as the player with 752 assists, the highest in the NBA this season. 

#### ANALYSIS: PLAYER ASSISTS BY POSITION
Next, the NBA was interested in understanding the distribution of assists among players and positions. So, as shown below, I used a treemap to visualize this data.
<img src="images/NBA3.png?raw=true"/>

Each rectangle represents a player and is color-coded for the position they play. The larger the rectangle, the more assists that player had during the season, which allows for quick identification of top assist leaders. Overall, point guards are responsible for the majority of assists, which, as discussed earlier, makes sense given their role in directing the team's offense. LeBron James of the Los Angeles Lakers had 589 assists, the highest of all power forwards in the NBA. Centers Nikola Jokić and Domantas Sabonis have the highest number of assists (708 and 673, respectively), nearly double that of the next-highest center, Kelly Olynyk (347). 

#### ANALYSIS: TEAM POINTS BY PLAYERS
To quickly identify general trends in the distribution of total points made by each player, I created a quick stacked bar chart in Tableau, displayed below.
<img src="images/NBA4.png?raw=true"/>

While the visualization above houses a lot of information, it is clear that the Indiana Pacers (IND) and Boston Celtics (BOS) are the two highest-scoring teams in the NBA this season, and they advanced to the final four of the playoffs. However, the Dallas Mavericks (DAL) and Minnesota Timberwolves (MIN) made it to the final four but were not among the top five scoring teams. This implies that advancing to the playoffs is not reliant on the offensive game alone. The defensive game is just as important.

Additionally, each team typically relies on three to four primary scorers, with points evenly distributed among them. However, some teams have one scorer that significantly outshines the others, including Shai Gilgeous-Alexander of the Oklahoma City Thunder, Giannis Antetokounmpo of the Milwaukee Bucks, Luka Dončić of the Dallas Mavericks, and Jalen Brunson of the New York Knicks.

#### ANALYSIS: TEAM POINTS BY POSITION
To better understand the breakdown of total team points, I changed the bars in the stacked bar chart above from individual players to listed player positions, as shown below.
<img src="images/NBA5.png?raw=true"/>

Changing the stacked bar chart in this way makes it easier to see the overall composition of the types of players who are scoring the most. What stands out the most is the Atlanta Hawks (ATL) power forward’s lack of scoring power compared to other teams. Upon further exploration, the Hawks had only one power forward listed on their roster, Mouhamed Gueye. This rookie had a tough season of injuries. After being diagnosed with a stress fracture in November, he came back to play four months later in the NBA G League (the NBA’s official minor league) and then later suffered an ulnar collateral ligament (UCL) injury. Late in the regular NBA season, he was able to play in the last handful of games for the Hawks and brought in 24 points throughout the season. Understandably, other players on the team needed to fill this void. Jalen Johnson and De’Andre Hunter stepped up and played most of the season as power forwards despite being listed as small forwards on the team roster. According to position estimates found here, Johnson spent 94% of the season as a power forward. In comparison, Hunter played 67% of games in the same position. Together, they scored 1,787 points for the season, close to the NBA’s median of 1,839 points for power forwards. Although not uncommon, this shifting in positions also may explain why the Hawks’ listed shooting guards scored an impressive 3,685 points, 1,789 more than the league median, nearly surpassing the Toronto Raptors’ shooting guards, who secured 3,700 points. Overall, despite this adversity, the Atlanta Hawks were able to make adjustments that ultimately allowed them to clinch a spot among the NBA’s top five highest-scoring teams this season.

#### KEY FINDINGS AND RECOMMENDATIONS
1. Centers from the Boston Celtics and Minnesota Timberwolves achieved the highest 3-point shooting success rates of the season at 40%, and centers from the Charlotte Hornets and Cleveland Cavaliers had the lowest. Teams with low 3-point shooting success should consider investing in targeted training to improve this part of the game or implement offensive plays that will position centers and power forwards closer to the basket where they are most effective so they can continue to rely on other outer positions for the 3-pointers.
2. Since there is a strong positive linear correlation between total points and assists, with point guards leading in assists, developing plays across all positions that introduce offensive plays that create more assist opportunities for other players may enhance overall team performance
3. Teams should further analyze the play styles and training regimes of stand-out players like Domantas Sabonis, Nikola Jokić, and Luka Dončić, who excel in multiple areas. Implementing aspects of their individual training and play structure can potentially strengthen other key players and teams.
4. Teams like the Atlanta Hawks seemed to have benefited from adjusting player positions to balance the scoring load. However, adjusting the offensive strategy alone may not drastically improve certain teams. Therefore, targeting recruits and careful draft selections may be the next steps for some struggling teams.
<br><br>
 
---
<br><br>
  <p align="center"><a href="https://megansmithmath.github.io/"><img src="images/Home Button.png?raw=true"/>
  
