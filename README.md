# 🎬 Movie Recommendation System

A modern AI-powered Movie Recommendation System built with **Streamlit**, **FastAPI**, **TMDB API**, and **Machine Learning**. The application allows users to search movies, explore trending content, view detailed movie information, and receive personalized recommendations using **TF-IDF** and **Genre-Based Filtering**.

---

## 📌 Features

### 🔍 Smart Movie Search
- Real-time movie search
- Autocomplete suggestions
- Keyword-based filtering
- Beautiful poster grid layout

### 🏠 Home Feed
Browse movies from different categories:
- Trending
- Popular
- Top Rated
- Now Playing
- Upcoming

### 🎥 Movie Details
View complete information including:
- Movie Poster
- Backdrop Image
- Release Date
- Genres
- Overview

### 🤖 AI Recommendations

#### TF-IDF Based Recommendation
Recommends similar movies based on textual similarity.

#### Genre Based Recommendation
Suggests movies belonging to similar genres.

### ⚡ Fast Performance
- Cached API requests
- Optimized loading
- Responsive UI

---

# 🏗 Project Architecture

```
                User
                  │
                  ▼
          Streamlit Frontend
                  │
      HTTP Requests (REST API)
                  │
                  ▼
           FastAPI Backend
                  │
      ┌───────────┼───────────┐
      │           │           │
      ▼           ▼           ▼
 TMDB API    Recommendation   Dataset
              Engine (ML)
      │
      ▼
  JSON Response
      │
      ▼
 Streamlit UI
```

---

# 🛠 Tech Stack

## Frontend
- Streamlit
- HTML/CSS
- Requests

## Backend
- FastAPI
- Python

## Machine Learning
- Scikit-learn
- TF-IDF Vectorizer
- Cosine Similarity

## Data
- TMDB API
- Movie Metadata Dataset

---

# 📂 Project Structure

```
Movie-Recommender/
│
├── app.py                 # Streamlit Frontend
├── backend/
│   ├── main.py            # FastAPI Server
│   ├── recommendation.py
│   ├── tmdb.py
│   └── utils.py
│
├── models/
│   ├── tfidf.pkl
│   ├── vectorizer.pkl
│   └── movie_data.pkl
│
├── dataset/
│
├── requirements.txt
│
└── README.md
```

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/movie-recommendation-system.git

cd movie-recommendation-system
```

---

## Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run Backend

```bash
uvicorn main:app --reload
```

Default URL

```
http://127.0.0.1:8000
```

---

# ▶️ Run Frontend

```bash
streamlit run app.py
```

Default URL

```
http://localhost:8501
```

---

# 🌐 API Endpoints

| Endpoint | Description |
|-----------|-------------|
| `/home` | Home movie categories |
| `/tmdb/search` | Search movies |
| `/movie/id/{id}` | Movie details |
| `/movie/search` | TF-IDF + Genre recommendations |
| `/recommend/genre` | Genre recommendation |

---

# 📷 Screens

### Home

- Trending movies
- Popular movies
- Search bar
- Movie grid

### Details

- Poster
- Backdrop
- Overview
- Genres
- Release date

### Recommendations

- Similar Movies (TF-IDF)
- Genre Recommendations

---

# ⚙ Configuration

Update the backend API URL inside the Streamlit application.

```python
API_BASE = "https://movie-rec-466x.onrender.com"
```

For local development:

```python
API_BASE = "http://127.0.0.1:8000"
```

This configuration is defined near the top of the application. :contentReference[oaicite:0]{index=0}

---

# 💡 Recommendation Engine

The system combines two recommendation strategies:

### 1. TF-IDF Similarity
- Movie overview vectorization
- Cosine similarity
- Content-based filtering

### 2. Genre Matching
- Uses movie genres
- Finds similar genre movies
- Acts as fallback recommendations

---

# ✨ UI Features

- Responsive design
- Poster grid
- Sidebar navigation
- Dynamic routing
- Loading cache
- Modern card layout
- Clean movie detail page

---

# 📦 Requirements

- Python 3.10+
- Streamlit
- FastAPI
- Requests
- Scikit-learn
- Pandas
- NumPy
- Uvicorn

---

# 🔮 Future Improvements

- User authentication
- Watchlist
- User ratings
- Collaborative filtering
- Deep Learning recommendations
- Personalized profiles
- Dark/Light theme
- Voice search
- Trailer integration
- Review sentiment analysis

---

# 👨‍💻 Author

**Jatin Jangid**

B.Tech Artificial Intelligence & Data Science

Python • Machine Learning • Generative AI • FastAPI • Streamlit • LangChain

---

# 📄 License

This project is intended for educational and portfolio purposes.