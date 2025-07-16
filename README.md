# Projet : Optimisation pour l'Apprentissage Machine (MLSD-AMSD 2024/2025)

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License: Open](https://img.shields.io/badge/license-Open-lightgrey.svg)](#)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](#)
[![NumPy](https://img.shields.io/badge/numpy-supported-orange.svg)](https://numpy.org/)
[![Pandas](https://img.shields.io/badge/pandas-supported-lightblue.svg)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/matplotlib-supported-yellow.svg)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/seaborn-supported-purple.svg)](https://seaborn.pydata.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-supported-green.svg)](https://scikit-learn.org/stable/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-notebook-orange.svg)](https://jupyter.org/)


- [Projet : Optimisation pour l'Apprentissage Machine (MLSD-AMSD 2024/2025)](#projet--optimisation-pour-lapprentissage-machine-mlsd-amsd-20242025)
  - [Présentation](#-présentation)
  - [Objectifs](#-objectifs)
  - [Structure du projet](#-structure-du-projet)
    - [Partie 1 : Décomposition Matricielle et Visualisation](#partie-1--décomposition-matricielle-et-visualisation)
    - [Partie 2 : Optimisation pour la Régression Logistique](#partie-2--optimisation-pour-la-régression-logistique)
  - [Méthodologie Détaillée](#-méthodologie-détaillée)
  - [Installation](#️-installation)
  - [Exécution](#-exécution)
  - [Organisation des fichiers](#-organisation-des-fichiers)
  - [Auteurs](#-auteurs)


##  Présentation

Ce projet, réalisé dans le cadre du Master 1 MLSD-AMSD (Université Paris Cité) encadré par **Lazhar Labiod**, explore deux grandes thématiques clés en optimisation appliquée à l'apprentissage automatique :
- **Décomposition Matricielle (SVD)** pour réorganisation et visualisation de données.
- **Comparaison de méthodes d'optimisation** basées sur la descente de gradient et Newton sur différents jeux de données.

## Objectifs

- Implémenter et comparer la **SVD classique** et la **méthode de la puissance itérée**.
- Visualiser des matrices de données réordonnées pour mieux interpréter leur structure interne.
- Implémenter et évaluer plusieurs **algorithmes d'optimisation** (BGD, SGD, MiniBatch, Newton, Momentum, Nesterov, Adagrad, RMSProp, Adam, AdamW).
- Tester la sensibilité aux hyperparamètres.

##  Structure du projet

### Partie 1 : Décomposition Matricielle et Visualisation
- **Implémentation de la SVD par la méthode des puissances**
- **Analyse de reconstruction de matrices**
- **Vérification du théorème d'Eckart-Young**
- **Comparaison entre vecteurs propres et vecteurs singuliers**
- **Application de R1SVD pour réorganisation de matrices**
- **Visualisation graphique des matrices réordonnées**

### Partie 2 : Optimisation pour la Régression Logistique
- **Implémentation from scratch** de :
  - Batch Gradient Descent (BGD)
  - Stochastic Gradient Descent (SGD)
  - Mini-Batch Gradient Descent
  - Descente de gradient avec Momentum
  - Nesterov Accelerated Gradient
  - Newton Method
  - Adagrad
  - RMSProp
  - Adam
  - AdamW

- **Comparaison expérimentale sur 4 jeux de données** :
  - Haberman (peu d'exemples, peu de features)
  - Sonar (peu d'exemples, beaucoup de features)
  - Covertype (beaucoup d'exemples, beaucoup de features)
  - Mushroom (beaucoup d'exemples, peu de features)

- **Sensibilité aux hyperparamètres**
  - Learning Rate
  - Batch Size
  - Momentum / Beta

##  Méthodologie Détaillée

- **SVD (Singular Value Decomposition)** :
  - Calcul par puissance itérée
  - Reconstruction de matrices et mesure de l'erreur (Frobenius norm)
  - Test du théorème d'Eckart-Young
  - Application à la réorganisation de matrices de similarité

- **Optimisation de la Régression Logistique** :
  - Fonction Coût : Log Loss
  - Descente avec diverses stratégies d'optimisation
  - Évaluation par convergence du coût, temps d'exécution, stabilité

- **Analyse Expérimentale** :
  - Visualisation graphique (matplotlib, seaborn)
  - Tableaux récapitulatifs (tabulate)

## Installation

Prérequis Python >= 3.8 :

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tqdm tabulate
```

## Exécution

Ouvrir le projet dans Jupyter Notebook et exécuter les cellules dans l'ordre des sections.

```bash
jupyter notebook Projet_Opti_ML_24_FINAL.ipynb
```

## Organisation des fichiers

```text
Projet_Opti_ML_24_FINAL.ipynb
├── Partie 1 : SVD et Visualisation
│   ├── Décomposition Matricielle
│   ├── Reconstruction et Analyse d'erreurs
│   └— Réorganisation des matrices
├── Partie 2 : Optimisation de Modèles
    ├── Implémentation de 10 variantes d'optimisation
    └— Comparaison sur 4 datasets + Analyse de sensibilité
```

## Auteurs

- Bastien HOTTELET
- Hamady GACKOU
- Omar NAMOUS

Projet supervisé par **Lazhar Labiod**.

