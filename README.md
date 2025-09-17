# Football Data Analysis with Python ⚽📊

## 🎯 **Objectif**  
Ce projet consiste à analyser des données de football (résultats de matchs et cotes de bookmakers) en utilisant Python. L’objectif est de comprendre les performances des équipes, d’évaluer l’efficacité des cotes et d’explorer des stratégies de pari simples, tout en générant des visualisations claires et pertinentes.

---

## 🛠️ **Technologies utilisées**  
- **Python** : traitement et analyse de données  
- **Pandas** : nettoyage et manipulation des DataFrames  
- **NumPy** : calculs numériques et création de colonnes dérivées  
- **Matplotlib & Seaborn** : visualisations graphiques  
- **Jupyter Notebook** : développement interactif  

---

## 📂 **Contenu et analyses réalisées**

### 1. Nettoyage et préparation des données
- Gestion des valeurs manquantes (NaN) pour les colonnes clés : scores, cotes, cartons, tirs.  
- Standardisation des noms d’équipes pour éviter doublons ou variantes.  
- Conversion des colonnes de date en format datetime pour faciliter les filtrages par période.  
- Création de colonnes dérivées :  
  - `GoalDiff` = HomeGoals - AwayGoals  
  - `TotalGoals` = HomeGoals + AwayGoals  
  - `MatchResultBinary` (1 si victoire domicile, 0 sinon)  

### 2. Analyse de performance dynamique
- Calcul des points cumulés par journée pour chaque équipe (`cumsum`).  
- Visualisation de l’évolution du classement avec des line plots.  
- Heatmaps pour visualiser les séries de victoires et défaites par journée.  

### 3. Analyse des “big matches” et rivalités
- Sélection des matchs entre équipes du top 5 ou oppositions top vs bottom.  
- Calcul des marges de victoire moyennes pour ces rencontres.  
- Analyse de la variance des cotes pour détecter les désaccords des bookmakers.  
- Visualisations : scatter plots scores vs cotes, histogrammes des marges.  

### 4. Analyse “fan insights”
- Taux de buts marqués avant et après la mi-temps.  
- Cartons et fautes par match pour identifier les équipes “agressives”.  
- Ratio tirs cadrés → buts pour déterminer l’efficacité offensive.  
- Visualisations : radar charts par équipe et bar plots comparatifs.  

### 5. Exploration prédictive simplifiée
- Création d’un score “favori probable” basé sur les cotes.  
- Vérification si le favori “prévu” gagne réellement plus de 70 % du temps.  
- Visualisation de la fiabilité des prédictions avec bar charts et heatmaps.  

### 6. Approche data storytelling
- Classement des équipes à domicile vs extérieur (bar chart).  
- Identification des matchs les plus serrés (scatter plot des scores).  
- Détection des surprises de la saison (upsets) où l’outsider l’emporte.  

### 7. Manipulations Python typiques
- `groupby` par équipe ou période pour résumer les statistiques.  
- `merge` ou `concat` pour combiner les données domicile/extérieur.  
- Création de colonnes dérivées avec `apply` ou `np.where`.  
- Calcul de ratios et métriques : efficacité tirs → buts, cartons/match, over/under accuracy.  

### 8. Visualisations métier
- Classement final des équipes (bar chart).  
- Bilan domicile vs extérieur (side-by-side bar chart).  
- Heatmap de corrélation tirs / buts / cartons.  
- ROI d’une stratégie simple de pari (line chart ou bar chart).  
- Comparaison probabilité implicite vs fréquence réelle (scatter plot + line).