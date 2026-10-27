# M115 TP2 — Préparation et qualité des sources

## 📌 Présentation du projet

Ce projet est réalisé dans le cadre du module **M115 — Analyse de données multidimensionnelles et Business Intelligence (BI)**.

L’objectif est de préparer, nettoyer et contrôler le jeu de données **Online Retail** à l’aide de Python et Pandas afin de produire une source de données fiable et traçable pour les prochaines étapes du projet décisionnel.

## 🎯 Objectifs

- Explorer la structure et la qualité des données.
- Identifier les valeurs manquantes et les doublons exacts.
- Analyser les annulations, les retours et les valeurs incorrectes.
- Préparer les données selon les règles métier du TP.
- Conserver les lignes exclues dans une couche d’audit.
- Calculer le montant de chaque ligne de vente.
- Comparer les données avant et après préparation.
- Vérifier que les lignes avec un `CustomerID` manquant ne sont pas supprimées à tort.

## 📊 Jeu de données

**Online Retail Dataset — UCI Machine Learning Repository**

Le fichier source utilisé est `Online Retail.xlsx`.

Il contient les informations suivantes :

| Colonne | Description |
|---|---|
| `InvoiceNo` | Numéro de facture |
| `StockCode` | Code du produit |
| `Description` | Description du produit |
| `Quantity` | Quantité achetée |
| `InvoiceDate` | Date de la facture |
| `UnitPrice` | Prix unitaire |
| `CustomerID` | Identifiant du client |
| `Country` | Pays du client |

Source du dataset : https://archive.ics.uci.edu/dataset/352/online+retail

## 🛠️ Technologies utilisées

- **Python** — langage de programmation
- **Pandas** — manipulation et préparation des données
- **Matplotlib** — visualisation des résultats
- **Jupyter Notebook / Kaggle Notebook** — environnement de travail

## ⚙️ Étapes de réalisation

### 1. Exploration des données
Analyse du nombre de lignes et de colonnes, des types de données, des valeurs manquantes et des statistiques principales.

### 2. Contrôle des doublons
Suppression uniquement des doublons exacts sur les huit colonnes sources, sans utiliser `InvoiceNo` et `StockCode` seuls comme clé de ligne.

### 3. Analyse des anomalies
Identification des factures annulées, des quantités négatives ou nulles, des prix unitaires incorrects et des identifiants clients manquants.

### 4. Préparation des données
Application des règles de préparation pour identifier les lignes correspondant au périmètre des ventes. Les lignes exclues restent disponibles pour l’audit.

### 5. Calcul du montant
Création de la colonne dérivée :

`MontantLigne = Quantity × UnitPrice`

Les colonnes `Quantity` et `UnitPrice` sont conservées.

### 6. Contrôle et visualisation
Comparaison des nombres de lignes avant et après préparation, visualisation des résultats et vérification de la conservation des lignes avec un `CustomerID` manquant.

## ▶️ Exécution du projet

1. Ouvrir le notebook dans Kaggle ou Jupyter Notebook.
2. Ajouter le dataset Online Retail à l’environnement.
3. Vérifier le chemin du fichier Excel dans le code.
4. Exécuter les cellules dans l’ordre.
5. Consulter les résultats, les graphiques et les contrôles de qualité.

## 🔎 Résultat attendu

Le projet vise à produire une couche **L2 — Sources auditées et données préparées**, accompagnée de contrôles et de traces permettant d’expliquer les transformations effectuées.


