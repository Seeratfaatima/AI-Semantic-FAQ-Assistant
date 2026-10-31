
# AI-Powered Semantic FAQ Assistant

An NLP mini project that answers university-related questions by retrieving the most relevant FAQ using text vectorization, embeddings, and cosine similarity.

The project compares traditional keyword-based methods with semantic search to demonstrate how NLP techniques understand and match user queries.

## Project Overview

Students may ask the same question in different ways. For example:

- FAQ: *How can I apply for university admission?*
- User query: *What is the procedure to get into a university?*

Traditional keyword matching may struggle when the wording differs. This project uses sentence embeddings and cosine similarity to find the FAQ that is semantically closest to the user's question.

## Objectives

- Practice fundamental NLP preprocessing and text representation techniques.
- Compare traditional vectorization methods with embedding-based approaches.
- Implement semantic FAQ retrieval using cosine similarity.
- Explore word embeddings and Transformer-based sentence embeddings.
- Evaluate retrieval performance using test queries.

## NLP Techniques Implemented

| Technique | Purpose |
|---|---|
| Text Preprocessing | Lowercase text, remove punctuation, and normalize spaces |
| Tokenization | Split questions into tokens |
| One-Hot Encoding | Demonstrate basic word representation |
| Bag of Words (BoW) | Represent questions using word counts |
| TF-IDF | Weight words based on their importance |
| Word2Vec | Learn dense word vectors using Skip-gram |
| FastText | Learn word representations using character n-grams |
| Sentence Embeddings | Represent complete questions as dense vectors |
| Cosine Similarity | Measure similarity between query and FAQ vectors |
| Semantic Search | Retrieve and rank the most relevant FAQs |

## Technologies Used

- Python
- Google Colab
- NumPy
- Pandas
- Scikit-learn
- Gensim
- Sentence Transformers
- Pretrained model: `all-MiniLM-L6-v2`

## Project Workflow

1. Create a university FAQ knowledge base.
2. Preprocess and tokenize FAQ questions.
3. Convert questions into BoW and TF-IDF vectors.
4. Train Word2Vec and FastText embeddings on the FAQ corpus.
5. Generate sentence embeddings using a pretrained Transformer model.
6. Encode the user's query into a vector.
7. Calculate cosine similarity between the query and stored FAQ vectors.
8. Rank FAQs by similarity and return the best matching answer.
9. Evaluate retrieval performance using test queries.

## Repository Contents

- `AI_Powered_Semantic_FAQ_Assistant.ipynb` — Complete project implementation in Google Colab.
- `README.md` — Project documentation.

## How to Run

### Option 1: Google Colab

1. Open the notebook in this repository.
2. Click **Open in Colab** if available, or download the `.ipynb` file.
3. Upload the notebook to [Google Colab](https://colab.research.google.com/).
4. Run the cells in order.
5. Enter your own university-related questions and compare search methods.

### Option 2: Run Locally

Clone the repository:

```bash
git clone https://github.com/Seeratfaatima/AI-Semantic-FAQ-Assistant.git
cd AI-Semantic-FAQ-Assistant
```

Install the required libraries:

```bash
pip install numpy pandas scikit-learn gensim sentence-transformers
```

Open the notebook using Jupyter:

```bash
jupyter notebook
```

> The Sentence Transformer model is downloaded the first time it is loaded, so an internet connection is required for the initial run.

## Example

**User Query:**

```text
What papers do I need to submit to get into university?
```

The system retrieves a relevant FAQ:

```text
FAQ:
What documents are required for admission?
```

It then displays the associated answer and similarity score.

## Evaluation

The notebook includes test queries with expected FAQ matches and calculates **Top-1 Accuracy**.

Top-1 Accuracy measures how often the highest-ranked FAQ matches the expected answer:

\[
\text{Top-1 Accuracy} =
\frac{\text{Correct top matches}}{\text{Total test queries}}
\]

The project also allows comparison of BoW, TF-IDF, and semantic search results.

## Limitations

- The knowledge base contains a small set of sample university FAQs.
- Word2Vec and FastText are trained on a limited corpus, so their learned vectors are for demonstration.
- Similarity thresholds require tuning using validation queries.
- The assistant can only answer questions covered by its knowledge base.
- Sample answers should be replaced with verified university information before real-world use.

## Future Improvements

- Add a larger FAQ dataset from verified university sources.
- Build a web interface using Streamlit or Flask.
- Add support for multiple universities.
- Include Urdu and Roman Urdu queries.
- Store embeddings in a vector database for scalable retrieval.
- Integrate a language model to generate answers using retrieved FAQ content.
- Add a confidence threshold and fallback mechanism for unsupported questions.

## Learning Outcomes

Through this project, I practiced text preprocessing, vectorization, word embeddings, sentence embeddings, similarity measurement, and semantic information retrieval. I also explored how traditional NLP methods compare with Transformer-based embeddings in a practical application.

---

**Author:** Seerat Fatima  
**Project:** NLP Mini Project — Semantic FAQ Assistant
