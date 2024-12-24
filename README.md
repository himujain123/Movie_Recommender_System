# Movie_Recommender_System
# Movie Metadata Processing Project

## Overview
This project processes and analyzes movie metadata from the TMDB dataset. The goal is to clean, transform, and extract meaningful insights from the movie data, including genres, keywords, cast, and crew details. The project uses Python and libraries like `pandas` and `ast` for data manipulation and processing.

---

## Dataset
The project uses two datasets:
1. **Movies Dataset**: `tmdb_5000_movies.csv`
2. **Credits Dataset**: `tmdb_5000_credits.csv`

These datasets contain metadata for over 4,800 movies, including details like budget, genres, cast, crew, keywords, and popularity.

---

## Features and Workflow
1. **Data Loading**:
   - The datasets are read using `pandas` and previewed with `.head()` and `.info()`.

2. **Feature Selection**:
   - Focused columns:
     - `movie_id`
     - `title`
     - `overview`
     - `genres`
     - `keywords`
     - `cast`
     - `crew`

3. **Data Cleaning**:
   - Removed null values using `dropna()`.
   - Converted JSON-like strings in `genres`, `keywords`, `cast`, and `crew` columns into Python lists using the `ast` module.

4. **Data Transformation**:
   - Extracted top genres, keywords, and cast members.
   - Filtered crew to extract only directors.
   - Removed spaces from names for consistency.

5. **Language Insights**:
   - Analyzed the distribution of movies by their original language.

6. **Final Cleaned Data**:
   - A concise and cleaned DataFrame with the following columns:
     - `movie_id`
     - `title`
     - `overview`
     - `genres`
     - `keywords`
     - `cast` (top 3 actors)
     - `crew` (directors only)

---

## Libraries Used
- **pandas**: Data manipulation and analysis.
- **numpy**: Numerical computations.
- **ast**: Safely evaluate string expressions containing Python data structures.

---

## How to Run
1. Clone this repository and ensure you have the required CSV files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`).
2. Install the required libraries:
   ```bash
   pip install pandas numpy
