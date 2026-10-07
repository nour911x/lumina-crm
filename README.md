# Lumina & Co — Data Marketing (TP1, TP2, TP3)

Analyse de l'export CRM de Lumina & Co : nettoyage et EDA, segmentation RFM, KPIs de campagne et attribution multicanal.

## Contenu

| Fichier | Rôle |
|---|---|
| `Lumina_Co_TP1_TP2_TP3.ipynb` | Notebook unique, exécuté, couvrant les trois TP avec sorties et graphiques |
| `carte_segments_rfm.csv` | Carte des 8 segments RFM (taille, part du CA, médianes R/F/M, priorité) |
| `data/` | Les quatre CSV du CRM (non versionnés, 250 Mo) |

## Lancer le notebook

En local : placer `customers.csv`, `transactions.csv`, `touchpoints.csv` et `campaigns.csv` dans le dossier du notebook (ou dans `data/` en adaptant `DATA_DIR`), puis exécuter toutes les cellules. Dépendances : pandas, numpy, matplotlib.

Sur Google Colab : ouvrir le notebook, exécuter la cellule d'upload et déposer les quatre fichiers.

## Résultats clés

- `customers.csv` est inexploitable pour les métriques agrégées : tout le profil client est reconstruit depuis les transactions.
- 23 % des clients font 80 % du CA ; le pic d'activité est au printemps (avril-juin), pas à Noël.
- 8 segments RFM, priorité 1 aux clients « À risque », 2 aux Champions (19 % de la base, 62 % du CA), 3 aux Nouveaux.
- Display et social ouvrent 80 % des parcours et n'en ferment aucun : invisibles en last touch. Recommandation : attribution en U, renégociation de l'affiliation (84 % du budget, LTV:CAC de 1,8).
