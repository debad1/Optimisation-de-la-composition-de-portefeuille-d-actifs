# Projet d'Optimisation de la Composition de Portefeuille d'Actifs

## Formulation Mathématique du Problème

L'investisseur cherche à maximiser le rendement de son portefeuille tout en maintenant le risque à un niveau acceptable. Le problème consiste à trouver les proportions optimales d'investissement dans différents actifs, sous contraintes de rendement et de risque.

## Problème d'Optimisation

L'objectif est de maximiser le rendement attendu du portefeuille tout en maintenant la variance du portefeuille en dessous d'un seuil acceptable. Le problème est formulé comme une maximisation sous contraintes linéaires et quadratiques.

## Analyse Mathématique

- **Existence et Unicité:** L'objectif et les contraintes forment un problème convexe, assurant l'existence et l'unicité de la solution.
  
- **Caractérisation du Minimum:** Les conditions de Karush-Kuhn-Tucker sont utilisées pour caractériser le minimum du problème.

## Sélection d'un Algorithme de Résolution

Deux approches sont considérées: le **Gradient Projeté** et l'**Algorithme d'Uzawa**.

### Gradient Projeté
- Utilisation d'itérations de projection pour trouver les proportions optimales.
- Méthode itérative avec critère d'arrêt basé sur la convergence.

### Algorithme d'Uzawa
- Résolution du problème d'optimisation sous contraintes en utilisant une combinaison de multiplicateurs de Lagrange.
- Méthode itérative avec critère d'arrêt basé sur la convergence.

## Extraction des Données sur Yahoo Finance

Utilisation de l'API Yahoo Finance pour récupérer les données historiques des actifs considérés. Calcul des moyennes et covariances pour caractériser le comportement des actifs.

## Résolution avec Scipy

Utilisation de la bibliothèque Scipy pour résoudre le problème d'optimisation. Les résultats incluent les proportions optimales et la valeur du portefeuille.

## Gradient Projeté

- Utilisation d'une fonction de projection pour maintenir les contraintes du problème.
- Itérations basées sur le gradient négatif de la fonction objectif.

## Algorithme d'Uzawa

- Utilisation d'une combinaison de multiplicateurs de Lagrange pour résoudre le problème sous contraintes.
- Itérations avec ajustement des multiplicateurs et des coefficients d'itération.

## Discussion et Interprétation

Les résultats montrent que l'algorithme d'Uzawa a produit la meilleure valeur de portefeuille, tandis que le gradient projeté a donné la valeur la plus basse. En termes de temps d'exécution, l'algorithme d'Uzawa est plus rapide. Le choix de l'algorithme dépend des objectifs spécifiques de l'investisseur.
