# Projet Python S1 : the Movie Database
Auteurs : Claire He, Marie Ganon

## Prédiction de la "recette" parfaite pour un film performant

Ce projet s'inscrit dans le cadre du projet d'informatique du cours de *Python pour le datascientist* du 1er semestre de 2ème année à l'ENSAE. 
A partir de la base *The Movie Database* (disponible : https://www.kaggle.com/rounakbanik/the-movies-dataset) que nous avons nettoyée, complétée par du scrapping de mots-clés sur le site IMDB et d'une base labellisée de commentaires IMDB issue d'un projet de classification de sentiments binaires (disponible : http://ai.stanford.edu/~amaas/data/sentiment/), nous souhaitons à l'aide de modèles de ML et de NLP prédire la "recette", s'il y en a une, du succès d'un film au cinéma. 

## Détails des fichiers présents sur le repo

- Scraping_nettoyage.ipynb : Notebook comprenant les codes de nettoyage de la base initiale, ainsi que les différents scrapping réalisés
- Statistiques_descriptives.ipynb : Notebook comprenant les codes de visualisation des données et de statistiques descriptives
- Modélisation.ipnyb : Notebook comprenant les codes relatifs à la modélisation du problème

Dans les dossiers :
- Bases à télécharger (bases lourdes que nous avons zippées et qu'il faut télécharger pour tourner le notebook)
  - movies_metadata.csv.zip : Dataset originel, disponible à l'adresse ci-dessus
  - base_keywords2.csv.zip : Base de données comportant les mots-clés scrappés sur IMDB, ainsi que l'identifiant *imdb_id* du film et son titre *original_title*
  - train_review.csv.zip : Base construite à partir de review_train_{pos, neg} contenant les commentaires sur la première moitié de la base
  - test_review.csv.zip : Base construite à partir de review_test_{pos, neg} contenant les commentaires sur la seconde moitié de la base
        disclaimer : on a gardé les deux bases séparées afin de pouvoir lier les données aux url dans url_table.csv.
  
- Bases utilisées (bases intégrées directement dans le notebook, pas besoin de les télécharger)
  - base.csv : Base de données nettoyée de TMDb
  - url_table.csv : Base de données des url des commentaires
  - review_test_neg.csv : Dataset originel des commentaires négatifs sur la moitié des films utilisé comme base test dans le projet ACL
  - review_test_pos.csv : Dataset originel des commentaires positifs sur la moitié des films utilisé comme base test dans le projet ACL
  - review_train_neg.csv : Dataset originel des commentaires négatifs sur la moitié des films utilisé comme base d'entraînement dans le projet ACL
  - review_train_pos.csv : Dataset originel des commentaires négatifs sur la moitié des films utilisé comme base d'entraînement dans le projet ACL
  
  
## Méthodes utilisées 
LDA, régression linéaire,  sentiment analysis via classificateur bayésien naïf et SVM
