# AngularJs4Ionic
-------------------------------------------------------------------------------
    + BoilerPlate AngularJs to implement Ionic mobile framework, back-end API and angular front
      - Le design pattern MVC d'AngularJS et celui de PHP sont-ils compatibles pour un même site web ? Autrement dit, est-il possible / utile / pertinent d'avoir un back-end en PHP suivant le design pattern MVC et un front-end sous AngularJS ?
      Ce qui est pertinanet ici est d'avoir une API (Application Programming Interface). Le back-end renverra du json, un langage que javascript pourra comprendre et utilisé !
-------------------------------------------------------------------------------
    + Application Programming Interface
      - Une API est un logiciel qui offre des services à d'autres logiciels. Dans le cas du web, une API est donc une espèce de boîte noire à laquelle on envoie des requêtes (HTTP) et qui nous retourne les données demandées.
      - Nous utiliserons pour ces échanges le format JSON. Ce format est nativement géré par AngularJS et PHP.
      - Cette API devra pouvoir effectuer, à la demande du front-end, les 4 actions suivantes sur chaque entité de sa BDD, le système L'acronyme informatique anglais CRUD (pour create, read, update, delete) (parfois appelé SCRUD avec un "S" pour search) désigne les quatre opérations de base pour la persistance des données, en particulier le stockage d'informations en base de données :
        . Créer une entrée — Create
        . Récupérer une entrée — Read
        . Modifier une entrée — Update
        . Supprimer une entrée — Delete
      - Notre API va donc simplement implémenter un système de CRUD pour chaque objet. On pourrait donc coder notre API from scratch en ne considérant que cette nécessité. Pour des raisons de sécurité, de stabilité et d'uniformité, il existe un protocole tout trouvé : REST. On dit que notre API sera RESTful.
-------------------------------------------------------------------------------
    + RestFul :
      - Supposons que nous voulons réaliser un serveur REST pour gérer les données d'une base. Nous devons pouvoir ajouter (POST), modifier (PUT), Lire (GET) et Supprimer (DELETE) ces données (la ressource à manipuler).
      - Nous pourrons effectuer plusieurs manipulation sur les données :
          . Les lire : Requête de type GET
          . En écrire : Requête de type POST représente le contenu à créer.
          . Les modifier : Requête de type PUT représente le contenu modifié.
          . Les supprimer : Requête de type DELETE.
-------------------------------------------------------------------------------
    + Les 5 règles à suivre pour implémenter REST
      - l’URI comme identifiant des ressources
        . REST se base sur les URI (Uniform Resource Identifier) afin d’identifier une ressource.
          Ainsi une application se doit de construire ses URI (et donc ses URL) de manière précise, en tenant compte des contraintes REST.
          Il est nécessaire de prendre en compte la hiérarchie des ressources et la sémantique des URL pour les édite
      - les verbes HTTP comme identifiant des opérations
        . Utiliser les verbes HTTP existants plutôt que d’inclure l’opération dans l’URI de la ressource.
          Ainsi, généralement pour une ressource, il y a 4 opérations possibles (cf CRUD)
      - les réponses HTTP comme représentation des ressources
        . Il est important d’avoir à l’esprit que la réponse envoyée n’est pas une ressource, c’est la représentation d’une ressource.
          Ainsi, une ressource peut avoir plusieurs représentations dans des formats divers : HTML, XML, CSV, JSON, etc.
          C’est au client de définir quel format de réponse il souhaite reçevoir via l’entête Accept.
          Il est possible de définir plusieurs formats.
      - les liens comme relation entre ressources
        . les liens d’une ressource vers une autre ont tous une chose en commun : ils indiquent la présence d’une relation.
          Il est cependant possible de la décrire afin d’améliorer la compréhension du système.
          Pour expliciter cette description et indiquer la nature de la relation, l’attribut rel doit être spécifier sur tous les liens
      - un paramètre comme jeton d’authentification
        . C’est un des sujets les plus souvent abordé quand on parle de REST : comment authentifier une requête ?
          La réponse est très simple et est massivement utilisée par des APIs renommées (Google, Yahoo, etc.): le jeton d’authentification.
          Chaque requête est envoyée avec un jeton (token) passé en paramètre $_GET de la requête.
          Ce jeton temporaire est obtenu en envoyant une première requête d’authentification puis en le combinant avec nos requêtes.
          => demande d’authentification
          => accès aux ressources
-------------------------------------------------------------------------------
    + IONIC FRAMEWORK
      . Ionic est un SDK complet open-source pour le développement d'application mobile hybride.
      . Construit sur AngularJS et Apache Cordova, Ionic fournit des outils et des services pour le développement d'applications mobiles hybrides utilisant des technologies Web comme CSS, HTML5 et Sass.
      . Les outils:
        - Ionic Platform :
            Une plateforme cloud pour la gestion et mise en production des applications mobiles multi-plateformes. Les services intégrés permettent à vous et votre équipe de construire, déployer et développer vos applications efficacement.
        - Ionic Creator :
            Un outil de prototypage drag&drop pour créer des applications à l'aide Ionic.
        - Ionic Lab :
            
        - Ionic View :
            Ionic View vous permet de facilement télécharger et visualiser les applications créées avec Ionic Framework.
        - Ionic Market :
            Retrouvez toutes les meilleures ressources de la communauté dont vous aurez besoin pour démarrer le développement de votre application Ionic.
-------------------------------------------------------------------------------

