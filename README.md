Java EE
===

**Lundi**
veille sur java EE(Servlet & Jsp)

Demo projet Bank par groupe

Masterclass Laurent sur Internet

Téléchargement et intégration de Tomcat à Eclipse + Crée un nouveau WorkSpace JavaEE

17.1 Réaliser votre première appli web avec une page html simple qui affiche bonjour et bienvenue

17.2 Réaliser votre 1ère Servlet dans un projet javaJEE, ajouter le package co.simplon.web, puis insérer donc votre servlet Login.java en prenant soin d'y associer l'url mapping "/login". Executer votre programme, qu'observez vous ?

17.3 Ajouter à votre servlet tout ce qui vous permettra d'afficher une page html complète contenant les balises indispensables ainsi qu'un titre avec un message de bienvenue + date + inviter l'utilisateur à s'identifier en saisissant Login + password comme sur l'image :

 ![center](/log.png)

17.4 Au clic, si le login et le password correspondent à ceux que vous avez écrit en dur dans votre servlet, afficher connecté sinon revenir sur votre formulaire !

17.5 Trouver un moyen d'éviter de perdre les informations du formulaire une fois cliqué

18.1 Réaliser votre 1ère Jsp qui reprend à l'identique le programme précédent

Que Constatez vous ?

**Mardi**
veille sur le protocole Http & le pattern MVC

19.1 En vous inspirant du projet précédent, réaliser un nouveau projet "Mvc" par ex et mettez en oeuvre le pattern Mvc de sorte que l'utilisateur puisse ouvrir une session si login + password ok. Vous ouvrirez une nouvelle page Connected.jsp qui affichera un message de bienvenu ...
le **Controleur** est une servlet qui reçoit les requêtes http puis crée un objet HttpSession qui représentera notre **Modèle** contenant donc les informations de session, qui seront utilisées par la **Vue** une fois qu'elle sera appelé par le controleur.

NB : Votre servlet "Controleur.java" ne doit contenir que du code java in fine et votre "Vue.jsp" doit contenir un minimum de code.

19.2 En utilisant l'Expression Language (EL) trouver un moyen d'injecter directement les valeurs de la session courante (login/password)

19.3 De même, dans Connected.jsp, en utilisant le moteur de liaison de donnée, injecté le login courant dans votre message de bienvenu Mr ???

19.4 N'hésitez pas à habiler vos pages à l'aide d'une feuille de style à ajouter dans le WebContent du projet

19.5 Utiliser le mécanisme des web Listener pour compter le nombre de sessions en court et trouver un moyen de limiter la durée d'une session à 1 minute par ex pour vérifier si le mécanisme fonctionne.

**Mercredi**
1- veille sur l'expression des besoins et Cahier des charges
2- WebListener/WebFilter...

Ce petit programme est une synthèse de tout ce que nous avons vu. Il faudra proposer à l'utilisateur de saisir login + pwd, s'il existe dans la table des utilisateurs de la base de donnée WebShop, il aura accès à notre petite boutique en ligne qui affiche les articles de la table des articles qu'on peut parcourir grâce à aux boutons Suivant et Précédent :

 ![center](/badlog.png)
 
 Et si vous êtes bien un des utilisateurs en base qui a accés, vous pourrez parcourir les articles comme ici :
 
 ![center](/panier.png)


Pour résumé, la servlet Controleur reçoit les demandes de connection, si c'est bon, elle renvoi vers une page jsp qui affichera les articles.
N'hésitez pas à habiller vos pages avec fichier css et(ou) framework...

NB : Utiliser le fichier Web.xml pour configurer l'accès à votre base de donnée, celle-ci sera initialisée dans la méthode init de votre servlet.

**Jeudi**
1- veille sur les spécifications générales ou fonctionnelles
2- EL & JSTL

*RETOUR DANS VOS GROUPE UTILISANT SCRUM CETTE FOIS-CI : DEUXIEME SPRINT*

Créer un projet "OnlineBank" qui doit contenir les couches Dao et Métier de votre projet Bank
Il faut ici développer la couche Web !

20.1 Tout d'abord, assurez vous que votre projet est bien opérationnel et répond donc aux spécifications fonctionnelles :

° chaque compte est défini par un code, un solde et une date de création

° un compte courant est un compte avec la particularité d’avoir un découvert

° un compte épargne est un compte avec la particularité d’avoir un taux d’intérêt

° chaque compte appartient à un client

° chaque client est défini par son code, son nom et son prénom

° chaque compte peut subir plusieurs opérations

° il existe 2 types d’opérations : versement + retrait

° une opération est définie par un numéro, une date et un montant

Voir les diagrammes de classes ci dessous :

![center](/diagram.png)

20.2 Il y a 2 types d'utilisateurs, admin ou user, pour le moment concentrons nous sur le deuxième qui peut consulter les comptes aussi ajouter une table en base qui corresponde, elle ressemble fortement à T_Users que nous avons déjà rencontré.

20.3 Votre appli débutera donc par une demande d'authentification et devra ressembler à cela dans un premier temps :

![center](/onlineBank.png)

NB : COMMENCER PAR ENUMERER LES TACHES (POST IT) / UTILISER GIT & GITHUB(PROJECT) POUR GERER LE TRAVAIL D'EQUIPE

**Vendredi**
1- Spécifications techniques ou conception détaillée
2- Attaques XSS

Terminer tous les travaux de la semaine et envoyer sur Github au plutard dimanche minuit

Préparation OPQUAST

Rdv avec les entreprises

Démarches de recherches de stages & alternances

**Ressources**

[Java Platform, Enterprise Edition (Java EE) \| Oracle Technology Network | Oracle](https://www.oracle.com/technetwork/java/javaee/overview/index.html)

[KooR.fr - Un ensemble de ressources pédagogiques pour la plate-forme Java EE](http://koor.fr/Java/JavaEE.wp)

https://agiliste.fr/guide-de-demarrage-scrum/

