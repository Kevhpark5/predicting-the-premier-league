# Predicting the Premier League

## Sources

### FiveThirtyEight
I used data collected from FiveThirtyEight which includes a record of all matches played between 2016 and 2019 for all leagues around the world. This data includes over 32,000 rows including which teams played, projected goals scored, win probabilities, actual goals scored, spi ratings, and more. This data was provided as a CSV file.

### Krysstal.com
I webscraped tables from Krysstal.com that included a table of all Premier League(or English Top Flight) Champions since the beginning of the competition. From this data I was able to display running totals of championships won.

### Kaggle.com
From Kaggle I used a CSV including the final league tables from the top English league from before the 1890s to the 2016 season. This included the standard data provided in most league tables, such as games played, points, goal difference, wins, draws, losses, etc.

## Initial EDA
After importing the data, I decided to process my data through increasing degrees of specificity. Some of these tables are not fully complete with labels and proper formatting.

I first started to display total titles earned by club:

![Titles](data/images/titlebarchart.png)

I then included a plot of running totals over the years:

![Running1](data/images/titlesearned.png)

And a somewhat clearer version:

![Running2](data/images/titlesearnedplot.png)

After plotting the data, I saw that only a few teams have won in recent history, so I decided to see how the teams performed in terms of league position and not just title win. Since the plot was congested, I decided to separate the data in to the "Big Six"(six clubs widely known to be the most dominant in recent history) as well as other teams with a consistent presence in the Premier League.

![Positions](data/images/leaguepositions.png)

Here it is easier to see the congregation of the big teams towards the top of the title while the other teams have remained primarily in the remaining spots with little exposure to the top 5 or 6 positions. I believe further analysis on this topic is possible.

From here I wanted to explore what constitutes a team winning the league starting with goals scored. This plot shows data on two championship teams over the course of a single season. This shows each match result separated into Home and Away games as well as their projected goals to see how they performed against their own form and their opponent's form.

![Chelsea2016](data/images/projactscores.png)

![Mancity2016](data/images/mancityprojscores.png)

It appears from these plots that Chelsea primarily exceeded their projected scores when they won the title while Manchester City seemed to match or just fall short of projected scores.

After observing this data I wanted to see if there is a relationship between Goal Difference(Goals Scored - Goals Scored Against) and Points earned in a season:

![GD](data/images/gdvspts.png)

It seems as though there are some similarities between the two, but it is not a perfect relationship. I plan to see if hypothesis testing can help discover some information about this data.
