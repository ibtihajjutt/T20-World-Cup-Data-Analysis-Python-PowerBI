# T20-World-Cup-Data-Analysis-Python-PowerBI
Overview
This project aims to analyze match results and player performances from the T20 World Cup. By preprocessing the data and creating an interactive dashboard in Power BI, we provide insights into the tournament's trends, individual performances, and overall team statistics.

1. Data Preprocessing
Processing Match Results
Data Source: Match results are read from a JSON file.
Data Structure: The data is converted into a DataFrame, with key columns renamed for clarity.
Match ID Mapping: A dictionary maps unique team matchups to their corresponding match IDs, linking the match data with other datasets.
Export: The cleaned match results are saved to a CSV file for further analysis.

Processing Batting Summary
Data Cleaning: Special characters in player names are removed for consistency.
Export: The processed batting summary is exported to a CSV file.

Processing Bowling Summary
Data Source: Bowling summary data is loaded from a JSON file.
Data Structure: This data is converted into a DataFrame, with match IDs linked using the same dictionary.
Export: The cleaned bowling data is saved to a CSV file for analysis.

Processing Player Information
Data Source: Player information is compiled, detailing player names and teams.
Data Cleaning: Unusual characters in player names are cleaned.
Export: The player information is saved to a CSV file, excluding images.

3. Data Model
The data model comprises several tables with established relationships, supporting comprehensive analysis:

dim_match_summary: Contains match details, including ground, margin, date, and stage. It serves as the primary link to batting and bowling summaries.
dim_players: Stores player information, linking to batting and bowling statistics.
fact_batting_summary: Includes batting data, connecting performances to matches and players.
fact_bowling_summary: Contains bowling performance data, linked to matches and players.
Key_Measures: A calculated measure (e.g., average balls faced) for visualizations and analysis.
Relationships
The dim_match_summary table connects to fact_batting_summary and fact_bowling_summary via match_id.
The dim_players table connects to both summaries through batsmanName and bowlerName.
3. Dashboard Development in Power BI
With the cleaned data, we develop an interactive dashboard in Power BI that includes:

Match Results: Visualizations of match outcomes, scores, and team performances.
Top Batsmen and Bowlers: Rankings and statistics for top players based on runs and wickets.
Player Profiles: Individual player statistics across matches.
Win/Loss Trends: Analysis of match results trends over time.
The dashboard enables users to filter data and interact with visualizations for a comprehensive view of the T20 World Cup.

Conclusion
This project effectively transforms raw cricket data into actionable insights through preprocessing and the development of an engaging Power BI dashboard. The insights derived from match results, player performances, and tournament trends can help stakeholders make informed decisions.

