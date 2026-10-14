# IPL Dream11 Predictor — ETL Pipeline

An IPL fantasy-cricket analytics project that transforms ball-by-ball match data into player-level performance statistics to support fantasy team selection and player performance analysis.

The project demonstrates an ETL (Extract, Transform, Load) workflow using Python, Pandas, SQLAlchemy, and Neon PostgreSQL.

## Project Overview

Fantasy cricket team selection involves analysing player performance, batting contributions, and match statistics. This project processes historical IPL delivery-level data into structured player statistics that can be used for fantasy-point analysis and future prediction models.

## Objectives

- Extract and process historical IPL match data.
- Transform ball-by-ball records into player-level batting statistics.
- Calculate performance metrics such as runs, fours, sixes, and balls faced.
- Calculate an initial batting performance score for analysis.
- Load the transformed dataset into a Neon PostgreSQL database.
- Prepare structured data for future fantasy-point prediction and player ranking.

## Tech Stack

- **Python** — data processing
- **Pandas** — data cleaning, transformation, and aggregation
- **SQLAlchemy** — database connectivity
- **PostgreSQL** — structured data storage
- **Neon** — cloud-hosted PostgreSQL database
- **Git & GitHub** — version control

## ETL Workflow

1. **Extract:** Load historical IPL match and ball-by-ball data.
2. **Transform:** Group delivery records by match, season, batting team, and batter.
3. **Calculate:** Generate player statistics, including runs, fours, sixes, and balls faced.
4. **Score:** Calculate an initial batting performance score for exploratory analysis.
5. **Load:** Upload the transformed DataFrame to Neon PostgreSQL using Pandas `to_sql()`.
6. **Validate:** Check the database table and row count to confirm that the data was uploaded.

## Player Statistics

The transformed table contains metrics such as:

| Column | Description |
|---|---|
| `match_id` | Unique match identifier |
| `batter` | Batter's name |
| `score` | Dream11 score |


## Database

The transformed player-level statistics are stored in a PostgreSQL table named `player_batting_stats` in Neon.

The database layer makes the processed data available for SQL queries and future analytics.

## Example Use Cases

- Compare player batting performances across matches.
- Identify high-scoring batters.
- Analyse boundaries and batting contributions.
- Build player rankings from historical performance.
- Extend the pipeline to support fantasy-point prediction.

## Future Improvements

- Add bowling and fielding statistics.
- Implement the applicable fantasy-cricket scoring rules.
- Include recent player form and match-level features.
- Incorporate playing XI, venue, and opposition information.
- Build a model to estimate future fantasy points.
- Develop a dashboard for player comparison and fantasy team selection.
- Automate ETL execution and data validation.

## Project Status

**In development.** The current version focuses on transforming IPL ball-by-ball data into player-level batting statistics and storing the results in PostgreSQL. A complete fantasy-point prediction system requires additional features and validation.


## Disclaimer

This is an independent educational and portfolio project. It is not affiliated with or endorsed by Dream11 or the IPL. The initial batting score is not an official fantasy scoring metric.
