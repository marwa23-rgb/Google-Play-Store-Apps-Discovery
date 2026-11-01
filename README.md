<h1 align="center">📱 Google Play Store Apps Analysis</h1>

<p align="center">
  Exploratory data analysis of 10,000+ Google Play Store apps using Python
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Seaborn-Visualization-4C8CBF" alt="Seaborn">
  <a href="https://www.kaggle.com/lava18/google-play-store-apps"><img src="https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle&logoColor=white" alt="Kaggle"></a>
</p>

## 📌 Overview

This project explores the **Google Play Store Apps** dataset from Kaggle. It cleans the raw data (missing values, duplicates, malformed rows, text columns that should be numbers), answers questions about categories, ratings, installs, reviews, genres, pricing and update dates with Pandas, and visualizes the results with Matplotlib and Seaborn.

---

## ⚡ At a Glance

| 📲 Apps (after cleaning) | 🗂️ Categories | 🎭 Genres | ⭐ Average Rating |
|:---:|:---:|:---:|:---:|
| **10,357** | **33** | **119** | **≈ 4.19** |

---

## 🔄 Workflow

1. **Load & Inspect** – Reviewed the first rows, shape and data types (`head()`, `shape`, `info()`).
2. **Clean the Data** – Handled missing values, removed duplicates and a malformed row, and converted text columns to numbers.
3. **Analyze** – Used `groupby()`, `value_counts()`, sorting and filtering to answer the questions below.
4. **Visualize** – Built bar plots, count plots, a histogram and scatter plots with Matplotlib and Seaborn.

> **Columns:** `App` · `Category` · `Rating` · `Reviews` · `Size` · `Installs` · `Type` · `Price` · `Content Rating` · `Genres` · `Last Updated` · `Current Ver` · `Android Ver`

---

## 🧹 Data Cleaning

| Step | Action |
|---|---|
| **Missing `Rating`** | 1,474 missing values filled with the mean rating |
| **Other missing values** | `Type` (1), `Content Rating` (1), `Current Ver` (8), `Android Ver` (3) |
| **Duplicates** | 483 duplicate rows found and dropped |
| **Malformed row** | Dropped the row whose `Category` was `1.9` |
| **`Price`** | Removed the `$` sign and converted to `float` |
| **`Type`** | Replaced the invalid value `0` with `Free` |
| **`Installs`** | Removed `,` and `+`, then converted to `int` |
| **`Reviews`** | Converted to `int` |

The dataset went from **10,841** rows to **10,357** rows.

---

## 🔍 Key Findings

| Question | Result |
|---|---|
| Number of app categories | **33** |
| Category with the most apps | **FAMILY** (1,943) |
| Average rating of all apps | **≈ 4.19** |
| Apps with a perfect 5.0 rating | **271** |
| Most common genre | **Tools** (842) |
| Most reviewed app | **Facebook** |
| Most common size | **Varies with device** (1,526 apps) |
| Most expensive apps | **I'm Rich - Trump Edition** ($400) and several "I am Rich" apps ($399.99) |
| Average rating: Paid vs. Free | **Paid** (≈ 4.25) vs. **Free** (≈ 4.18) |
| Free vs. Paid apps | **9,591** free · **765** paid |

**Top 5 categories by average rating**

| # | Category | Average Rating |
|:---:|---|:---:|
| 1 | Education | 4.37 |
| 2 | Events | 4.36 |
| 3 | Art and Design | 4.35 |
| 4 | Books and Reference | 4.31 |
| 5 | Personalization | 4.31 |

**Most installed apps** (all at 1,000,000,000+ installs)

Hangouts · YouTube · Gmail · Google Chrome · Subway Surfers · Google Drive · Google Photos · Google Play Games

**Top 10 categories by number of apps**

| Category | Apps | Category | Apps |
|---|:---:|---|:---:|
| Family | **1,943** | Personalization | 388 |
| Game | 1,121 | Lifestyle | 373 |
| Tools | 843 | Communication | 366 |
| Business | 427 | Finance | 360 |
| Medical | 408 | Productivity | 407 |

**Top 10 genres**

| Genre | Apps | Genre | Apps |
|---|:---:|---|:---:|
| Tools | **842** | Personalization | 388 |
| Entertainment | 588 | Lifestyle | 372 |
| Education | 527 | Communication | 366 |
| Business | 427 | Sports | 364 |
| Medical | 408 | Productivity | 407 |

**Content rating**

| Content Rating | Apps |
|---|:---:|
| Everyone | **8,382** |
| Teen | 1,146 |
| Mature 17+ | 447 |
| Everyone 10+ | 377 |
| Adults only 18+ | 3 |
| Unrated | 2 |

**Last updated by year**

| 2014 | 2015 | 2016 | 2017 | 2018 |
|:---:|:---:|:---:|:---:|:---:|
| 204 | 454 | 789 | 1,826 | **6,934** |

---

## 📊 Visualizations

| Plot | Shows |
|---|---|
| Bar plot | Number of apps in each category |
| Histogram | Distribution of ratings |
| Count plot | Number of apps per install bracket |
| Scatter plot | Rating vs. number of reviews |
| Bar plot | Top 10 most common genres |
| Count plot | Distribution of content rating |
| Count plot | Free vs. paid apps |
| Scatter plots | Paid apps and free apps vs. number of installs |
| Count plot | Number of apps by last-updated year |
| Bar plot | Top 5 apps by number of reviews |
## 👩‍💻 Author

**Marwa Samy** · [GitHub](https://github.com/marwa23-rgb)
