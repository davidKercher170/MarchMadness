Data Extraction and Initialization:

Team List Creation: The code starts by reading a file (2023.txt) containing game results. It extracts team names from each line and maintains a list of unique teams.
Adjacency Matrix Setup: An adjacency matrix n is initialized, where each element n[i][j] will represent the competitive strength or result between team i and team j.

Matrix Population:

The code parses the game results again to populate the adjacency matrix. For each game:
It calculates a value based on the score difference between the two teams.
If one team wins, the matrix is updated with a value derived from the score ratio, with a maximum value constraint to ensure reasonable weighting.

Degree Centrality:

The function 'degree_centrality' calculates the degree centrality of each team by summing the values in each row of the matrix.
Teams are sorted based on their degree centrality scores.

Power Series Iteration Centrality:

Another function 'pr' computes the PageRank-like centrality using iterative methods.
It constructs a probability matrix from the adjacency matrix and normalizes it.
Iterative power series updates are performed to calculate the centrality scores, with convergence achieved after a fixed number of iterations.
Teams are then ranked based on these centrality scores.

The Teams were ranked by PageRank Centrality as follows, excluding Division 2 Programs:

Rank: Team (AP Poll Ranking)
1: "Kansas" (4)
2: "Purdue" (3)
3: "Tennessee" (20)
4: "Alabama" (1)
5: "Texas" (5)
6: "UCLA" (7)
7: "Kansas St." (15)
8: "Houston" (2)
9: "Baylor" (11)
10: "Texas A&M" (17)
11: "UConn" (10)
12: "Saint Mary's (CA)" (18)
13: "Duke" (12)
14: "Iowa St." (Unranked)
15: "Arizona" (8)
16: "Marquette" (6)
17: "Indiana" (21)
18: "Kentucky" (Unranked)
19: "San Diego St." (18)
20: "Miami (FL)" (16)
21: "Arkansas" (Unranked)
22: "Boise St." (Unranked)
23: "VCU" (Unranked)
24: "Maryland" (Unranked)
25: "Virginia" (14)

Suprisingly, the results from PageRank (with a typical 0.85 alpha) ranks teams similarly to the Final AP Poll Rankings for the Season.
In the future, it would be interesting to incorporate more information into the matrix valutations such as home/away team, injuries, trap games, talent rankings, etc.
It would also be interesting to create game outcome probabilities based on the direct interaction between neighbor teams (we could extend this to neighbors of neighbors).
