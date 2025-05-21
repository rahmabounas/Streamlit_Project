# 💳 Détection de Fraudes par Carte Bancaire avec XGBoost

Ce projet vise à détecter automatiquement les fraudes dans les transactions bancaires à l'aide du modèle **XGBoost**, en se basant sur des données réelles et fortement déséquilibrées.

## 📊 Données utilisées

- **Source** : Transactions par carte bancaire (données anonymisées)
- **Nombre total de transactions** : 284,807
- **Nombre de fraudes détectées** : 492 (soit 0.17 % du total)

### 📁 Description des variables

- `Time` : Temps écoulé depuis la première transaction enregistrée (en secondes)
- `Amount` : Montant de la transaction
- `V1` à `V28` : Variables numériques transformées par ACP (données confidentielles)
- `Class` : Variable cible
  - `0` : Transaction normale
  - `1` : Transaction frauduleuse

## 🧠 Objectif du projet

- Identifier automatiquement les transactions frauduleuses à partir de données historiques.
- Maximiser le **rappel** et le **F2-score** pour limiter les fraudes non détectées.

## ⚙️ Modèle utilisé

- **XGBoost (Extreme Gradient Boosting)**
- Seuil de classification optimisé à **0.34**
- Bonnes performances sur données déséquilibrées

## 📈 Résultats obtenus

| Métrique    | Valeur |
|-------------|--------|
| Précision   | 0.883  |
| Rappel      | 0.847  |
| F1-score    | 0.862  |
| F2-score    | 0.854  |
| AUC ROC     | 0.965  |

## 🛠️ Environnement et dépendances

- Python >= 3.8
- Libraries : `pandas`, `numpy`, `scikit-learn`, `xgboost`, `matplotlib`
