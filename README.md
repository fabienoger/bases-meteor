# Bases Meteor JS


Nous allons découvrir Meteor qui est un framework JavaScript qui permet de faire des Web Apps ou encore des applications mobiles hybrides.
Tout d'abord MeteorJS vous permet d'écrire du JavaScript côté client et côté serveur grâce à NodeJS.

## Pourquoi Meteor ?
* Meteor n'envoie pas de code HTML, il envoie des données au client qui va se charger d'afficher les données.
* Un seule language pour le côté client et le côté serveur.
* Vous pouvez accéder à la base de donnée côté client grâce à Mini Mongo.
* Meteor est en temps réel c'est à dire que les données changent automatique sur le navigateur de l'utilisateur (le client).
* Meteor est open-source (https://github.com/meteor/meteor "GitHub") et comptent plus de 250 contributeurs.

## Installation
Pour installer Meteor éxécuter la commande suivante dans votre terminal :
`curl https://install.meteor.com/ | sh`

Une fois installer vous pouvez créer un projet :
`meteor create myApp`

Ensuite éxécuter votre application en local :
```
cd myapp
meteor npm install
meteor
// Meteor server running on: http://localhost:3000/
```


## Packages

Dans une application Meteor vous pouvez ajoutez des packages.
Ces packages sont de petites librairies construites qui vous permettent d'intégrer directement un système de connexion et authentification, une librairie existante ou un framework (Bootstrap, semantic-ui).
Il existe un site qui repertorie tous les packages : (https://atmospherejs.com/ "Atmosphere").
Vous pouvez vous aussi créer votre packages (http://guide.meteor.com/writing-atmosphere-packages.html "guide").

### Nom du package
Excepté les packages de la plate-forme Meteor, tous les packages sur (https://atmospherejs.com/ "Atmosphere") ont un préfixe *prefix:package-name*.
Le préfixe est le nom d'utilisateur du développeur Meteor ou de l'organisation qui a publié le package.

### Installer un package Atmoshpere
`meteor add prefix:package-name`

### Désinstaller un package Atmoshpere
`meteor remove prefix:package-name`


## Structure de l'application

Lorsque Meteor va s'executer il va compiler tous les fichiers qui se trouvent dans votre application.
Après avoir créer votre application Meteor vous pouvez voir que Meteor a déjà généré des dossier et fichiers.

```
- .meteor
- client
  - main.css
  - main.html
  - main.js
- package.json
- server
  - main.js
```

Meteor génère également un dossier caché: *.meteor*
Il ne faut **jamais** modifier directement des fichiers de ce dossier, il permet de faire fonctionner Meteor.

### Le nom des dossiers et fichiers

Les fichiers et dossiers ne vont pas être exécuter au même moment selon leur nom :

* Les fichiers se trouvant dans le dossier */client* seront exécutés uniquement sur le navigateur.
* Les fichiers se trouvant dans le dossier */server* seront exécutés uniquement sur le serveur.
* Vous pouvez créer un dossier */both* qui s'exécutera côté client et serveur.
* Le dossier */lib* est exécuté en premier
* Les fichiers __main.*__ sont exécutés en dernier.
* Le dossier */public* contient les éléments publics (images, vidéos, fonts).