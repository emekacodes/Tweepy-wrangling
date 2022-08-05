# Tweepy-wrangling

## Dataset
3 datasets were used for this project.
1. Twitter Archive Enhanced : The WeRateDogs Twitter archive contains basic tweet data for 2356 tweets with rating
2. Image Predictions : image predictions alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction
3. tweet-joson : retweet count and favorite count of WeRateDogs tweets.

## Wrangling
1. Renamed the id column to tweet_id
2. Merged all dog level columns into one column
3. Merged the rt_fav and twitter_archive table
4. Merge the image_pred and twitter_archive table
5. Droped all rows that have retweeted_status_id and retweeted_status_user_id as notnull
6. Removed all +0000 from every row in the timestamp column
7. Changed the timestamp datatype from object to datetime
8. Changed all names in the name column that are weird to None (Coincidentally, all the names are in lowercase)
9. Removed the html part of the source column
10. Changed all cells in the rating_denominator column that has a value that is not 10 to 10 to 10
11. Removed underscores from dog names in p1, p2 and p3
12. Changed all dognames to lowercase in p1, p2 and p3
13. Extracted the correct URLs from the expanded_urls column

## Summary
1. As the years progress, the mean retweet counts and favorite counts have increased (The favorite count and retweet count have a positive corellation)
2. Golden Retriver is the dog with a p1_conf greater than 0.7 that was recognized the most by the neural network
3. We can see the admin mostly tweets between 11pm to 4am
