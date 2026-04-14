# BT4222 Group 8 Final Project

## Source Code
[GitHub Repository](https://github.com/seraang04/bt4222-multimodal-movie-recommender-system/tree/main)

## Raw Datasets

1. **MovieLens 1M Dataset**  
   [Download here](https://grouplens.org/datasets/movielens/1m/)  
   Files used: `ratings.dat`, `users.dat`, `movies.dat`

2. **IMDb Top 10000 Movies Kaggle Dataset**  
   [Download here](https://www.kaggle.com/datasets/moazeldsokyx/imdb-top-10000-movies-dataset)  
   File used: `Top_10000_Movies_IMDb.csv`

3. **MovieLens Latest Links Dataset (ml-latest-small)**  
   [Download here](https://files.grouplens.org/datasets/movielens/ml-latest-small-README.html)  
   File used: `links.csv`

4. **Multimodal Features Dataset**  
   [Download here](https://zenodo.org/records/18499145)  
   Files used: `TEXT_mpnet.zip`, `AUD_whisper.zip`, `VID_mvit.zip`

> The above 8 files are also available in this [Google Drive folder](https://drive.google.com/drive/folders/11TXSl9oA9PDux-oxAV1hGZIK-qqZmDXt?usp=sharing).

## Intermediary / Processed Datasets

The processed datasets can also be found in the same [Google Drive folder](https://drive.google.com/drive/folders/11TXSl9oA9PDux-oxAV1hGZIK-qqZmDXt?usp=sharing).

The following 4 parquet files allow users to start running from the **“Engineering Interaction Data”** section of the Jupyter notebook onwards:

- `/BT4222 Project Datasets/preprocessed_data/movie_features_df.parquet`
- `/BT4222 Project Datasets/preprocessed_data/user_features_df.parquet`
- `/BT4222 Project Datasets/preprocessed_data/movie_embeddings.parquet`
- `/BT4222 Project Datasets/preprocessed_data/ratings_filtered.parquet`

## Our Purpose

In today’s highly saturated content environment, users often struggle to discover films that genuinely match their preferences. Our project addresses this problem by improving the relevance of personalized movie recommendations, with the broader aim of enhancing user experience. We formulate this as a **Top-K recommendation** problem, where the objective is to predict and rank **previously unseen user–movie pairs** according to their relevance for each user. More specifically, we investigate whether incorporating multimodal movie information can improve recommendation quality beyond conventional rating- and metadata-based approaches.

## Content

To support this objective, we integrated four datasets — **MovieLens 1M**, **IMDb Top 10000 Movies**, **MovieLens Latest Links**, and a **Multimodal Features** dataset — to enrich user–movie interaction data with structured user metadata, movie metadata, and pretrained text, audio, and video embeddings.

On top of this integrated pipeline, we adapted and evaluated two recommendation model families: a hybrid **Neural Matrix Factorisation (NeuMF)** model and a **Transformer-based multimodal recommender**. Through controlled experiments, ablation studies, and sensitivity analysis, we assessed how different modality combinations and model architectures perform under different amounts of retained user history.

Our results show that multimodal features can improve recommendation quality, particularly within the **NeuMF** framework, and that **text and audio** form the most effective modality combination in our setting.
