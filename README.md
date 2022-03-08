# LeBrignolaisSportif

Présentation du Projet “Le Brignolais Sportif”


## 1 Présentation.

La ville de Brignoles regorge d'activités et même de potentiels qui ne sont que trop peu souvent mis en avant. L'idée du Brignolais sportif est donc de rencontrer, de faire découvrir, d'exposer toutes ces associations sportives qui enrichissent la capitale de la Provence Verte ainsi que les hommes, les femmes et les enfants passionnés qui les font vivre. A travers ce journal, l'ensemble des associations sportives brignolaises référencées comme telles, seront mises en lumière ainsi que leurs milliers de licenciés, dirigeants et bénévoles actifs. Ce journal a pour objectif de partager, de faire connaître et d'inviter à découvrir ces clubs et ces gens qui font vivre notre ville par le sport associatif.

Le but de notre projet est de rendre une application fonctionnelle pour ce journal, qui est principalement actif via sa page Facebook. Cette application pourra être utilisée par tout les utilisateurs de ce réseau afin de pouvoir parcourir les évènements passés/à venir, échanger sur les résultats de ces derniers via des commentaires, lire les éditions numériques du journal et recevoir des newsletters avec un condensé des éléments qui ont été publiés récemment sur la plateforme.


## 2. Parcours utilisateur

### 2.1. Utilisateur prenium
| Accueil | Articles | Evenements | Journal numérique | dropdown: Editer le profil/Se déconnecter |
Les utilisateurs premium ont accès à tous les articles et évènements (ainsi qu'à leurs commentaires et la possibilité de commenter ceux-ci). Ils auront la possibilité de mettre des sports favoris afin d'être informés de la mise en ligne d'un article ou d'un événement de leurs sports favoris.

### 2.2. Utilisateur connecté
| Accueil | Articles | Evenements | Journal numérique | Souscrire à un abonnement  | dropdown: Editer le profil/Se déconnecter |
Les utilisateurs connectés ont accès aux articles et événements de la semaine (sans avoir la possibilité de les commenter), la version numérique du journal du mois en cours et reçoivent une newsletter hebdomadaire. Ils auront également la possibilité de devenir un utilisateur premium via une page dédiée.

### 2.3. Utilisateur non-connecté
| Accueil | dropdown: S'enregistrer/Connexion |
Les utilisateurs non enregistrés sur l'application auront accès uniquement à la page d'accueil et à une page les menant à un formulaire d'inscription.


##3 Concrètement et techniquement.

###3.1 Base de données.

La BDD sera constituée sous PostgreSQL, composée des éléments suivants (“models” sous Rails) :

Users/Admins
Il sera possible de parcourir l’application de trois manières différentes :
Utilisation sans connexion à un compte User ;
Utilisation via un compte User
Utilisation via un compte User Premium
Articles
Chaque User et User Premium pourront poster des Articles 
Comments
Il sera possible (sous compte User et User Premium) de commenter les Articles.
Ces comments pourront à leur tour être commentés par un User ou User Premium.
En revanche, le contenu des comments pourra être vérifié par l’application afin d’empêcher l’utilisation de mots portant atteinte aux règles de bonne conduite au sein d’une communauté d’internautes (insultes, …etc) 
Events

Ces éléments seront connectés les uns aux autres après une étude en équipe du ActiveRecordAssociation (module Rails)  le plus pertinent pour rendre l’application fonctionnelle, et ce via l’outil Lucidchart.

### 3.2. Front. (propositions by Sam ?)

L’application sera désignée sur le thème du sport
Propositions :
Un logo inspiré éventuellement d’un élément d’un sport en particulier (ballon de foot, ou autre…)
Une couleur dominante évoquant l’atmosphère d’un sport populaire (le vert d’une pelouse d’un stade de foot, ou encore une couleur terre battue faisant écho à terrains de tennis de Roland - Garros ?)

Un Kit UI sera constitué pour fournir la base première de couche CSS de l’application
Une utilisation de Bootstrap est à prévoir (navbar, landing page, formulaires, cartes …)
Une couche Javascript serait utilisée afin d’apporter un dynamisme supplémentaire à l’UX (User Xperience)


### 3.3 BackEnd.

L’application sera codée via l’utilisation du framework Ruby on Rails, basé sur le langage RUBY.
***
Devise
Stripe
Mailer
Cookies
***

### 3.4 Dream Team

Ici, on se présente !

Commençons par : A COMPLETER (en discours direct ?)
Laissons la deuxième place à :  A COMPLETER (en discours direct ?)
Voici le troisième membre de notre Dream Team :  BONNET Enzo
Et pour finir, accueillons :  A COMPLETER (en discours direct ?)

On est chaud pour vous livrer une App digne de ce nom !!


## 4 MVP.

	Nous prévoyons de livrer une première version minimaliste comprenant les éléments suivants : 

BDD fonctionnelle ;
Utilisateur : Inscription & connexion (Devise), Remember me, accès à la page profil de l’utilisateur, accès aux articles et aux évènements de la semaine (sans les commentaires), réception d’une newsletter hebdomadaire. Possibilité de s’abonner pour devenir Premium (Stripe).
Utilisateur premium : Accès à tous les articles et événements (et aux commentaires qui y sont liés), tri par date et/ou catégorie, possibilité de commenter articles et événements.
Admin : Gestion des Utilisateurs, gestion des commentaires, accès aux commentaires d’un utilisateur en particulier, possibilité de publier articles et événements.
Mailer fonctionnel : envoi d’un mail à l’utilisateur (et à l’admin?) lors de l’inscription / de l’abonnement, possibilité de réinitialiser le mot de passe.
Kit UI basique mais potable.
seed.rb fonctionnel.
Envoi de la newsletter hebdomadaire manuellement.


## 5 Version Finale.

Pour la version finale du site, nous souhaitons implémenter les fonctions suivantes :

Rendre le site responsive.
Automatisation de l'envoi de la newsletter hebdomadaire.
Articles premium (à déterminer par l’admin) dont la totalité du contenu n’est accessible qu’aux utilisateurs premium, les utilisateurs non premium ne pouvant lire qu’un teasing de quelques lignes de l’article.
Possibilité pour les utilisateurs premium de choisir leurs sports favoris : affichage des articles et événements correspondants sur la page d’accueil, et envoi automatique d’un mail à la publication d’un article lié à ces sports. 
Possibilité pour les utilisateurs premium de commenter les commentaires déjà publiés.
Possibilité de réagir aux commentaires par une emote (façon Discord).
Envoi d’un mail lorsque l’abonnement va arriver à expiration.

OPTIONNEL :

Afficher les articles et événements sous forme de carrousel ;
Possibilité pour les utilisateurs premium de créer une ‘liste de lecture’ avec articles et événements.
Filtre des commentaires : remplacer les mots ‘indésirables’ par des **** et donner aux utilisateurs la possibilité de signaler un commentaire.
Scrapping des sites de journaux locaux pour afficher une image contenant le lien vers l’article (= vers le site du journal en question, respect de la propriété intellectuelle).

A terme (= après le rendu de la version finale du projet), nous souhaiterions implémenter un système de cookies publicitaires et/ou de publicité (type "Google Ads") sur le site, qui seraient désactivés pour les utilisateurs premium.


##6 Notre mentor.

Notre mentor, vaillant le bien-aimé jeune disciple de Zuckerberg, j’ai nommé Steve, bachelier ingénieur informatique, passionné des métiers du numériques, de robotique et Top 1 à Fortnite.
Il nous fait l’honneur d’être notre guide, notre lumière dans la pénombre du Ruby et du JS, que nous gravissons ligne par ligne tant bien que mal en espérant voir le bout de cette épique et interminable épopée.
Conseil et accompagnement il pourvoira, nos larmes il sèchera, gros billet il encaissera.
Merci à toi Steve alias @Reiner#5080.
