# Optimisation-Combinatoire


 
I.	Objectif du TP : 

Le problème du sac à dos, (en l'anglais Knapsack Problem) est un problème d'optimisation combinatoire. Il modélise une situation analogue au remplissage d'un sac à dos, ne pouvant supporter plus d'un certain poids, avec tout ou une partie d'un ensemble donné d'objets ayant chacun un poids et une valeur. Les objets mis dans le sac à dos doivent maximiser la valeur totale, sans dépasser le poids maximum.
Ce qui est demandé dans ce TP, c’est de programmer des algorithmes d’optimisation combinatoire selon des méthodes exactes et approchées pour la résolution du problème du sac à dos avec comme critère 0/1 càd on autorise qu’un élément d’un même type. 

II.	Algorithmes réalisés

Les algorithmes réalisés sont les suivants :
•	Algorithme Branch & Bound
•	Algorithme Recuit simulé
•	Algorithme génétique

a.	Algorithme Branch & Bound (BB)
La méthode par séparation et évaluation (Branch and Bound : BB) est une méthode exacte, qui permet d’énumérer intelligemment toutes les solutions possibles. En pratique, seules les solutions potentiellement de bonnes qualités seront énumérées, les solutions ne pouvant pas conduire à améliorer la solution courante ne sont pas explorées.
Pour présenter BB, nous utilisons un arbre de recherche constitué :
•	De nœuds ou sommets, où un nœud représente une étape de construction de la solution
•	D’arcs pour indiquer certains choix faits pour construire la solution
b.	Algorithme Recuit simulé (RS)
Il s’agit d’une méthode approchée et qui a pour but de trouver une solution avec un bon compromis entre la qualité de la solution et le temps. Il se base sur les opérations de recuit en métallurgie. L’opération de recuit consiste à mettre en œuvre tous les moyens nécessaires pour atteindre un maximum qui ne soit pas un maximum local. Pour cela nous avons lancer plusieurs itérations de la fonction de RS afin d’atteindre le maximum global.
c.	Algorithme génétique (GN)
Il s’agit d’une méthode approchée et qui a pour but de trouver une solution avec un bon compromis entre la qualité de la solution et le temps.  Cet algo est un algorithme d’optimisation métaheuristique basé sur les populations. L’implémentation de cet algo passe par les étapes suivantes :
•	Initialisation de la génération
•	Sélection
•	Crossover
•	Mutation 
•	Finalisation
Pour cette fin nous avons défini trois paramètres, le nombre d’individues dans une solution P, le maximum de génération à généré maxGen, et le nombre d’itérations à lancer l’algo. 
III.	Données
On va appliquer les algorithmes développés sur les données du cours ainsi que sur datasets de petite, moyenne et grande échelle.
Données du cours :
| Capacité maximale   | Nbre d’objets  | 
|---------------------|----------------|
|      10             |         5      |
 
 
 
 
|       |1 	|2	|   3    | 4	|5      |
|-------|-------|-------|--------|------|-------|         
|Values	|40	|50	|100	|95	|30     |
|Weights|2  	|3	|   1 	|5  	|3      |


Datasets : J’ai fait le choix de travailler sur ces 4 datasets 

|Petite échelle	 |Capacité maximale|	Nbre d’objets|		|Grande échelle	     |Capacité maximale	|Nbre d’objets|
|----------------|-----------------|-----------------|----------|--------------------|-----------------------|-------------|  
|f1_l-d_kp_10_269|	269        |	           10|		| knapPI_1_100_1000_1|	1000	             |100          |
f2_l-d_kp_20_878 |	878        |	20	     |    	|knapPI_3_200_1000_1 |	1000	             |200          |



IV.	Résultats



Après analyse des résultats, nous pourrons faire les constats suivants :
•	L’algo BB, effectivement, il nous donne toujours le résultat optimal en moins de temps
•	Avec les algos GN et RS, pour avoir le résultat optimal ça nécessite du temps et plusieurs paramètres à ajuster tel que le nombre d’itérations pour le RS, et le nombre de population, le nombre de génération et le nombre d’itération pour l’algo GN 
•	Pour certains datasets, on a pu obtenir les résultats optimaux après l’affinement de ces paramètres mais pour les larges datasets même si on a augmenté ces valeurs est des valeurs aussi importantes nous n’avons pas pu obtenir les résultats optimaux.
•	Avec l’algo génétique en affinant les paramètres, on a pu obtenir les résultats optimaux en moins de temps que l’algo recuit simulé.
