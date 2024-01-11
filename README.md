### Introduction

This project focuses on building and evaluating a movie recommendation system using a dataset of user-movie interactions. 

### Project Steps

#### Step 1: Data Loading and Preprocessing

- Read `movies.txt` and create a DataFrame `movies_df`.
- Read `movie_users_10_20.txt` and create a DataFrame `movie_users_df`.
- Convert relevant columns to appropriate data types.

#### Step 2: Data Merging

- Merge `movie_users_df` and `movies_df` on `movie_id`.

#### Step 3: Creating User-Item Interaction Matrix

- Pivot the merged DataFrame to create an interaction matrix with users as rows, movies as columns, and ratings as values.

#### Step 4: Creating Sparse Matrix

- Map user and movie IDs to unique indices.
- Create a COO (Coordinate Format) sparse matrix from the interaction data.
- Optionally convert the COO matrix to CSR (Compressed Sparse Row) format.

#### Step 5: Model Training and Evaluation

- Initialize and train the LightFM model with WARP loss.
- Evaluate the model using precision and recall at k.

#### Step 6: Generating Recommendations

- Define a function `get_top_recommendations` to predict top N movie recommendations for a given user.
- Generate and display recommendations for selected users.



#### Future Work

For future enhancements, we could consider:
- Integrating more diverse data sources for richer user and item profiles.
- Experimenting with different model parameters and advanced algorithms for improved accuracy.
- Implementing a more interactive and user-friendly interface for users to interact with the recommendation system.

This project is a stepping stone towards building more sophisticated and user-centric recommendation systems in the rapidly evolving field of data science and machine learning.

