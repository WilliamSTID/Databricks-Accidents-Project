# Databricks-Accidents-Project

## I - Présentation du projet:

Dans le cadre de la ressource R5.VCOD.09 enseignée par M. SARDELLITTI, nous avons produit ce projet qui fait figure d'examen final. Au cours de celui-ci, nous appliquerons les techniques et méthodes que l'on a vues durant les différents TDs, que ce soit sur la partie GIT, avec le stockage des différents composants, livrables produits, dans ce repository. Mais aussi pour le Cloud avec la production d'un Notebook Databricks dans lequel nous appliquons des techniques de data-science.

## II - Les sources des données:

Dans le cadre de ce projet, nous allons utiliser des données qui portent sur les accidents de la route. Les données que nous avons utilisées nous proviennent du site [data.gouv.fr](https://www.data.gouv.fr/fr/). Au total, nous avons 4 fichiers au format csv:

- carac.csv fournit des caractéristiques sur les accidents
- lieux.csv recense les données sur les lieux des accidents
- veh.csv possède des informations sur les véhicules impliqués
- vict.csv donne des informations sur les victimes

## III - Éléments du repository:

Ce repository contient:

- Les données utilisées:
  - Les données brutes
- Les deux notebooks Databricks:
  - 'Modelisation.dbc' qui est le notebook où l'on a préprocessé nos données brutes et où l'on a développé nos différents modèles.
  - 'Test API' qui est le notebook où l'on a testé l'API de notre meilleur modèle de classification.

## IV - Modèle retenu:

Au cours de notre notebook 'Modelisation.dbc', nous avons pu tester trois types de classifieurs:
- `K-Nearest Neighbors`
- `Decision Tree`
- `Random Forest`

En comparant les performances de ces trois classifieurs, nous avons pu retenir le meilleur qui est `Decision Tree` avec un score de 61,33% en précision et 59,5% pour le F1-Score.
Les paramètres que l'on a utilisés avec ce classifieur pour obtenir ces résultats sont:

- `max_depth`: None
- `min_samples_leaf`: 0.01

## V - Lien à l'API:

Vous pouvez tester notre classifieur avec cette API:
https://adb-7274745417909117.17.azuredatabricks.net/serving-endpoints/Best_model/invocations
