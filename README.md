# 🎬 Barbenheimer : NLP Analysis of Audience Discussions

### Executive Summary:

This project analyzes how audiences talked about Barbie and Oppenheimer, the two films released on the same day in July 2023 that created the "Barbenheimer" phenomenon.
Using Python and NLP techniques, more than 48,000 YouTube trailer comments (pre-release) and IMDb reviews (post-release) were cleaned and analyzed with sentiment analysis, word frequencies, word clouds, topic modeling (LDA), TF-IDF and Word2Vec.
Findings show a clear shift in audience discussions: before release, comments were short and speculative, focused on hype, cast and the rivalry between the two films; after release, reviews became longer, more positive and more analytical, focused on storytelling, performances and themes. Based on these findings, I recommend the following actions for film marketing teams:

1. Use the "rivalry" between releases as a viral marketing lever, as it drives engagement and word-of-mouth.
2. Put the cast at the center of pre-release communication, as actors are among the most discussed topics.
3. Monitor post-release reviews with NLP to understand what audiences value in the story and themes.

#### Business Problem:

Barbie and Oppenheimer were released on the same day with opposite styles: a colorful comedy and a dark historical drama. Instead of competing, the two films fed each other's popularity through a viral online phenomenon. Studios and marketing teams need to understand how audience perception changes from trailer to release in order to adapt their communication. This project explores the question: **What linguistic shifts occurred in audience discussions of Barbie and Oppenheimer from pre-release speculation to post-release reception?**

#### Methodology:

1. Data Collection: Used two Kaggle datasets: YouTube comments from the Barbie trailer, the Oppenheimer trailer and a video comparing both films (Barbenheimer), and IMDb reviews for both films (5 CSV files).
2. Data Cleaning: Removed duplicates, extracted review dates, removed spoiler warnings and IMDb page elements with regular expressions, and computed review lengths.
3. Exploratory Analysis: Compared the number of words, average review length and outliers across the 5 datasets.
4. Text Preprocessing: Removed URLs, HTML tags and symbols, expanded slang, then applied tokenization, POS tagging, lemmatization, lowercasing and removal of stop words, punctuation and digits.
5. Sentiment Analysis: Scored valence, extremity and ambivalence of each comment and review with The Lexical Suite, before and after release.
6. Text Analysis: Built word clouds and frequency distributions, extracted topics with LDA, created a TF-IDF document-term matrix, and trained a Word2Vec model visualized with t-SNE.

#### Skills:

1. Data Cleaning & Text Processing: Using regular expressions to clean scraped web text (URLs, HTML, spoilers, dates).
2. Natural Language Processing: Tokenization, POS tagging, lemmatization and stop word removal with NLTK and spaCy.
3. Sentiment Analysis: Measuring valence, extremity and ambivalence of audience opinions.
4. Text Mining & Machine Learning: Topic modeling (LDA), TF-IDF vectorization, word embeddings (Word2Vec) and dimensionality reduction (t-SNE).
5. Python Programming & Tools: Using Pandas, NumPy, NLTK, spaCy, Gensim, Scikit-learn, WordCloud, Matplotlib, Seaborn and Google Colab.

#### Results & Business Recommendation:

**Sentiment shift from pre-release to post-release**

| | Barbie (trailer) | Barbenheimer (trailer) | Oppenheimer (trailer) | Barbie (IMDb) | Oppenheimer (IMDb) |
|---|---|---|---|---|---|
| Number of texts | 23,956 | 9,374 | 12,291 | 797 | 2,036 |
| Overall sentiment | 18.44% | 24.64% | 20.72% | 58.53% | 59.66% |
| Avg. valence score | 1.66 | 2.22 | 1.87 | 5.27 | 5.37 |
| Avg. extremity score | 0.96 | 1.24 | 0.91 | 2.46 | 2.43 |
| Ambivalence | 17.08% | 20.45% | 20.94% | 25.47% | 25.10% |

Before release, comments were short (13 to 27 words on average) and carried little sentiment. The video comparing both films generated the most positive and engaged reactions, which shows the power of the Barbenheimer rivalry. After release, reviews were much longer (170 to 181 words), sentiment about tripled for both films and reached a similar level, and opinions became more nuanced (higher ambivalence).

**What people talked about**

- **Barbie:** discussions focused on the cast (Ryan Gosling, Margot Robbie, Ken), the viewing experience ("watch", "look", "see") and positive emotions ("love", "good", "fun"). Word2Vec links "barbie" to "doll", "land", "pink" and "mattel".
- **Oppenheimer:** discussions focused on Christopher Nolan and Cillian Murphy, and on the film's serious themes ("bomb", "death", "destroyer", "world").
- **Barbenheimer:** comments compared the two films ("first", "two", "time") and mixed Barbie's positive emotions ("love") with Oppenheimer's darker themes ("doom").
- **Topic modeling (LDA):** pre-release topics were about anticipation, marketing and comparisons between the films, while post-release topics moved to reviews, awards and key scenes.

I recommend these actions to film studios and marketing teams:

1. Build marketing campaigns around shared cultural events and audience-driven memes, as the Barbenheimer content drove the strongest engagement.
2. Highlight the director and lead actors in trailers and promotion, as they dominate audience discussions.
3. Adapt communication after release toward story, performances and themes, which become the main topics of reviews.
4. Use NLP tools to track sentiment and topics in real time across social media and review platforms.

#### Next steps:

1. Use transformer-based models (e.g. BERT) for more accurate, context-aware sentiment analysis.
2. Analyze sentiment over time to measure the effect of marketing events and release dates.
3. Add other platforms (Twitter/X, Reddit, TikTok) and handle non-English comments.
4. Link sentiment and topics to box office performance.

#### Files:

- `Barbenheimer NLP python file.ipynb` : Python code (cleaning, preprocessing, sentiment analysis, text analysis)
- `Barbenheimer presentation.pdf` : Final presentation
- `.png` files : Main visualizations (word clouds, word frequencies, TF-IDF, Word2Vec, t-SNE)

*Group project – Natural Language Processing course.*
