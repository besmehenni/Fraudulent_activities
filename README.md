# Fraudulent_activities

Le but de ce challenge est de construire un modèle qui permet de prédire si une activité d’achat sur un site de E-commerce est frauduleuse.

Après avoir étudié la donnée et réalisé le feature engineering, nous avons utilisé un modèle random forest. Celui-ci donne **95.7% de bonnes prédictions**. Comparé à un modèle base line qui consistant à considérer que tous les achats ne sont pas des fraudes (accuracy score de 90.64%), le modèle fait mieux que la base line ce qui est réconfortant au sujet de l’intérêt du modèle utilisé.

La proportion de fraudes effectives mais qui n'ont pas été prédites est très important. Nous avons dès lors formulé l’objectif de diminuer cette proportion en tenant d’améliorer le modèle. Ceci est traité en deuxième partie.

Les courbes ROC ont été construites et les fraudes difficiles à prédire isolées. Suite à la vérification des corrélations entre variables du jeu de données difficile à prédire, nous avons réduit le nombre de variables explicatives.

Nous avons ensuite préparé un modèle de **stacking**, une méthode d’**ensembling** qui consiste à utiliser plusieurs modèles pour une prédiction. Les modèles de première couche sont un **Random Forest Classifier** et un **XGBoost XGBClassifier**. Le modèle de seconde couche est un **LogisticRegressor**.

Les résultats obtenus par ce second modèle de stacking ne sont pas meilleurs que ceux du premier modèle basé sur le random forest seul. En conclusion, la proportion de fraudes non prédites est restée au même niveau malgré nos efforts. Une piste d’amélioration serait peut-être de davantage travailler le feature engineering du jeu de données difficile à prédire.
