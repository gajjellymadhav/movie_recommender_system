# movie_recommender_system

A machine learning-powered movie recommendation engine that uses content-based filtering to suggest movies based on user preferences. The system features a beautiful interactive web interface built with Streamlit.

## 🎯 Overview

This project implements a content-based movie recommendation system that analyzes movie features like genres and overviews to recommend similar movies. Users can select a movie from the database and receive personalized recommendations with poster images fetched from The Movie Database (TMDb) API.

## ✨ Features

- **Content-Based Filtering**: Recommends movies based on genre and plot similarity
- **Interactive Web Interface**: Built with Streamlit for an intuitive user experience
- **Movie Posters**: Displays poster images for recommended movies via TMDb API integration
- **Large Movie Database**: Contains over 10,000 movies from various genres and languages
- **Fast Recommendations**: Generates recommendations instantly using cosine similarity

## 📊 Dataset

The system uses a comprehensive movie dataset containing:
- **Total Movies**: 10,000
- **Features**: Movie ID, Title, Genre, Overview, Popularity, Release Date, Vote Average, Vote Count, Original Language
- **Coverage**: International films across multiple genres and languages

### Dataset Statistics
- Average movie rating: 6.62/10
- Average popularity score: 34.70
- Average vote count: 1,547

## 🛠️ Technology Stack

### Backend
- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning and vectorization
- **Requests**: API calls to TMDb
- **Pickle**: Model serialization

### Frontend
- **Streamlit**: Interactive web application framework
- **Custom React Components**: Image carousel for movie poster display

### API Integration
- **The Movie Database (TMDb) API**: For fetching movie posters and metadata

## 🚀 Getting Started

### Prerequisites
- Python 3.7+
- pip or conda package manager

### Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/Chando0185/movie_recommender_system.git
     cd movie_recommender_system
    
2. **Install dependencies**
    ```bash
    pip install -r requirements.txt
   
4. **Required packages:**
   ```bash
    streamlit
    pandas
    scikit-learn
    requests
    pickle (built-in)

6. **Run the application**
    ```bash
    streamlit run app.py
   
**The application will open in your default browser at http://localhost:8501**

## Performance Metrics
Dataset Size: 10,000 movies
Feature Vector Dimension: Up to 10,000 features
Similarity Calculation: O(1) lookup time (precomputed)
Recommendation Generation: ~100ms average response time

## API Configuration
The app uses The Movie Database (TMDb) API. A pre-configured API key is included in app.py for demonstration purposes. For production use:

Get your own API key from TMDb
Replace the API key in app.py line 6
Python
url = "https://api.themoviedb.org/3/movie/{}?api_key=YOUR_API_KEY&language=en-US".format(movie_id)


