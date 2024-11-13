# Cricket Data Analysis and Interpretability of Player of the Match Awards

## Overview
This project explores cricket analytics by analyzing detailed metrics from Test matches, One Day Internationals (ODIs), and T20 formats, aiming to interpret 'Player of the Match' awards through statistical and machine learning models. The project highlights the importance of data-driven insights in cricket, providing context and interpretability to player performances.

## Motivation
Cricket is a sport that demands skill, strategy, and precision. With the evolution of the game and an increasing reliance on data-driven decision-making, this project delves into the nuances of cricket statistics to extract insights beyond the scoreboard. The analysis focuses on discovering patterns that distinguish top performers and understanding factors contributing to Player of the Match awards.

## Literature Review
This project draws from various resources in cricket data analysis:
1. **Cricket Data Analysis and Score Prediction** by Sagidur Rahman (Kaggle)
2. **Data Analytics in the Game of Cricket: A Novel Paradigm** by Varad Vishwarupe et al.
3. **CricViz**: a website offering cricket data and analytics
4. **End-to-End Cricket Data Analytics Project** by codebasics (YouTube)

These resources inspired the methods and models applied to derive insights into player and team performances.

## Data Sources
Two primary datasets were used:
- **Primary Dataset (Kaggle)**: Contains batting and bowling statistics for ODIs, Tests, and T20s, including runs, wickets, strike rates, and milestones.
- **Secondary Dataset (ESPN)**: Focuses on player achievements, including Player of the Match awards segmented by format.

An additional self-constructed table with team acronyms was created to ensure data consistency and accuracy.

## Data Manipulation and Cleaning
The data underwent extensive cleaning and manipulation:
1. **Handling Duplicate Names**: Players with identical names were distinguished based on career seniority.
2. **Segmentation and Deduplication**: Player names were segmented, and a team acronym table was constructed for easy identification.
3. **Merging**: Batting and bowling data were consolidated and merged with ESPN records for validation.
4. **Combining Datasets**: Primary and secondary datasets were merged to form a balanced dataset for modeling Player of the Match awards, ensuring both award-winning and non-award-winning players were included.

## Visualizations
Key visualizations were created to capture patterns and trends:
- **Correlation Matrix**: Shows relationships between metrics like runs, wickets, and match counts.
- **Player Analysis**: Includes metrics for longest careers, top scorers, and players with the most wickets, with breakdowns for centuries and half-centuries.
- **Team Analysis**: Aggregates runs and wickets per team, with visualizations like raincloud and world plots.
- **Skill Plots**: Radar plots show skill profiles for players with the highest match counts across multiple metrics.

## Data Analysis
### Regression Analysis
A regression using Ordinary Least Squares (OLS) explored the relationship between players' highest scores and their career start year, revealing significant changes over time.

### Clustering
KMeans clustering was applied to identify patterns within player data:
- **Best Clustering**: Achieved with 3 clusters (Silhouette Score: 0.77), grouping players into categories of good batsmen, good bowlers, and intermediate players based on runs and balls faced.

### Player of the Match Prediction
To predict Player of the Match awards, we used:
- **Model Selection**: Random Forest and Gradient Boosting Regressors were tested, with Gradient Boosting chosen for its 91.7% accuracy.
- **Feature Importance**: The permutation feature importance identified `Inns_bat` and `Mat` as the most significant predictors of awards.
- **SHAP Analysis**: SHAP values provided insights into model predictions, identifying feature contributions to specific predictions and enhancing model interpretability.

## Conclusion
This project demonstrated that data-driven models can effectively interpret and predict Player of the Match awards. SHAP analysis added interpretability, illustrating how specific features influenced player recognition. The analysis advances cricket analytics by offering a data-centric view of player contributions, helping to contextualize exceptional performances.


## References
1. **Sagidur Rahman**: [Cricket Data Analysis and Score Prediction](https://www.kaggle.com/code/sazid28/cricket-data-analysis-and-score-prediction) (Kaggle, 2018)
2. **Varad Vishwarupe et al.**: *Data Analytics in the Game of Cricket: A Novel Paradigm*, *Journal of Sports Sciences*, 2023
3. **CricViz**: [CricViz Website](https://cricviz.com)
4. **Codebasics**: *End-to-End Cricket Data Analytics Project*, [YouTube](https://m.youtube.com/watch?v=4QkYy1wANXA)
