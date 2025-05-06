# FiabAssur : Fiabilisation de données contractuelles en assurance collective

## Objectif

Ce projet personnel simule une mission de contrôle de qualité de données dans le contexte de l’assurance collective. 
Il s'agit de comparer deux sources contractuelles (assureur vs délégataire) afin d'identifier des anomalies : écarts de montant, erreurs de dates, ou contrats manquants.

## Contexte simulé

Deux fichiers Excel sont fournis dans le dossier "data/" :
- "contrats_assur.xlsx" : contrats enregistrés par l'assureur
- "contrats_deleg.xlsx" : contrats transmis par un partenaire délégataire

Chaque ligne représente un contrat avec plusieurs attributs clés :
- Numéro de contrat
- Dates (début, fin)
- Montant

## ⚙️ Étapes de traitement

1. 📥 Lecture des deux fichiers Excel (avec pandas)
2. 🔗 Jointure automatique sur l'ID contrat
3. 🚨 Comparaison des colonnes critiques :
    - Montant incohérent (> seuil)
    - Date de début/fin divergente
    - Contrat manquant d’un côté
4. 📊 Génération d’un tableau récapitulatif des écarts
5. 📤 Export en Excel ou affichage dans une interface Streamlit

## 🛠️ Stack technique

- Python 3.10+
- Pandas
- Streamlit
- openpyxl

Installation des dépendances :
pip install -r requirements.txt
