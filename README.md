# Movies-Recommendation-system
This project builds a Movie Recommendation System in Python using **collaborative filtering**. The system suggests movies similar to the ones users have liked, based on the **K-Nearest Neighbors (KNN)** algorithm applied on user ratings.

## Features
- **User Input for Movie Recommendations**: The system takes a movie title from the user and recommends similar movies based on ratings.
- **Collaborative Filtering**: Recommendations are based on the preferences of users with similar tastes.
- **KNN for Similarity**: The system uses KNN to find movies that are close in terms of user ratings.

## Datasets Used
The recommendation system uses the following datasets from the [MovieLens](https://grouplens.org/datasets/movielens/) dataset:
- **`ratings.csv`**: Contains user ratings for various movies.
- **`movies.csv`**: Contains metadata about the movies such as movie ID and title.

Both datasets are automatically loaded from a URL.

## Installation and Requirements

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ritika-dhanda/recommendation-system.git
   cd recommendation-system
   ```

2. **Install Dependencies**:
   Make sure you have the required libraries installed. You can install them using `pip`:
   ```bash
   pip install numpy pandas scikit-learn matplotlib
   ```

## Usage

1. **Run the Recommendation System**:
   Run the Python script and enter a movie title to get recommendations:
   ```bash
   python recommendation_system.py
   ```

2. **Example Interaction**:
   ```
   Enter a movie you like: Toy Story
   Movies similar to 'Toy Story':
   - Toy Story 2
   - A Bug's Life
   - Monsters, Inc.
   - Finding Nemo
   ...
   ```

## How It Works

- **Step 1: Data Loading**: The `ratings.csv` and `movies.csv` datasets are loaded.
- **Step 2: User-Item Matrix**: A sparse matrix is created where rows represent movies and columns represent users. Each entry is a user’s rating for a movie.
- **Step 3: KNN Algorithm**: The system uses the KNN algorithm to find movies that are rated similarly by users.
- **Step 4: Movie Recommendations**: Based on the movie input by the user, the system finds the most similar movies and recommends them.

## Code Explanation

The project contains the following key functions:

- **`create_user_item_matrix(df)`**: Converts the ratings dataset into a user-item matrix.
- **`find_similar_movies(movie_id, X, movie_mapper, movie_inv_mapper, k=10)`**: Uses KNN to find movies similar to the given movie ID.
- **`recommend_movies_based_on_input(movie_title, X, movies, movie_mapper, movie_inv_mapper, k=10)`**: Recommends movies based on user input by finding similar movies using the KNN model.

## Future Improvements
- **GUI Integration**: Create a web or desktop interface to take user input and display recommendations.
- **Hybrid Filtering**: Combine collaborative filtering with content-based filtering for improved recommendations.

## Contributing
Feel free to fork this repository, make changes, and submit a pull request. All contributions are welcome!

## License
This project is licensed under the MIT License.
