# Movie-Recommender-


# Dataset: 
https://files.grouplens.org/datasets/moviel
Dataset (ml-latest-small) is from MovieLens, a movie recommendation service. It contains 100836 ratings and 3683 tag applications across 9742 movies. The data are contained in the files links.csv, movies.csv, ratings.csv and tags.csv.

# Technique 
The two most common types of recommender systems are Content-Based(CB) and Collaborative Filtering(CF).
Content based: uses item features to recommend ie. other items similar to what the user likes, has seen or given feedback.
Collaborative: here first the similar users are found and ratings for each user/item is calculated using ratings of similar users. 

For the following project I have created a movie recommender system which is a hybrid of both the above methodology. I have used a movie dataset which contains 1000000 ratings, 600 users, 9000 movies and 3600 tags. The process of system is:
  1)Cleaning of data
      Removal of symbols like dashes 
      Remove users who haven’t at least rated 55 movies. This helps in  reducing data volume and improving data quality.
  2)Creating of content based latent matrix
      Merging of movie and tag dataset to get metadata which consist of movie genre and tags given by user.
      Use of TF-IDF which is a method which gives us a numerical weightage of words which reflects how important the particular word is to a document.
      Perform dimension reduction using SVD
  3)Creating of collaborative based latent matrix:
      Merging the movie and rating dataset to get metadata that consist of all users ratings
      Perform dimension reduction using SVD
  5)Find similarities between the target movie and others using cousin similarity and combine both matrices for a hybrid recommendation. 
