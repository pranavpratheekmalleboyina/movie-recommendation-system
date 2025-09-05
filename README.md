# 🎬 Movie Recommendation System using Artificial Intelligence

## 📌 Project Overview
This project is a **content-based Movie Recommendation System** built with **Flask** and **Machine Learning techniques**. It recommends movies to users based on genres and similarity scores. By leveraging **TF-IDF vectorization** and **cosine similarity**, the system learns from user queries and provides refined recommendations.


## 🚀 Features
- Recommend movies similar to the genre or keyword provided by the user.
- Uses **TF-IDF** for text vectorization of genres and descriptions.
- Ranks movies using **cosine similarity**.
- Provides movie details such as:
  - 🎥 Title
  - 🎭 Genre
  - ⭐ Average Rating
  - 📅 Release Year
- Interactive **Flask web interface** for recommendations.

## 🛠️ Technologies Used
- **Python 3.12+**
- **Flask** – for the web application
- **scikit-learn** – for TF-IDF vectorization and cosine similarity
- **pandas / NumPy** – for data handling and preprocessing
- **Pickle** – for saving and loading models
- **HTML/CSS (Jinja templates)** – for front-end rendering

## 📦 Requirements (requirements.txt)
Create a `requirements.txt` with the following pinned versions (tested on Python 3.12.6):

```txt
# Web
Flask==3.0.3
Werkzeug==3.0.3
Jinja2==3.1.4
itsdangerous==2.2.0
click==8.1.7

# ML & Data
scikit-learn==1.5.2
pandas==2.2.2
numpy==2.0.1
```

> Optional for production deployments:
> ```txt
> gunicorn==22.0.0
> ```

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/movie-recommendation-system.git
   cd movie-recommendation-system
   ```

2. **Create a virtual environment & activate it**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Linux/Mac
   venv\Scripts\activate      # On Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Ensure the dataset and pickle files are available**
   - `movies_with_ratings.pkl`
   - `vectorizer.pkl`
   - `ratings.csv`

5. **Run the Flask application**
   ```bash
   python app.py
   ```

6. Open your browser and visit:
   👉 `http://127.0.0.1:5000/`

## 📂 Project Structure
```
├── app.py                     # Main Flask application
├── templates/                 # HTML templates (home & results)
│   ├── home.html
│   ├── movies.html
├── static/                    # CSS, JS, images
├── movies_with_ratings.pkl    # Preprocessed movie dataset
├── vectorizer.pkl             # Trained TF-IDF vectorizer
├── ratings.csv                # Ratings dataset
├── MRS.ipynb                  # Jupyter notebook (exploration)
├── README.md                  # Documentation
```

## ▶️ Usage
1. Go to the homepage.
2. Enter a **genre** or **keyword** (e.g., "Action", "Romance", "Sci-Fi").
3. The system will display the **top 5 recommended movies** with their details.


## 📊 Datasets
- **movies_with_ratings.pkl** – Preprocessed dataset containing movie titles, genres, ratings, and release years.
- **ratings.csv** – Raw user ratings dataset used for preprocessing.

## 🤝 Contributions
Contributions are welcome! To contribute:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit changes (`git commit -m "Add new feature"`)
4. Push to branch (`git push origin feature-name`)
5. Create a Pull Request

## 📜 License
This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.
