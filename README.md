## Machine Learning supervisé — Régression & Classification (Python / scikit-learn)

Ce dépôt contient deux scripts Python complets et reproductibles illustrant une mise en œuvre rigoureuse du machine learning supervisé, en régression et en classification, avec :

préparation des données propre,

pénalisations (LASSO, Ridge, Elastic Net),

validation croisée interne + externe,

prédictions honnêtes (out-of-sample),

métriques finales globales.

### 📌 Script 1 — Régression supervisée (ML_regression_supervisee.py)
#### 🎯 Objectif

🧠 Comparer plusieurs modèles de régression linéaire pénalisée sur le jeu de données Ozone, en respectant une validation croisée externe stricte.

#### 🧪 Modèles implémentés

MCO (régression linéaire classique)

LASSO

Ridge

Elastic Net (α = 0.5)

🔁 Méthodologie

Encodage des variables catégorielles (dummies)

Standardisation apprise uniquement sur le train

Validation croisée interne pour le choix des hyperparamètres

Validation croisée externe (10 blocs) pour des prédictions honnêtes

Agrégation finale des prédictions

📊 Évaluation

RMSE globale calculée sur l’ensemble des prédictions out-of-sample

Sauvegarde :

PREV_regression_base.csv → toutes les prédictions

perf_regression_base.csv → tableau de performance

### 📌 Script 2 — Classification supervisée (ML_classification_supervisee.py)
🎯 Objectif

Comparer plusieurs variantes de régression logistique pénalisée sur le jeu de données SAheart (maladie coronarienne).

🧪 Modèles implémentés

Logistique non pénalisée

Logistique LASSO

Logistique Ridge

Logistique Elastic Net

🔁 Méthodologie

Construction de la matrice de design via patsy

Standardisation intégrée dans des Pipeline

Validation croisée interne pour le choix de λ

Validation croisée externe (10 blocs) pour des probabilités honnêtes

Grilles de pénalisation construites de manière contrôlée

📊 Évaluation

AUC globale calculée sur toutes les observations

Sauvegarde :

PROB_classif.csv → probabilités prédites

perf_classif.csv → AUC par modèle
