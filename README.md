 # Social-lstm-for-predicting-player-trajectories-in-soccer

Traditional methods of predicting outcomes of sports like soccer rely upon averaged statistics like expected goal value and player ratings. While these methods are sufficient to describe the general trend, they are unable to capture the dynamics of human interaction that occur as part of the sport. In this paper, we develop and explore approaches to create representations of the gameplay which are able to predict the trajectory of players. Convential sequence prediction models are insufficient for trajectory prediction because it involves player interactions in the same time frame as well. Social-LSTM can be particularly useful in such cases and can help in learning player behavior. It has been applied to analyze pedestrian behavior in crowded environment but this is first time it has been applied to sports domain. We present our results on the data provided by STATS (https://www.stats.com/).

![Alt text](sampleCase.png?raw=true "Sample Scenario")

Above figure shows a sample scenario from a real match. Atletico Madrid (red) is attacking and Real Madrid (white) is defending in this play. The two central defenders have the responsibility of closing the opposing attacker Torres (circled). Also, Correa just moved into an open space to receive the pass from Oliver. Marcelo on left flank, meanwhile, is following a trajectory which makes sure Juanfran and Griezmann don't have an opportunity to run for a through ball. Such decisions are intuitive for a player but very hard for a programmer to model. They are observed very frequently in the game and are an important aspect of good strategies. We aim to learn these behaviors from data. Achieving this goal will allow us to gain insights into the rules that players inherently model through experience, and thus allow us to predict their motion and form strategies accordingly. 

![Alt text](results.png?raw=true "Sample Scenario")

Above figure shows the results on a sample sequence. The trajectories of the players are observed for a few time steps (solid lines). Predicted trajectories are then plotted (dashed lines) as a continuation on the same chart. As can be seen in the figure, Defenders D1 and D2 are initially closing down the attacker A1 in the observed part of the sequence. But, as soon as the attacker A1 sees an open space, it changes the path and tries to occupy that space. This however alerts the defender D2 and as such he also follows the attacker A1 to close him down. Meanwhile, defender D1 who was earlier covering A1 now finds another attacker A2 in its neighborhood. As such, D2
changes path to close that defender down.

* The approach was inspired by the work of Anirudh et. al. on 'Social Attention : Modeling Attention in Human Crowds.'. 
* Please contact me at jagjeets@andrew.cmu.edu to get more details
