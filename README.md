# Does a Consistent Lineup Matter for Team Success?
This article is part of College Gym News's [Data Deep Dive](https://collegegymnews.com/category/data/) series. [College Gym News](https://collegegymnews.com/) is "a one-stop-shop for college gymnastics news" and provides a wide-variety of coverage from more than 30 contributors. 

The full article can be found [here](https://collegegymnews.com/2024/01/22/does-a-consistent-lineup-matter-for-team-success/). Statistical analysis and writing was completed by Bailey Sutton with additional writing contributions by Emma Hammerstrom. 

## Navigation
- **:computer: code:** Files for scraping data from [Road to Nationals (RTN)](https://roadtonationals.com/results/index.php) and statistical analysis
- **:file_folder: data:** Individual results and event ranking data files
- **:bar_chart: plots:** Line charts

## Methods
This project adapts [FiveThirtyEight’s](https://projects.fivethirtyeight.com/epl-consistency-2023/) consistency calculations for Premier League teams to develop a Lineup Consistency Score (LCS) for college gymnastics. The LCS compare the total lineup changes to the total number of spots per event per team for the 2023 season. A maximum score of 100% means that over the entire season, a team never changed the number of events in which each individual gymnast competed.

### Data
The data for this project comes from [Road to Nationals (RTN)](https://roadtonationals.com/results/index.php), the official statistical site of NCAA Gymnastics.

2023 individual results and event rankings were scraped using the `scraping_rtn` Python package developed by CGN Senior Data Editor Claire Harmon.

### Programs
Data scraping was done with Python using Google Colab. Analysis was done in R and graphics were created using `ggplot2`.

## Results
The resulting LCS range from N.C. State at 98.9% to Greenville at 83.3%. The average score across all teams is 90.5%, so on average, only about 10% of a team’s lineup changed over the 2023 season. The trend line indicates a negative relationship between a team’s final ranking and its LCS, so higher-ranked teams at the end of the 2023 season tended to have fewer lineup changes than teams who finished lower in the rankings.

<p align="center">
<img src="https://github.com/user-attachments/assets/a10ef7f5-18f1-4566-be4f-bf7c1c2d4a12" width=50% height=50%>
</p>

To see how this looks at an event level, LCS was recalculated for each one. The uneven bars trend line is very close to the overall rank trend line, while vault and beam are nearly twice as steep. Beam had the greatest overall relationship between LCS and final team rank on that event, indicating that stronger teams relied more heavily on a core group of beam workers all season compared to less strong teams. 

<p align="center">
<img src="https://github.com/user-attachments/assets/4c721a21-169d-4a3a-8cc8-a66ca826fcf1" width=50% height=50%>
</p>

For both teams and individual events, having consistency in lineups positively impacts rankings.
