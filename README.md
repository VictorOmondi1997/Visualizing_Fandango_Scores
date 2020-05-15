# Visualizing Fandango Scores

To investigate the potential bias that movie reviews site have, [FiveThirtyEight](https://fivethirtyeight.com/) 
compiled data for `147` films from 2015 that have substantive reviews from both 
critics and consumers. Every time Hollywood releases a movie, critics from 
[Metacritic](https://www.metacritic.com/), [Fandango](https://www.fandango.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), and [IMDB](https://www.imdb.com/) review and rate the film. 
They also ask the users in their respective communities to review and rate the film. Then, they calculate the average rating from both critics and users and display them on their site. Here are screenshots from each site:
![](https://s3.amazonaws.com/dq-content/review_sites_screenshots.png)
FiveThirtyEight compiled this dataset to investigate if there was any bias to Fandango's ratings. In addition to aggregating ratings for films, Fandango is unique in that it also sells movie tickets, and so it has a direct commercial interest in showing higher ratings. After discovering that a few films that weren't good were still rated highly on Fandango, the team investigated and published [an article about bias in movie ratings.](http://fivethirtyeight.com/features/fandango-movies-ratings/)


## Dataset

You can explore/download the data set [here](data/fandango_scores.csv)

## Columns Description

The descriptions of the columns are as follows.

* `FILM` - film name
* `RT_user_norm` - average user rating from Rotten Tomatoes, normalized to a 1 to 5 point scale
* `Metacritic_user_nom` - average user rating from Metacritic, normalized to a 1 to 5 point scale
* `IMDB_norm` - average user rating from IMDB, normalized to a 1 to 5 point scale
* `Fandango_Ratingvalue` - average user rating from Fandango, normalized to a 1 to 5 point scale
* `Fandango_Stars` - the rating displayed on the Fandango website (rounded to nearest star, 1 to 5 point scale)

> Instead of displaying the raw rating, it has been discovered that Fandango usually rounded the average rating to the next highest half star (next highest 0.5 value). The `Fandango_Ratingvalue` column reflects the true average rating while the `Fandango_Stars` column reflects the displayed, rounded rating.