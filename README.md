# Movie-recommendation
This project is a Movie Recommendation System built using Collaborative Filtering and the K-Nearest Neighbors (KNN) algorithm. The system recommends movies based on user ratings and their similarity to other movies.

Key Features:
User-Based Collaborative Filtering: The system uses user ratings to find similar movies and recommends the top 10 movies based on cosine similarity.
KNN Algorithm: It applies K-Nearest Neighbors using cosine distance to identify the closest matches to a given movie.
Interactive User Input: The user can input any movie name, and the system will recommend a list of movies similar to the input movie.
Data Visualization: Includes visualizations that show the distribution of user ratings per movie, helping to filter out movies that have received fewer ratings.
Dataset:
The project utilizes two datasets:

movies.csv: Contains movie titles and movie IDs.
ratings.csv: Contains user ratings for different movies.
How It Works:
Data Preprocessing: The ratings dataset is pivoted to create a matrix where rows represent movies, columns represent users, and values are the ratings.
Filtering: Movies rated by fewer than 10 users are filtered out, as well as users who have rated fewer than 50 movies.
Sparsity Calculation: The dataset's sparsity is calculated, showing how much of the matrix is populated with ratings.
KNN Model: A K-Nearest Neighbors model is trained using cosine similarity on the sparse matrix of movie ratings.
Movie Recommendation: After training, users can input a movie name, and the system will return 10 similar movies with their cosine distances from the input movie.
Example:

Enter a movie name for recommendations: Toy Story
Output:


1. Toy Story 2 (1999)                 - 0.1234
2. A Bug's Life (1998)                - 0.1456
3. Monsters, Inc. (2001)              - 0.1678
4. Finding Nemo (2003)                - 0.1890
5. Shrek (2001)                       - 0.2021
Technologies Used:
Python:Core language used for building the project.
Pandas: For data loading and manipulation.
NumPy: Used for numerical operations and matrix manipulation.
Matplotlib & Seaborn: For data visualization.
scikit-learn: For implementing the K-Nearest Neighbors algorithm.
SciPy: For working with sparse matrices.
How to Run:
Clone this repository: git clone https://github.com/yourusername/movierecommender.git
Install the required libraries: pip install -r requirements.txt
Download the dataset (movies.csv and ratings.csv) and place them in the project directory.
Run the Python script: python recommender.py
Enter a movie name when prompted to get movie recommendations.
