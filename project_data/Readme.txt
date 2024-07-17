COMP30027 Machine Learning 2024
Assignment 2

_____________________________________________________

The provided dataset is modified "IMDb rating prediction dataset".

https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset

It includes a variety of features extracted from movie metadata, including director names, actor names, genres, plot keywords, and more. 

Additionally, this version of the dataset incorporates advanced text processing techniques such as CountVectorizer, Doc2Vec, and FastText to enrich the feature set with textual data from movie titles, genres, and plot keywords.

The dataset is public available for research. Please include detailed relevant citations. 
_____________________________________________________


Data Description

The dataset consists of multiple columns, each representing different aspects of movies and their metadata. Below is a description of the key columns included in the dataset(excluding id):

	1- 	director_name: 			Name of the movie director.
	2-	num_critic_for_reviews: 	Number of critic reviews.
	3-	duration: 			Duration of the movie in minutes.
	4-	director_facebook_likes: 	Number of Facebook likes for the director.
	5-	actor_3_facebook_likes: 	Number of Facebook likes for the third listed actor.
	6-	actor_2_name: 			Name of the second listed actor.
	7-	actor_1_facebook_likes: 	Number of Facebook likes for the first listed actor.
	8-	gross: 				Gross earnings of the movie.
	9-	genres: 			Genres of the movie.
	10-	actor_1_name: 			Name of the first listed actor.
	11-	movie_title: 			Title of the movie.
	12-	num_voted_users: 		Number of users who voted for the movie.
	13-	cast_total_facebook_likes: 	Total number of Facebook likes for the entire cast.
	14-	actor_3_name: 			Name of the third listed actor.
	15-	facenumber_in_poster: 		Number of faces in the movie poster.
	16-	plot_keywords: 			Keywords describing the plot of the movie.
	17-	num_user_for_reviews: 		Number of user reviews.
	18-	language: 			Language of the movie.
	19-	country: 			Country where the movie was produced.
	20-	content_rating: 		Content rating of the movie.
	21-	title_year: 			Year the movie was released.
	22-	actor_2_facebook_likes: 	Number of Facebook likes for the second listed actor.
	23-	movie_facebook_likes: 		Number of Facebook likes for the movie.
	24-	title_embedding: 		Embedding vector for the movie title, generated using FastText.
	25-	average_degree_centrality:	A measure of centrality for the movie in the network of movies based on shared actors.

	26-	imdb_score_binned: (OUTPUT)	Binned IMDb score of the movie, used as the target variable for prediction.


_____________________________________________________


**    1. train_dataset.csv & test_dataset.csv

	- train_dataset.csv file contains movie features and the target label for training instances.
	- Number of instances: 3004
	- Number of columns: 27
	- test_dataset.csv file contains movie features without the target label for training instances.
	- Number of instances: 752 
	- Number of columns: 26
	- The columns are (no imdb_score_binned for test):
		id director_name num_critic_for_reviews duration director_facebook_likes actor_3_facebook_likes actor_2_name actor_1_facebook_likes 
		gross genres actor_1_name movie_title num_voted_users cast_total_facebook_likes actor_3_name facenumber_in_poster plot_keywords num_user_for_reviews
		language country content_rating title_year actor_2_facebook_likes movie_facebook_likes title_embedding average_degree_centrality imdb_score_binned	
	
_____________________________________________________


Data Preprocessing

The dataset includes preprocessing and additional features: 

	Binning IMDb Scores: 	The IMDb scores have been categorized into bins to transform the prediction task into a classification problem.
	Missing Value Handling: Missing values in the dataset have been carefully handled, either by imputation or removal.

_____________________________________________________

