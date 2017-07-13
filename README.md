[![GitHub license](https://img.shields.io/badge/license-New%20BSD-blue.svg)](https://github.com/Fukotaku/files-manager/blob/master/LICENSE)
# files-manager

files-manager est une application web développé en php qui permet de gérer vos fichiers présents sur le serveur en http (Upload/Download). L'application dispose de divers fonctionnalités, comme le visionnage de vidéo et le partage de dossiers entre utilisateur.

Pour toutes contribution sur github, merci de lire le document [CONTRIBUTING.md](https://github.com/Fukotaku/files-manager/blob/master/CONTRIBUTING.md).


## Objectifs

- [ ] Comptes utilisateur.
- [ ] Panel d'administration.
- [ ] Upload de fichiers.
- [x] Bar de progression d'upload.
- [ ] Téléchargement des fichiers.
- [ ] Visualisation des fichiers type (vidéo/image/musique/pdf...).
- [ ] Partage de dossier entre utilisateur.
- [ ] Possibilité d'accès à des répertoires du serveur.
- [ ] Mise en place de logs au panel admin.


## Pre-requis

- php 5.6+
  - extension pdo
  - extension mbstring  


## Librairies/outils

Projet basé sur le template [Fukotaku/fufu](https://github.com/Fukotaku/fufu/)


## Installation

Via git

``` bash
$ git clone https://github.com/Fukotaku/files-manager
```

Via composer

``` bash
$ composer install
```

Vérifiez que le fichier `.env` a bien été créé, il s'agit du fichier de configuration de votre environnement ou vous définissez la connexion à la base de données, l'environnement `local` ou `prod` et l'activation du cache de twig.

Si jamais le fichier n'a pas été créé, faite le manuellement en dupliquant `.env.example`.

Effectuer la migration des tables via les commandes `phinx`

``` bash
$ vendor/bin/phinx migrate
```

``` bash
$ vendor/bin/phinx seed:run
```


## Permissions

Autoriser le dossier `cache` à l'écriture (chmod 775).