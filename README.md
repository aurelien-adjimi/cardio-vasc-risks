# cardio-vasc-risks
 
## Introduction
Ce projet va vous permettre de mettre en œuvre une régression logistique dans le but d’analyser une variable binaire en fonction d'une variable explicative quantitative. La régression logistique consiste à prédire des variables binaires
et non à prédire des variables continues.

## Contexte
Nous travaillons dans le domaine de la médecine préventive. Notre métier est donc de donner des conseils d'hygiène de vie ainsi que de proposer un accompagnement dans le dépistage de maladies et plus spécifiquement, dans la prévention des risques cardio-vasculaire. 

## Déroulement 
Pour ce faire, nous avons une liste des facteurs de risque cardio-vasculaire:  
- Dépression  
- Diabète  
- Antécédents familiaux  
- Obésité  
- Sexe  
- Tabagisme  
- Sédentarité  
- Dyslipidémies  
- Abus d'alcool  
- Hypertension artérielle  
- Troubles du sommeil  
- Age  

En fonction de ces intéractions, des chercheurs ont pu mettre en évidence quatre groupes de facteurs de risque:  
1. Des facteurs non modifiables (le sexe, l’âge et les antécédents
familiaux) : ils prédisent d’autres facteurs, mais ne peuvent pas être
prédits par d’autres facteurs.  

2. Des facteurs liés au mode de vie (le tabagisme, la sédentarité,
l’alcoolisme) : ils prédisent beaucoup d’autres facteurs (sauf les
facteurs non modifiables), mais sont très peu prédits par d’autres
facteurs.  

3. Des facteurs cliniques en amont (les troubles du sommeil, l’obésité, la
dépression) : ils prédisent beaucoup d’autres facteurs et sont
eux-mêmes prédits par de nombreux facteurs.  

4. Des facteurs cliniques en aval (l’hypertension artérielle, les
dyslipidémies, le diabète) : ils prédisent très peu de facteurs, mais sont
en revanche prédits par beaucoup de facteurs.  

Pour nous accompagner au mieux dans notre démarche de prévention de ces risques, on décide de développer un outil qui permet de poser un diagnostic rapide de risques cardio-vasculaire. Cet outil mettra en œuvre un algorithme de machine learning de
classification binaire (prédiction de 0 ou 1) permettant de prédire s’il y a un
risque cardio-vasculaire ou s’il n’y en a pas.


## Veille sur la régression logistique  

**Qu'est-ce que la régression logistique**  
La régression logistique est une technique d'analyse de données qui utilise les mathématiques pour trouver les relations entre deux facteurs de données. Elle utilise ensuite cette relation pour prédire la valeur de l'un de ces facteurs en fonction de l'autre. La prédiction a généralement un nombre fini de résultats, comme oui ou non.

Par exemple, supposons que vous souhaitez savoir si le visiteur de votre site web cliquera ou non sur le bouton de paiement dans son panier d'achat. La régression logistique examine le comportement des visiteurs précédents, tels que le temps passé sur le site web et le nombre d'articles dans le panier. En s'appuyant sur des données du passé, elle détermine que si les visiteurs ont passé plus de cinq minutes sur le site et ajouté plus de trois articles au panier, ils ont cliqué sur le bouton de paiement. À l'aide de ces informations, la fonction de régression logistique peut alors prédire le comportement d'un nouveau visiteur du site web.  

**Pourquoi la régression logistique est-elle importante ?**  
La régression logistique est une technique importante de l'intelligence artificielle et du Machine Learning. Les modèles de ML sont des programmes que l'on peut entraîner afin d'effectuer des tâches complèxes de traitement de données sans intervention humaine. Les modèles de ML crées avec la régression logistique aident par exemple des entreprises à obtenir des informations exploitables à partir de leurs données commerciales. Grâce à ces informations, elles peuvent réaliser une analyse prédictive afin de réduire les coûts opérationnels, d'augmenter l'efficacité et d'accélérer la mise à l'échelle. Voici une liste des avantages de l'utilisation de la régression logistique par rapport à d'autres techniques de ML:  

- Simplicité, les modèles de régression logistique sont mathématiquement moins complexes que les autres méthodes de machine learning. Par conséquent, vous pouvez les mettre en œuvre même si aucun membre de votre équipe ne possède d'expertise approfondie en machine learning.  

- Rapidité, les modèles de régression logistique peuvent traiter de grands volumes de données à grande vitesse, car ils nécessitent moins de capacité de calcul, comme la mémoire et la puissance de traitement. Cela fait d'eux une solution idéale pour les organisations qui se mettent au machine learning afin d'obtenir des résultats rapides.  

- Flexibilité, on peut utiliser la régression logistique pour trouver des réponses aux questions qui ont au moins deux résultats finis. On peut également l'utiliser pour prétraiter les données. Par exemple, la régression logistique peut permettre de trier les données ayant une large plage de valeurs, telles que les transactions bancaires, dans une plage de valeurs finie plus petite. On peut ensuite traiter ce plus petit jeu de données en utilisant d'autres techniques de machine learning pour une analyse plus précise.  

- Visibilité, l'analyse de régression logistique donne aux développeurs une meilleure visibilité sur les processus logiciels internes par rapport aux autres techniques d'analyse des données. Le dépannage et la correction des erreurs sont également plus faciles, car les calculs sont moins complexes.  

**Quelles sont les applications de la régression logistique ?**  
La régression logistique a plusieurs applications concrètes dans de nombreux secteurs d'activité différents comme par exemple la fabrication, les soins médicaux, la finance ou encore le marketing.  

**Comment fonctionne l'analyse de régression ?**  
La régression logistique est l'une des nombreuses techniques d'analyse de régression couramment utilisées par les spécialistes des données dans le domaine du machine learning. Pour comprendre la régression logistique, nous devons d'abord comprendre l'analyse de régression de base. Ci-dessous, j'explique comment fonctionne l'analyse de régression au moyen d'un exemple d'analyse de régression linéaire.

*Identifier la question*  
Toute analyse de données commence par une question commerciale. Pour la régression logistique, on doit formuler la question pour obtenir des résultats spécifiques, par exemple: 
- Les jours de pluie ont-ils un impact sur nos ventes mensuelles ? (oui ou non)  
- Quel type d'activité de carte de crédit le client effectue-t-il ? (activité autorisée, frauduleuse ou potentiellement frauduleuse)  

*Collecter les données historiques*  
Après avoir identifié la question, on doit identifier les facteurs de données impliqués. Nous collecterons ensuite les données passées pour tous les facteurs. Par exemple, pour répondre à la première question ci-dessus, nous pouvons collecter le nombre de jours de pluie et les données de ventes mensuelles pour les trois dernières années.  

*Entraîner le modèle d'analyse de régression*  
Nous allons traiter les données historiques à l'aide d'un logiciel de régression. le logiciel traitera les différents points de données et les reliera mathématiquement à l'aide d'équations. Par exemple, si le nombre de jours de pluie pendant trois mois est de 3, 5 et 8 et que le nombre de ventes pendant ces mois est de 8, 12 et 18, l'algorithme de régression reliera les facteurs à l'équation :  

Nombre de ventes = 2*(nombre de jours de pluie) + 2  

*Faire des prévisions pour des valeurs inconnues*  
Pour les valeurs inconnues, le logiciel utilise l'équation pour effectuer une prédiction. Si nous savons qu'il pleuvra pendant six jours en juillet, le logiciel estimera la valeur de vente de juillet à 14.  

**Comment fonctionne le modèle de régression logistique ?**  
*Equations*  
En mathématiques, les équations donnent la relation entre deux variables : x et y. On peut utiliser ces équations, ou fonctions, pour tracer un graphique le long de l'axe des x et de l'axe des y en saisissant différentes valeurs de x et y. Par exemple, si on trace le graphique pour la fonction y = 2*x, nous obtiendrons une ligne droite. Par conséquent, cette fonction est également appelée fonction linéaire.  
![Fonction linéaire](./img/1.png "Fonction linéaire")  

*Variables*  
En statistique, les variables sont les facteurs ou attributs de données dont les valeurs varient. Pour toute analyse, certaines variables sont des variables indépendantes ou explicatives. Ces attributs sont à l'origine d'un résultat. Les autres variables sont des variables dépendantes ou des variables de réponse, c'est-à-dire que leurs valeurs dépendent des variables indépendantes. En général, la régression logistique explore la façon dont les variables indépendantes affectent une variable dépendante en examinant les valeurs de données historiques des deux variables. 

Dans notre exemple ci-dessus, x est appelé variable indépendante, variable de prédiction ou variable explicative, car sa valeur est connue. Y est appelée variable dépendante, variable de résultat ou variable de réponse, car sa valeur est inconnue.  

*Fonction de régression logistique*  
La régression logistique est un modèle statistique qui utilise la fonction logistique, ou fonction logit, en mathématiques comme l'équation entre x et y. La fonction logit mappe y en tant que fonction sigmoïde de x.  
![Fonction logistique](./img/2.png "Fonction logistique")  

Si on trace cette équation de régression logistique, nous obtenons une courbe en S comme illustré ci-dessous.  
![Courbe](./img/3.png "Courbe de fonction logistique")  

Comme on peut le constater, la fonction logit renvoie uniquement des valeurs comprises entre 0 et 1 pour la variable dépendante, quelles que soient les valeurs de la variable indépendante. C'est ainsi que la régression logistique estime la valeur de la variable dépendante. Les méthodes de régression logistique modélisent également des équations entre plusieurs variables indépendantes et une variable dépendante.  

*Analyse de régression logistique avec plusieurs variables indépendantes*  
Dans de nombreux cas, plusieurs variables explicatives affectent la valeur de la variable dépendante. Pour modéliser de tels jeux de données d'entrée, les formules de régression logistique supposent une relation linéaire entre les différentes variables indépendantes. Nous pouvons modifier la fonction sigmoïde et calculer la variable de sortie finale comme suit : 

y = f(β0 + β1x1 + β2x2+… βnxn)

Le symbole β représente le coefficient de régression. Le modèle logit peut effectuer un calcul inverse de ces valeurs de coefficient lorsqu'on lui donne un jeu de données expérimental suffisamment grand avec des valeurs connues de variables dépendantes et indépendantes.  

*Quels sont les types d'analyse de régression logistique ?*  
Il existe trois approches d'analyse de régression logistique basées sur les résultats de la variable dépendante.  

Régression logistique binaire  
La régression logistique binaire fonctionne bien pour les problèmes de classification binaire qui n'ont que deux résultats possibles. La variable dépendante ne peut avoir que deux valeurs, par exemple oui ou non ou 0 ou 1.

Même si la fonction logistique calcule une plage de valeurs comprise entre 0 et 1, le modèle de régression binaire arrondit la réponse aux valeurs les plus proches. En général, les réponses inférieures à 0,5 sont arrondies à 0, et les réponses supérieures à 0,5 sont arrondies à 1, de sorte que la fonction logistique renvoie un résultat binaire.

Régression logistique multinomiale
La régression multinomiale peut analyser des problèmes qui ont plusieurs issues possibles tant que le nombre de résultats est limité. Par exemple, elle peut prédire si les prix des maisons augmenteront de 25 %, 50 %, 75 % ou 100 % sur la base des données démographiques, mais elle ne peut pas prédire la valeur exacte d'une maison.

La régression logistique multinomiale fonctionne en mappant les valeurs de résultat à différentes valeurs comprises entre 0 et 1. Comme la fonction logistique peut renvoyer une plage de données continues, telles que 0,1, 0,11, 0,12, etc., la régression multinomiale regroupe également la sortie aux valeurs les plus proches possibles.

Régression logistique ordinale
La régression logistique ordinale, ou modèle logit ordonné, est un type spécial de régression multinomiale pour les problèmes dans lesquels les nombres représentent des rangs plutôt que des valeurs réelles. Par exemple, on utilisera la régression ordinale pour prédire la réponse à une question de sondage qui demande aux clients de classer un service comme mauvais, passable, bon ou excellent sur la base d'une valeur numérique, telle que le nombre d'articles qu'ils vous achètent au cours de l'année.