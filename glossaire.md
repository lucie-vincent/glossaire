# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général

1.	Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte
    

2.	Qu’est-ce qu’un algorithme ? 
    Ensemble d’actions pour résoudre un problème / accomplir une tâche. Un programme est l’ensemble des instructions qui représentent un algorithme.

3.	Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?
    Un élément qui associe un nom (identifiant) à une valeur. La valeur peut avoir différentes natures : nombre, texte, booléen. La valeur de la variable peut varier au cours de l’exécution du programme.

4.	Qu’est-ce que la portée d’une variable ?
    La portée d’une variable détermine l’endroit où la variable va être accessible et utilisable. 

    La portée de la variable est locale lorsqu’elle est définie -et donc limitée- à  l’intérieur d’une fonction. (variable locale.)

    La portée de la variable est globale lorsqu’elle est définie en dehors d’une fonction et donc accessible dans l’ensemble du script. (variable globale)

5.	Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
    Une constante est une variable dont la valeur ne peut être modifiée. La portée des constantes est globale.

6.	Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation 
    En PHP, les superglobales sont des variables prédéfinies (internes) dont la portée est globale : elles sont toujours disponibles. Il en existe 9. Ex : $GLOBALS références les variables disponibles dans 1 contexte global.

7.	Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
    +	Chaine de caractère (string) :  $chaine = « Hello world » ;
    +	Entier (integer) : $entier = 29 ; Un nombre sans virgule
    +	Flottant (float) : $flottant = 10.35 ; Un nombre à virgule
    +	Booléen (bool) : $booleen = true ; Utilisé pour exprimer valeur de vérité : True / False
    +	Tableau (array) : $tableau = [« Marie » => 5 , « Jeanne » => 8, « Paul » => 7]
Liste, collection, qui associe 1 clé à 1 valeur (tableau associatif) 
    +	NULL : $valeur = NULL ; Une variable qui n’a pas de valeur assignée

8.	Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?
    +	Tableau indexé sans clé : $tableau = [« bonjour », « coucou », « salut »] ;
    +	Tableau associatif : $tableau = [« Marie » => 5 , « Jeanne » => 8, « Paul » => 7]
    « Marie » = clé (key)	|	5 = valeur (value)

9.	Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles
    +	Structure conditionnelle : une instruction qui n’est exécutée que si une condition est validée.
    +	If / Ternaire
    +	Structure itérative (à répétition) : une instruction (un ensemble de) est répétée plusieurs fois
    +	while (Tant que) : condition de  bouclage | for (Pour) : itération définie

10.	Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
    strlen($string) : int – retourne la taille d’une chaine de caractères.
11.	Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP
    
    Une session est l’ensemble des interactions par l’utilisateur sur le site durant un temps donné (généralement 30mn) : visiter plusieurs pages d’un même site, enregistrer des articles dans 1 panier, poster des messages dans un tableau de bord.
    session_start(); pour démarrer la session dans le ficher PHP

12.	Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
    Un cookie est une quantité de données échangées entre l’utilisateur et le serveur par le protocole HTTP. Il est créé par le serveur et envoyé à l’utilisateur pour être enregistré durant la session. Il est renvoyé par l’utilisateur au serveur lors de chaque requête HTTP.

13.	Quelle est la différence entre les instructions « require » et « include » en PHP
    Les deux instructions permettent d’inclure le contenu d’un autre fichier appelé. La différence est que « require » provoque une erreur bloquante(error) et « include » non(warning).

14.	Comment effectuer une redirection en PHP ?
    La fonction header() permet de créer une redirection en envoyant des entêtes de type Location (adresse). Ex : header(‘Location : http://www.monsite.com /page.php) ;
    La fonction exit() permet de couper l’exécution du script ; la redirection a lieu immédiatement et le reste du code n’a pas d’intérêt à être interprété.
    À noter: cette function doit être appelée avant instructions au navigateur (echo, print,…)

15.	Définir la partie « front-end » et « back-end » d’une application
    +	Front-end : côté client ; fait référence à ce que voient les utilisateurs : texte, boutons,… et avec lesquels les utilisateurs peuvent interagir (menus de navigation,…) : HTML, CSS,JavaScript.  Ce que les utilisateurs voient.
    +	Back-end : côté serveur ; fait référence aux fonctionnalités générales de l’application. Traite les demandes dues aux interactions des utilisateurs. : Requêtes http, serveur de base de données  Ce qui fait fonctionner l’application

16.	Définir le contrôle de version ? Qu’est-ce que Git ?
    +	Contrôle de version : pratique qui consiste à suivre et à gérer les changements apportés au code d’un logiciel
    +	Git est un système de contrôle de version (Version Control  Système) – parmi les plus populaire, gratuit et open source.

17.	Qu’est-ce qu’un CMS ? Citer au moins 2 exemples
    Content Management System. Programme qui permet de créer, modifier un site internet (blog, vente en ligne…)
    +	WordPress, PrestaShop, Drupal


## Front-end
18.	Définir HTML
    HyperText Markup Language : langage de balisage hypertexte.
    Langage utilisé pour structurer une page web et son contenu (paragraphes, formulaires, images)

19.	Définir CSS
    Cascading Style Sheets : feuilles de style en cascade.
    Langage utilisé pour mettre en forme une page web. Permet d’appliquer des styles sur des éléments sélectionnés dans un document HTML.

20.	Définir Javascript
    JavaScript est un langage de programmation orienté objets qui ajoute aux sites web de l’interactivité/permet de les rendre dynamiques. (animations, événements lors de clics)

21.	Définir JSON. Dans quel contexte ce format est-il utilisé ? 
    Le format de données JSON (JavaScript Object Notation) est dérivé de la notation des objets du langage JavaScript. Il peut comprendre des objets (ensemble de paires clé/valeur), des listes ordonnées de valeur (tableaux)

22.	Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?

23.	Qu’est-ce qu’un sélecteur CSS ?
    Un sélecteur définit les éléments sur lesquels les styles s’appliquent.
    + Sélecteur de type : <input> | 
    + sélecteur de classe : .nomclasse | 
    + sélecteurs d’identifiants : #valeurid (unique)

24.	Quelle balise HTML permet de créer un lien hypertexte ?
    La balise <a href =’#url’> description du lien </a>

25.	Qu’est-ce qu’une requête AJAX ?

26.	Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
    + sélecteur de classe : .nomclasse | 
    + sélecteurs d’identifiants : #valeurid (unique)

27.	Définir le responsive design
    Ensemble de pratiques qui permet aux pages web de modifier leur disposition et leur apparence pour s’adapter à différentes largeurs d’écran

28.	Qu’est-ce que le templating ?
    Les templates améliorent l’organisation du code en séparant la présentation( l’affichage)  du reste de l’application.

29.	Qu’est-ce qu’une fonction anonyme en Javascript ?
    Une fonction anonyme est une fonction qui ne possède pas de nom ; le nom d’une fonction est facultatif. Les fonctions anonymes sont généralement utilisées lorsque l’on n’a pas besoin de l’appeler par son nom : son code est appelé qu’à un endroit et n’est pas réutilisé. On peut l’exécuter :
    -	en affectant notre fonction à une variable ; on pourra alors appeler cette variable et exécuter la fonction qu’elle contient : let alerte = function() {…} ; alerte() ;
    -	en créant une fonction auto-invoquée : en ajoutant un couple de () autour de la fonction et après celle-ci : (function(){alert(‘Message d’alerte’)})()
    -	lors du déclenchement d’un événement avec les gestionnaires d’événements : la méthode addEventListener() permet d’exécuter une fonction lors du déclenchement de l’événement

30.	Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
    La classe Array fournit les méthodes pour traiter les tableaux. La méthode push() peut-être utilisée pour ajouter un élément à la fin d’un tableau

31.	Qu’est-ce qu’un « media query » ?
    Les requêtes média (media queries) permettent de modifier l’apparence d’un site ou d’une application en fonction du type d’appareil ( impression, écran, …) et de ses caractéristiques (résolution d’écran, largeur de la zone d’affichage(viewport)).
    Les media queries permettent d’appliquer certains styles de manière conditionnelle avec le CSS grâce aux règles @media et @import

32.	Qu’est-ce qu’un pseudo élément en CSS ?
    Un mot-clé ajouté à un sélecteur qui permet de mettre en forme certaines parties de l’élément ciblé par la règle : p ::first-line { -> la 1ere ligne de l’élément p sera visé

33.	Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
    Bootstrap est un framework utile pour la création de design

34.	Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes
    Grâce à l’attribut « method », la méthode HTTP utilisée pour envoyer les données du formulaire peut-être définie : GET ou POST
    -	GET : utilisée pour récupérer des données. Les données sont de l’utilisateur passent par l’URL
    -	POST : utilisée pour envoyer des données au serveur ; les paramètres(= données saisies par utilisateur) sont passés dans la requête elle-même


## UX UI
35.	Quelle est la différence entre UX Design et UI Design ?
    + UX : User eXperience Design (UXD) est une méthode de conception centrée sur l’utilisateur : l’objectif est de concevoir la meilleure expérience utilisateur possible. Pour résumer l’UX : comment prendre en compte les exigences d’usage au long du processus de conception du produit. Les étapes sont : Analyse (User Research: observer comportement utilisateurs), Conception(maquetter les solutions pour répondre aux besoins des utilisateurs), Évaluation(test utilisateur)

    + UI Design : User Interface (UID) est l’étape de conception de l’interface utilisateur : l’expérience utilisateur(UX) est liée au design graphique de l’interface (UI). UI englobe tout ce qui s’apparente au graphisme, à l’aspect agencement : polices, icônes, couleurs, disposition boutons navigations etc

36.	Qu’est-ce qu’un wireframe ? 
    Maquette “fil de fer” de l’interface : schéma de la structure et des fonctionnalités de l’appli.
    Maquette fonctionnelle, squelette de future interface - esthétique est secondaire (à la différence du mock-up)

37.	Qu’est-ce qu’un prototype ? 

38.	Qu’est-ce que la hiérarchie visuelle en UI Design ?
39.	Qu’est-ce que l’accessibilité en UX Design ? 
40.	Qu’est-ce qu’une grille de mise en page ?
41.	Qu’est-ce que la notion d’affordance en UX Design ?
42.	Qu’est-ce qu’un « mobile first design » ?
    Le responsive design est l’adaptation du design à la taille de l’écran sur lequel il est chargé. Le mobile first design est une approche qui consiste à commencer la réalisation des sites web en commençant par les versions mobiles : mobile  tablette  desktop, en ajoutant au fur et à mesure des interactions ou des effets plus complexes

## Programmation orientée objet (POO)

43.	Donner une définition de la programmation orientée objet 
    Consiste à modéliser un système comme un ensemble d’objets, où chaque objet représente un aspect du système. Les objets contiennent des fonctions (méthodes). Un objet fournit une interface publique pour le reste du code qui voudrait l’utiliser, mais maintient son propre état interne.

44.	Qu’est-ce qu’une classe ? Comment la déclare-t-on ?
    Une classe est une représentation abstraite d’un objet : c’est la somme des propriétés de l’objet. On déclare une classe avec le mot-clé class suivi du nom de la classe et des {} ; on déclare ensuite ses attributs et méthodes. 

45.	Qu’est-ce qu’un objet ?
    On peut rendre une classe concrète au moyen d’une instance de classe (1 objet) : on instancie la classe. Un objet est un exemple concret de la classe. En PHP, on instancie une classe avec le mot-clé new (càd qu’on crée 1 objet)

46.	Définir la notion de propriété / attribut / méthode
    +	Les propriétés (properties) ou attributs sont des variables définies/déclarées au sein d’une classe.
    +	Les méthodes sont les fonctions définies/déclarées à l’intérieur d’une classe.

47.	Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité
    La visibilité d’1 propriété ou d’une méthode définit son accessibilité. Les propriétés et méthodes peuvent avoir une visibilité publique, privée ou protégée. On définit la visibilité avec un mot-clé avant la déclaration ; sans mot-clé la visibilité est automatiquement définie comme publique
    +	public : les éléments sont accessibles partout
    +	private : les éléments sont réservés à la classe qui les a définis
    +	protected : l’accès est réservé à la classe elle-même ainsi qu’aux classes qui en héritent

48.	Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
    Le constructeur _ _ construct($values) permet de créer une nouvelle instance de classe. On peut passer des arguments dans la méthode construct.

49.	Qu’est-ce que l’encapsulation ?
    L’encapsulation consiste à restreindre l’accès à certains éléments d’une classe – ses attributs, méthodes. L’objectif est de ne laisser accessible que le strict nécessaire pour que la classe soit utilisable. En modifiant la visibilité (public, private,..) des éléments de classe, n modifie le niveau d’encapsulation.

50.	Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
    Cela signifie créer une classe à partir d’une autre existante. Le concept mis en œuvre est le concept d’héritage. La nouvelle classe va hériter des méthodes et propriétés de la classe qu’elle étend. Ex : 1 classe Personne, 2 classes Acteur et Réalisateur qui l’étendent.

51.	Définir l’opérateur de résolution de portée
    L’opérateur de résolution de portée (double deux-points (::)) permet d’accéder à une constante, une propriété statique, une méthode d’une classe ou d’une classe parente.

52.	Définir une méthode / propriété statique
    Déclarer une propriété ou une méthode comme statiques permet d’y accéder sans avoir besoin d’instancier une classe. Elles peuvent être accédées depuis une instance d’objet.

53.	Définir le polymorphisme en POO
    Lorsqu’une méthode est décrite dans une classe parente, elle est héritée automatiquement par les classes enfants ; redéfinir cette méthode pour la classe enfant signifie qu’elle aura un comportement différent.

54.	Définir une méthode / classe abstraite ?
    Une classe abstraite est une classe qui ne va pas pouvoir être instanciée directement, càd ne peut pas être manipulée directement. Une méthode abstraite est une méthode dont seule la signature (nom et paramètres) peut-être déclarée mais on ne peut pas déclarer d’implémentation (ce que fait la fonction). Cela permet d’éviter les problèmes de compatibilité dans un code partagé. 

55.	Définir le chaînage de méthodes
    Le chaînage de méthodes permet d’exécuter plusieurs méthodes d’affilée, en les écrivant les unes à la suite des autres.
    Ex : $objet->methodeUn()->methodeDeux()->methodeTrois()->methodeQuatre();
    Il faut finir l’implémentation de la méthode par l’instruction  return $this

56.	Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
    La méthode _ _toString() détermine comment l’objet doit réagir lorsqu’il est traité comme une chaîne de caractères. 
    Il existe plusieurs méthodes magiques ( _ _construct(), qui permet de déclarer un constructeur pour les classes : cette méthode est appelée à chaque création d’une nouvelle instance de l’objet). Ces méthodes sont appelées automatiquement lors d’un événement déclencheur ; elles sont prédéfinies et sont toutes préfixées par 2 _ _

57.	Qu’est-ce qu’un « autoload » ?
    L’auto-chargement de classes. Les classes sont séparées dans différents fichiers individuels ; lorsque l’on veut charger chacune des classes, on doit donc le faire avec une inclusion (require). L’autoload permet d’inclure et de charger plusieurs classes
    
58.	Comment appelle-t-on en français les « getters » et les « setters » ?
    +	Getters -> accesseurs : permettent de retourner la valeur d’une variable
    +	Setters -> mutateurs : permettent de modifier la valeur d’une variable

59.	Qu’est-ce que la sérialisation en PHP ? 

## Architecture 

60.	Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence
    L’architecture client-serveur représente l’environnement dans lequel des programmes transmettent des informations : les consommateurs du service : Client – les fournisseurs du service : Serveur. Ex : le navigateur web d’un client demande (formule une « requête ») le contenu d’une page web à un serveur web qui lui envoie le résultat (formule une « réponse »)
    Le protocole HTTP (HyperText Transfer Protocol) est un protocole de communication client-serveur
    HTTPS- pour secure : variante sécurisée par chiffrement(rendre compréhension d’un document impossible sans clé de chiffrement) et authentification (autoriser accès selon condition)

61.	Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
    Design pattern ou patron de conception : façon standard de résoudre un problème de conception d’un logiciel ; gérer les problèmes d’organisation du code ; ensemble de bonnes pratiques 
    Ex : architecture MVC, Factory(Fabrique), Composite

62.	Qu’est-ce que l’architecture MVC ?
    L’architecture MVC (Model-View-Controller) est une forme (un motif) de design pattern, utilisée pour le développement d’interfaces utilisateur.  

63.	Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
    Model (modèle) : contient les données à afficher
    View (Vue) : contient la présentation de l’interface graphique
    Controller (Contrôleur) : contient la logique concernant les actions effectuées par l’utilisateur 

64.	Quels sont les avantages de l’architecture MVC ?
    
65.	Existe-t-il des variantes à l’architecture MVC ?
66.	Qu’est-ce qu’une API ? Définir l’architecture REST

## Modélisation - Base de données 

67.	Qu’est-ce que la modélisation de données ? Définir la méthode Merise
68.	Quelles sont les 3 étapes principales de la méthode Merise ? 
a.	Analyse, conception et réalisation
b.	Planification, exécution et contrôle
c.	Création, modification et suppression
69.	Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
70.	Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
71.	Donner la définition des mots suivants :
a.	Entité
b.	Relation
c.	Cardinalité
d.	Clé primaire / clé étrangère
72.	Que devient une relation de type « Many To Many » dans le modèle logique de données ?

73.	Qu’est-ce qu’une base de données ?
Une base de données est un ensemble d'informations qui est organisé de façon à être accessible, géré et mis à jour. C'est une méthode de stockage, de gestion et de récupération de l'information.

74.	Définir les notions suivantes : 

a.	SQL : Structured Query Language. Langage de requête structuré. Langage de programmation permettant de stocker et de traiter des informations dans une base de données relationnelle (càd sous forme de tableau, avec des lignes et des colonnes représentants différents attributs de données et les diverses relations entre les valeurs de données)

b.	MySQL : Un système de gestion de base de données (SGBD) open-source.

c.	SGBD (donner 2 exemples de SGBD) : Système de gestion de base de données. Logiciel permettant de stocker manipuler ou gérer des données dans une base de données. Ex: MariaDb, MongoDB, MySQL, Oracle DataBase

75.	Dans une base de données, les données sont stockées dans des tables. Celles-ci sont constituées de lignes appelées enregistrement et de colonnes appelées attribut

76.	Quelle est la différence entre une base de données relationnelle et non relationnelle ?
77.	Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
78.	A quoi sert une vue dans une base de données ?
79.	Qu’est-ce que l’intégrité référentielle dans une base de données ?
80.	Quelles sont les fonctions d’agrégation en SQL ?
81.	Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?
82.	Quelles sont les clauses qui permettent de :
a.	Insérer un nouvel enregistrement dans une table - INSERT INTO table
b.	Modifier un enregistrement dans une table - UPDATE table
c.	Supprimer un enregistrement dans une table - DELETE FROM table 
d.	Supprimer la base de données - DROP 
e.	Filtrer les résultats d’une requête SQL
f.	Trier les résultats d’une requête SELECT
g.	Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique - WHERE 
h.	Concaténer 2 chaînes de caractères - CONCACT

83.	Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?
On se connecte à une base de données en PHP en utilisant la classe native PDO - PHP Data Object.


## Symfony

84.	Qu’est-ce que Symfony ?
85.	Sur quel langage de programmation et design pattern repose Symfony ? 
86.	Quelle est la dernière version en date de Symfony ?
87.	Qu’est-ce qu’un bundle ? 
88.	Quel est le moteur de template utilisé par défaut dans Symfony ?
89.	Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
90.	Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?
91.	Que permet le bundle Maker au sein de Symfony ? 
92.	Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
93.	Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?

## Sécurité

94.	Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
95.	Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
96.	Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
97.	Définir l’attaque par force brute et l’attaque par dictionnaire
98.	Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
99.	A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
100.	Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
101.	Qu’est-ce qu’une politique de mots de passe forts ?
102.	Qu’est-ce que l’hameçonnage ?
103.	Définir la « validation des entrées »

## RGPD

104.	Qu’est-ce que le RGPD ?
Réglement Général sur la Protection des Données (GDPR en anglais). Il encarde le traitement des données personnelles sur le territoire de l'Union Européenne.

105.	Quel est son objectif principal ?
Il fixe les conditions dans lesquelles les données peuvent être collectées, conservées et exploitées, en harmonie sur le territoire de l'Union Européenne.

106.	Quelle est la date d’entrée en vigueur du RGPD ?
Applicable depuis le 25 mai 2018

107.	Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
Rappel à l'ordre, ordonner de satisfaire aux demandes d'exercice des droits des personnes, sanctions péuniaire (jusqu'à 20 millions d'€ ou jusqu'à 4% du chiffre d'affaire annuel mondial)

108.	En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ? 
La CNIL - Commission Nationale de l'Informatique et des Libertés. Elle est chargée de veiller à la protection des données personnelles contenues dans les fichiers et traitements informatiques ou papiers, publics ou privés.

109.	Quel est le consentement valide selon le RPGD ?
Un consentement est valable lorsqu'il s'agit d'une manifestation de volonté, libre, spécifique, éclairée et univoque par laquelle une personne accepte par une déclaration ou un acte positif clair

110.	Qu’est-ce qu’une politique de confidentialité ?
Il s'agit d'un contrat qui décrit comment une société retient, traite, publie et efface les données transmises par ses clients. L'information doit être concise et transparente, compréhensible et accessible aisément.

111.	Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
Les données ne peuvent pas être conservées indéfiniment, elles peuvent être conservées 5 ans maximum. 

112.	Quels sont les droits des utilisateurs selon le RGPD ?
Droit d'information, d'accès, de rectification, d'opposition, à l'affacement (à l'oubli), à la portabilité, ...

113.	Qu’est-ce que le principe de minimisation des données selon le RGPD ?
Ce principe prévoit que les données à caractère personnel doivent être adéquates, pertinentes et limitées à ce qui est nécessaire au regard des finalités pour lesquelles elles sont traitées.

## SEO

114.	Qu’est-ce que le SEO ? 
115.	Quel est l’objectif principal du SEO ?
116.	Existe-t-il plusieurs types de référencement ? Lesquels ?
117.	Qu’est-ce que la densité de mots-clés en SEO ?
118.	Qu’est-ce qu’une balise « alt » ?
119.	Qu’est-ce que la balise « meta description » ?
120.	Qu’est-ce que le « nofollow » en SEO ?
121.	Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
122.	Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
123.	Quelle est la recommandation pour les URL d'un site web bien référencé ?
124.	Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
125.	Qu'est-ce que l'optimisation des images pour le référencement ?
126.	Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

## Gestion de projets - DevOps

127.	Qu’est-ce que la gestion de projet ?	
128.	Qu’est-ce qu’une méthode Agile de gestion de projet ? 
129.	Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
130.	A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
131.	Qu’est-ce que la planification itérative ?
132.	Citer 3 méthodes Agiles dans le cadre d’un projet informatique
133.	Qu’est-ce qu’une réunion de revue de projet ?
134.	Qu’est-ce qu’un livrable dans un projet ? 
135.	Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
136.	Qu’est-ce que le DevOps et quel est son objectif principal ?
137.	Qu’est-ce que l’intégration continue ? 
138.	Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
139.	Qu’est-ce qu’un test unitaire ? 
140.	Quelle est l'unité de code testée lors d'un test unitaire ?
141.	Quelles sont les caractéristiques d'un bon test unitaire ?
142.	Qu'est-ce qu'une assertion dans un test unitaire ?
 
## English

1)	What does JavaScript enable you to do on a website ?
a.	Add interactive behavior and dynamic content
b.	Define the layout and design of web pages
c.	Handle server-side operations
2)	Which programming language is primarily used for server-side web development ?
a.	PHP
b.	JavaScript
c.	HTML
3)	What is the purpose of a web browser ?
a.	To render and display web pages
b.	To execute serve-side code
c.	To manage databases
4)	What is the difference between GET and POST methods in HTTP ?
a.	GET retrieves data from a server, while POST submits data to a server
b.	GET submits data to a server, while POST retrieves data from a server
c.	GET and POST methods are interchangeable
5)	What is the purpose of version control systems (e.g., Git) in web development ?
a.	To track changes and manage collaborative development
b.	To optimize website loading speed
c.	To handle server-side scripting
6)	What is the purpose of a framework in web development ?
a.	To provide a structured environment for building web applications
b.	To handle network protocols and data transfer
c.	To create visual designs and layouts for websites
7)	What does NoSQL stand for ?
a.	Not Only SQL
b.	Non-Structured Query Language
c.	New Object-Oriented Language
8)	Which of the following is a characteristic of NoSQL databases ?
a.	Strict schema enforcement
b.	Support for complex transactions
c.	Scalability and flexible data models