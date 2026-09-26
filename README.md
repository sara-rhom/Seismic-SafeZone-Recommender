# 🌍 Seismic SafeZone Recommender - Agadir

Un système de recommandation intelligent et hybride développé en Python pour guider la population vers des zones de refuge sûres et accessibles en cas de séisme à Agadir.

---

## 🎯 Problématique & Solution

Lors d'un séisme, l'évacuation rapide vers des zones sûres est vitale. Ce système résout ce problème en combinant deux critères fondamentaux :
1. **La Proximité Géographique** : Trouver instantanément les refuges les plus proches.
2. **Le Score de Sécurité Experte** : Prioriser les lieux jugés fiables par des ingénieurs civils, experts sismiques et forces de l'ordre.

---

## 🔬 Approche Algorithmique Hybride

Le système calcule un **score hybride** équilibrant accessibilité et sûreté :
- **Filtrage basé sur le contenu (KDTree)** : Recherche spatiale rapide pour extraire les k-points d'intérêt les plus proches.
- **Filtrage Collaboratif (KNN / Surprise)** : Prédiction des notes de sécurité pour les zones non évaluées à partir des avis d'experts.
- **Visualisation Cartographique (Folium & GeoPandas)** : Génération automatique de cartes interactives affichant la position utilisateur et les 5 meilleures recommandations.

---

## 📊 Performance du Modèle

- **RMSE** : `0.8263` | **MAE** : `0.6889` *(Modèle collaboratif de sécurité)*
- **Precision@5** : `72.22%`
- **Recall@5** : `100%`

---

## 💻 Tech Stack

- **Langage** : Python 3.x
- **Data & Machine Learning** : Pandas, NumPy, SciPy (KDTree), Scikit-Surprise (KNN)
- **Geospatial & Cartographie** : GeoPandas, Folium
- **Environnement** : Jupyter Notebook

---

## 🚀 Installation & Utilisation

```bash
# 1. Cloner le dépôt
git clone [https://github.com/VOTRE_PSEUDO/seismic-safezone-recommender.git](https://github.com/VOTRE_PSEUDO/seismic-safezone-recommender.git)
cd seismic-safezone-recommender

# 2. Installer les dépendances
pip install pandas numpy scipy scikit-surprise geopandas folium