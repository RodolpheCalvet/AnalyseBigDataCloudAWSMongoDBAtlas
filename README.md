# Spark project MS Big Data Télécom : 

Reprise du prjet de TPP KickStarter 2020-2021

Puis ajout de deux classes scala dans l'environnement configuré Kick Starter
- une classe Scale pour projet Furets NoSQL : MongoDB Atlas (Dans le cloud AWS)
- une classe SCALA pour le même projet version : Hadoop/Spark sur EMR (SolutionEMREC2S3)

/// DEPENDENCIES + IMPORTS dans IntelliJ  -> compilateur sbt   /////////////////////
Le fichier build.sbt est celui de KickStarter modifié avec :
- ajout de dépendencies vers connecteur MongoSpark et MongoScala,
- ajout de dependency AWS : en cours

Ces dependencies sont les liens donnés à sbt pour download les packages pas présents en local.
Les versions se trouvent en allant sur Maven et en checkant les versions.

Ensuite IntelliJ a en local les classes proposées dans les import pour les inclure (si ça se passe mal le nom de classe passe en rouge).

/// DEPENDENCIES + IMPORTS dans spark shell -> compilateur du spark shell  /////////////////////

Des fichier .txt sont présents:

- Il récapitulent notamment pour mon mongo la procédure de connexion au spark shell :
  - lignes de commande pour terminal-> spark shell avec SparkConf qui a pour paramètres :
    - dependencies vers mongo ("packages", coma separated SANS ESPACE),
    - les URL lecture/écriture des serveurs Atlas Mongo.
  - puis le spark shell étant ouvert avec cette commande du .txt, on peut commencer à copier coller notre code IntelliJ pour travailler en session : débug, test..

L'idée est de faire des A/R entre le shell et IntelliJ:
IntelliJ run tout le fichier Scala mais ne retient pas les variables dans une session, alors que le shelle le permet -> une fois les df chargés onteste vite comme en TP,
Les Spark UI sont dispo pour voir les jobs etc sur un port distinct Shell/IntelliJ : 2 process différents..
