# Graph-attention
Graph Attention Networks (GAT) for Binary Graph Classification

Description

Ce projet implémente un modèle Graph Attention Network (GAT) pour une tâche de classification binaire sur des graphes. Le projet utilise le dataset ogbg-molhiv de l'Open Graph Benchmark (OGB) et un dataset synthétique généré pour tester le modèle.

Fonctionnalités

Chargement et analyse du dataset ogbg-molhiv.

Création d'un dataset synthétique pour les tests.

Implémentation d'une couche d'attention pour graphes (Graph Attention Layer).

Construction d'un modèle GAT.

Entraînement et évaluation du modèle sur une tâche de classification binaire.

Prérequis

Python 3.8+

PyTorch

PyTorch Geometric

scikit-learn

NumPy

Installation des dépendances

Pour installer les dépendances nécessaires, utilisez la commande suivante :

pip install torch torchvision torch-geometric scikit-learn numpy

Structure du code

Chargement des données

Le dataset OGB-MOLHIV est chargé à l'aide de la bibliothèque ogb.graphproppred. Une distribution des classes est calculée pour équilibrer les poids des classes lors de l'entraînement.

Dataset Synthétique

Un dataset synthétique est généré avec des matrices d'adjacence aléatoires, des caractéristiques de nœuds et des étiquettes de graphes. Cela permet de tester rapidement le modèle sans dépendre d'un dataset externe.

Modèle GAT

Le modèle GAT est composé de :

Plusieurs couches d'attention pour graphes (Graph Attention Layer).

Une couche de sortie utilisant la moyenne des caractéristiques des nœuds pour produire la prédiction binaire.

Entraînement

L'entraînement est effectué en utilisant :

La fonction de perte BCEWithLogitsLoss pour les tâches de classification binaire.

L'optimiseur Adam avec une régularisation L2 (décay de poids).

Un calcul de précision pour évaluer la performance du modèle.

Usage

Pour exécuter le projet :

python script.py

Le script entraîne un modèle GAT sur le dataset synthétique et affiche la perte et la précision à chaque époque.

Résultats attendus

Le script affiche les valeurs suivantes après chaque époque :

La perte moyenne pour l'époque.

La précision du modèle sur le dataset d'entraînement.

Améliorations futures

Support des graphes pondérés.

Ajout d'une étape d'évaluation sur un jeu de test.

Visualisation des poids d'attention pour interpréter les résultats.

Intégration avec des datasets plus complexes pour des cas réels.
