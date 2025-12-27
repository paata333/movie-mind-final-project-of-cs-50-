MovieMind – Smart Movie Recommendation System
MovieMind is a Flask-based movie recommendation system that suggests films based on content similarity using machine learning techniques. The system analyzes movie metadata and generates relevant recommendations by applying natural language processing (NLP) techniques to extract important features.
Unlike simple recommendation engines, MovieMind offers a user-driven feedback mechanism where users can remove unwanted suggestions, ensuring a personalized and dynamic recommendation process.
Additionally, this repository includes a Jupyter Notebook, which contains data visualizations, heatmaps, similarity matrices, and feature extraction insights, providing a deeper look into the dataset and recommendation logic.
________________________________________
Core Functionality
1. Movie Recommendation System
The system allows users to search for a movie and receive recommendations based on content similarity. Using NLP techniques, it analyzes movie metadata—including genres, keywords, and overview descriptions—to find the most relevant films.
2. Dual Search Modes
•	Initial Mode – Provides recommendations purely based on similarity, without filtering.
•	Refine Mode – Excludes previously disliked movies, ensuring a more tailored recommendation list.
3. User Feedback Integration
Users can check movies they do not find relevant, and the system remembers this feedback by storing it in a JSON file. This allows MovieMind to refine recommendations dynamically, ensuring that previously disliked movies do not appear again when searching in Refine Mode.
4. Persistent Filtering and Learning
The system stores user feedback in user_feedback.json, which acts as a database to track disliked movies. This ensures that feedback is not lost upon refreshing the page and that recommendations continuously evolve over time.
5. Data Processing and Machine Learning
•	Feature Extraction – The system extracts key information such as genres, keywords, and descriptions.
•	Vectorization – Uses CountVectorizer to convert text-based movie features into numerical representations.
•	Cosine Similarity – Measures how closely movies are related based on their extracted features, allowing the system to rank recommendations effectively.
6. Data Visualization (Jupyter Notebook)
The repository includes a Jupyter Notebook that provides:
•	Heatmaps of movie similarity matrices
•	Feature extraction visualizations
•	Data analysis on movie metadata
•	Exploration of how cosine similarity ranks recommendations
________________________________________
Technology Stack
•	Flask – Powers the backend and request handling.
•	Python – Core language for processing and analysis.
•	Pandas – Used for dataset manipulation and preprocessing.
•	Scikit-learn – Implements NLP techniques such as CountVectorizer and cosine similarity.
•	HTML & CSS – Provides the UI structure and styling.
•	Jupyter Notebook – Used for data analysis and visualization.
•	JSON – Stores user feedback for refining recommendations dynamically.
________________________________________
Dataset Information
MovieMind utilizes the TMDB 5000 Movies Dataset, which includes:
•	tmdb_5000_movies.csv – Contains information such as movie titles, genres, and keywords.
•	tmdb_5000_credits.csv – Stores data about cast and crew members.
•	cleaned_data_file.csv – A preprocessed version of the dataset used for recommendations.
________________________________________
How Recommendations Are Generated
1.	User searches for a movie – The system retrieves its metadata from the dataset.
2.	Vectorization and similarity analysis – The model compares feature vectors to identify the most relevant movies.
3.	Recommendation output – A ranked list of most similar movies is displayed.
4.	User feedback integration – If a movie is disliked, it is stored in user_feedback.json.
5.	Refine Mode activation – On future searches, disliked movies are removed from recommendations.

