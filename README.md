# 📊 Student Performance — Exploratory Data Analysis

> Can graphs alone tell the full story of student success? This EDA explores what really drives academic performance using visual analysis only — no ML, no predictions.

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Pandas](https://img.shields.io/badge/Pandas-Data-green) ![Seaborn](https://img.shields.io/badge/Seaborn-Viz-orange) ![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-lightblue)

---

## Dataset

2392 high school students (ages 15–18) with features across 4 categories:

| Category | Variables |
|---|---|
| Démographique | Age, Gender, Ethnicity, ParentalEducation |
| Habitudes d'étude | StudyTimeWeekly, Absences, Tutoring |
| Implication parentale | ParentalSupport |
| Activités | Extracurricular, Sports, Music, Volunteering |

**Target** : `GradeClass` — A / B / C / D / F dérivé du GPA (0–4.0)  
✅ 0 valeurs manquantes.

---

## ❓ Questions & Réponses par les graphes

---

### 1. Quel facteur impacte le plus le GPA ?

> **Les absences.** La heatmap révèle une forte corrélation négative entre GPA et absences — la plus forte de toutes les variables. Plus un élève s'absente, plus son GPA chute.

---

### 2. Étudier plus = meilleures notes ?

> **Pas vraiment.** Le joint plot montre une légère corrélation positive, mais très faible. Le temps d'étude est quasi uniformément distribué, ce qui suggère que d'autres facteurs compensent — certains élèves étudient peu et réussissent, d'autres beaucoup et échouent.

---

### 3. Le soutien scolaire (tutoring) aide-t-il vraiment ?

> **Un peu, mais attention au biais.** Le box plot montre une légère amélioration du GPA chez les élèves avec tutoring. Mais le KDE plot révèle que ces élèves étudient déjà plus — donc la performance améliorée pourrait venir de leur motivation, pas du tutoring lui-même.

---

### 4. L'éducation des parents influence-t-elle le soutien parental ?

> **Non, contre-intuitivement.** On s'attendrait à ce que les parents les plus éduqués soutiennent le plus leurs enfants. Les count plots montrent le contraire : la distribution de l'éducation parentale est similaire à tous les niveaux de soutien. D'autres facteurs (temps, croyances, travail) jouent un rôle plus déterminant.

---

### 5. L'ethnie a-t-elle un impact sur les résultats ?

> **Non.** Le bar plot par ethnie montre des GPA moyens quasi identiques entre les groupes. La surreprésentation des Caucasiens dans le KDE plot était un artefact statistique, pas une réalité de performance.

---

### 6. Les activités extra-scolaires aident-elles ?

> **Légèrement, sauf le bénévolat.** Les bar plots montrent que Sports, Musique et Extracurriculaire sont associés à un GPA légèrement plus élevé. Mais la vraie question : est-ce que les bons élèves font plus d'activités, ou les activités améliorent-elles les résultats ? **Les deux** — mais les élèves à GPA élevé tendent à participer davantage.

---

## 💡 Ce que les graphes seuls peuvent révéler

```
