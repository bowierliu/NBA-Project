# NBA Dataset Analysis

## Project Motivation

The NBA dataset contains statistics of players from 1982 to 2021, providing insights into player performance, team dynamics, and the evolution of the game over the years. This project aims to explore key trends such as the increase in three-point attempts, analyze player efficiency, and identify the most efficient players in NBA history.

## Libraries Used

- **Pandas**: For data manipulation.
- **Matplotlib**: For data visualization.
- **NumPy**: For numerical operations.

## Data Overview

The dataset contains the following columns:
- **season**: Year of the season.
- **player**: Name of the player.
- **pos**: Position of the player (e.g., C, PF, SG, etc.).
- **age**: Age of the player.
- **team_id**: The team the player played for.
- **g**: Games played.
- **gs**: Games started.
- **mp_per_g**: Minutes played per game.
- **fg3a_per_g**: Three-point attempts per game.
- **fg2a_per_g**: Two-point attempts per game.
- **per**: Player Efficiency Rating.
- ... (Additional statistical features such as rebounds, assists, blocks, and more).

### Sample Data

| Unnamed: 0 | season | player              | pos | age | team_id | g  | gs   | mp_per_g | fg3a_per_g | ... |
|------------|--------|---------------------|-----|-----|---------|----|------|----------|------------|-----|
| 0          | 1982   | Kareem Abdul-Jabbar | C   | 34  | LAL     | 76 | 76.0 | 35.2     | 9.9        | ... |
| 1          | 1982   | Alvan Adams          | C   | 27  | PHO     | 79 | 75.0 | 30.3     | 6.4        | ... |
| 2          | 1982   | Mark Aguirre         | SF  | 22  | DAL     | 51 | 20.0 | 28.8     | 7.5        | ... |
| 3          | 1982   | Danny Ainge          | SG  | 22  | BOS     | 53 | 1.0  | 10.6     | 1.5        | ... |

## Key Findings

### Three Pointers Attempted Over the Years

We observed a significant increase in three-point attempts over the decades. For instance:
- From 1982 to 1990, only 842 three-pointers were attempted.
- From 2010 to 2019, 9253 three-pointers were attempted, showing a drastic increase in the volume of shots taken from beyond the arc.

#### Code Snippet: Visualization of 2's and 3's Attempts Over the Years

```python
plt.plot(nba_season3['season'], nba_season3['fg3a_per_g'], label = "3 pt")
plt.plot(nba_season2['season'], nba_season2['fg2a_per_g'], label = "2 pt")
plt.title("2's and 3's Attempted over the Seasons")
plt.xlabel("Season")
plt.ylabel("Total 2 and 3 Pointers Attempted")
plt.legend()
plt.show()
