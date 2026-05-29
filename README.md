# 🎬 Movie Search & Recommendation System

> A production-style hybrid movie discovery engine combining **BM25 ranking**, **TF-IDF retrieval**, and **genre-aware recommendations** across **22,657+ movies** with **sub-200ms search latency**.

Built using **Flask**, **custom information retrieval pipelines**, and **optimized ranking algorithms** to simulate modern recommendation and search systems used in streaming platforms and AI-powered content discovery engines.

---

# ✨ Features

* 🔍 **Smart Search** – BM25, TF-IDF, and hybrid (BM25 + TF-IDF) ranking
* 🎭 **Genre-Based Recommendations** – weighted by user preference
* ⚡ **Fast Performance** – caching and optimized retrieval pipelines
* 🖼️ **Movie Posters** – dynamic fetching using OMDB API
* 📱 **Responsive UI** – mobile-first responsive interface
* 🔗 **External Resource Links** – quick access to movie resources
* ☁️ **Production Ready** – deployed using Flask + Gunicorn on Render

---

# 🧠 Information Retrieval Concepts Used

## 🔹 BM25 Ranking

State-of-the-art probabilistic ranking algorithm widely used in modern search engines.

## 🔹 TF-IDF Retrieval

Term Frequency–Inverse Document Frequency scoring for contextual relevance estimation.

## 🔹 Hybrid Ranking Pipeline

Weighted combination of BM25 and TF-IDF scores for improved search precision.

## 🔹 Inverted Indexing

Efficient lookup structures enabling fast query processing.

## 🔹 Query Caching

Reduces repeated computation and improves response latency.

These concepts form the foundation of:

* search engines,
* recommendation systems,
* enterprise retrieval systems,
* and Retrieval-Augmented Generation (RAG) pipelines.

---

# 🛠️ Tech Stack

| Category        | Technology                         |
| --------------- | ---------------------------------- |
| Backend         | Flask, Python 3.9                  |
| Search          | Custom BM25, TF-IDF, Hybrid Ranker |
| Recommendations | Genre-Based Scoring                |
| API Integration | OMDB API                           |
| Frontend        | HTML5, CSS3, Jinja2                |
| Deployment      | Render, Gunicorn                   |

---

# 📊 Performance Metrics

| Metric                 | Value                  |
| ---------------------- | ---------------------- |
| Movie Database Size    | 22,657+ movies         |
| Search Latency         | <200 ms                |
| Recommendation Latency | <2 seconds             |
| Search Modes           | BM25 / TF-IDF / Hybrid |
| Deployment             | Cloud-hosted on Render |

---

# 📁 Project Structure

```text id="h8w90o"
movie-search-and-recommendation/
│
├── app.py
├── requirements.txt
├── Procfile
├── runtime.txt
├── build.sh
│
├── models/
│   ├── fast_genre_recommend.py
│   ├── bm25_search.py
│   └── hybrid_search.py
│
├── templates/
│   ├── user_id_entry.html
│   ├── search_page.html
│   ├── genre_recommendations.html
│   └── results.html
│
├── static/
│   └── css/style.css
│
└── data/
    └── movies_links.txt
```

---

# 🚀 Local Development

## Prerequisites

* Python 3.9
* Git

## Setup

```bash id="x1ms5g"
# Clone repository
git clone https://github.com/PriyanshiSingh19/movie-search-and-recommendation.git

cd movie-search-and-recommendation

# Create virtual environment
python -m venv venv

# Activate environment
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Download NLTK data
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet')"

# Run application
python app.py
```

Open in browser:

```bash id="z2i6bw"
http://localhost:5000
```

---

# ☁️ Deployment on Render

## Deployment Steps

1. Push the repository to GitHub

2. Create a new **Web Service** on Render

3. Connect your GitHub repository

4. Configure the following settings:

```bash id="g8i7xn"
Build Command:
./build.sh
```

```bash id="aj8l12"
Start Command:
gunicorn app:app --bind 0.0.0.0:$PORT --timeout 120 --workers 2
```

5. Deploy the application

The `build.sh` script automatically:

* downloads required NLTK data,
* creates cache directories,
* and prepares the environment.

---

# 🎯 Usage

## 🔍 Search Movies

* Enter movie title, genre, or keywords
* Choose search mode:

  * Specific Search
  * General Hybrid Search
* View ranked movie results with posters and external resource links

---

## 🎭 Get Recommendations

* Enter genre preferences
  Example:

```text id="h4p1zs"
action comedy latest
```

* Receive weighted genre-based movie recommendations
* Browse posters, metadata, and resource links

---

# 🔒 Security & Reliability

* Input validation for user queries
* Graceful error handling
* Session-based preference handling
* Cached retrieval for improved reliability
* Deployment-ready production configuration

---

# 🔮 Future Enhancements

## 🚀 Search & Retrieval

* Semantic search using sentence embeddings
* Vector database integration
* Learning-to-Rank pipelines

## 🤖 Recommendation Systems

* Collaborative filtering using user ratings
* Personalized recommendation profiles
* Watchlists and user accounts

## ☁️ Scalability

* REST API migration using FastAPI
* Docker containerization
* Cloud-native deployment pipelines

## 🧠 AI Extensions

* Natural language movie queries
* Conversational recommendation systems
* LLM-powered content discovery

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Test thoroughly
5. Open a pull request

---

# 📄 License

This project is licensed under the MIT License.

Free to use, learn from, and adapt for educational or portfolio purposes.

---

# 👩‍💻 About This Project

This project demonstrates practical implementation of:

* Information Retrieval
* Search Ranking Systems
* Recommendation Engines
* Backend Engineering
* Scalable AI-driven discovery systems

It reflects how modern streaming platforms combine retrieval algorithms with intelligent ranking pipelines to deliver personalized content discovery experiences.

---

Made with ❤️ for movie lovers and search enthusiasts 🎬✨
