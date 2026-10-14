# Créer un dépôt GitHub

## 1. Objectif

Cette procédure explique comment créer un dépôt GitHub, le connecter à un projet local et envoyer ses fichiers à l'aide de Git.

## 2. Prérequis

Avant de commencer, il faut disposer de :

- Un compte [GitHub](https://github.com/ "https://github.com/").
- Git installé sur l'ordinateur.
- Un terminal (Git Bash, PowerShell ou celui de VS Code).
- Un dossier contenant le projet à envoyer.

Pour vérifier que Git est installé :

```
git --version
```

## 3. Créer un dépôt sur GitHub

1. Se connecter à [GitHub](https://github.com/ "https://github.com/").
2. Cliquer sur le bouton **New repository**.
3. Renseigner le nom du dépôt (exemple : `MonProjet`).
4. Ajouter éventuellement une description.
5. Choisir la visibilité :
    - **Public** : visible par tout le monde.
    - **Private** : accessible uniquement aux personnes autorisées.
6. Pour cette procédure, ne pas initialiser le dépôt avec un README.
7. Cliquer sur **Create repository**.

Le dépôt distant est maintenant créé.

## 4. Initialiser Git dans le projet local

1. Ouvrir un terminal.
2. Se placer dans le dossier du projet :

```
cd chemin/vers/MonProjet
```

3. Initialiser un dépôt Git local :

```
git init
```

4. Ajouter les fichiers au suivi Git :

```
git add .
```

5. Créer un premier commit :

```
git commit -m "Initial commit"
```

> [!NOTE]  
> Un commit correspond à un enregistrement de l'état du projet à un instant donné.

## 5. Connecter le dépôt local à GitHub

1. Copier l'URL HTTPS du dépôt créé sur GitHub.
2. Ajouter le dépôt distant :

```
git remote add origin https://github.com/UTILISATEUR/MonProjet.git
```

3. Vérifier que le dépôt distant est correctement configuré :

```
git remote -v
```

4. Définir la branche principale :

```
git branch -M main
```

> [!IMPORTANT]  
> Remplacer `UTILISATEUR` et `MonProjet` par les informations réelles du dépôt GitHub.

## 6. Envoyer le projet sur GitHub

1. Envoyer les commits locaux vers le dépôt distant :

```
git push -u origin main
```

2. S'authentifier auprès de GitHub si nécessaire.
3. Actualiser la page du dépôt GitHub.
4. Vérifier que les fichiers du projet sont présents.

L'option `-u` permet d'associer la branche locale `main` à la branche distante `origin/main`.

## 7. Mettre à jour le dépôt

Après avoir modifié des fichiers, il faut enregistrer les changements et les envoyer sur GitHub.

1. Vérifier l'état des fichiers :

```
git status
```

2. Ajouter les modifications :

```
git add .
```

3. Créer un nouveau commit :

```
git commit -m "Description des modifications"
```

4. Envoyer les modifications :

```
git push
```

## 8. Résolution des erreurs courantes

### Repository not found

Cette erreur apparaît lorsque GitHub ne trouve pas le dépôt ou lorsque l'utilisateur ne dispose pas des autorisations nécessaires.

Vérifier l'URL configurée :

```
git remote -v
```

Corriger l'URL si nécessaire :

```
git remote set-url origin https://github.com/UTILISATEUR/MonProjet.git
```

Vérifier également que le dépôt existe et que le compte GitHub utilisé possède les droits d'accès.

### Remote origin already exists

Cette erreur signifie qu'un dépôt distant nommé `origin` est déjà configuré.

Il faut modifier son URL plutôt que de créer un second `origin` :

```
git remote set-url origin URL_DU_DEPOT
```

### Nothing to commit, working tree clean

Ce message signifie qu'aucune modification non enregistrée n'est présente dans le projet.

Il ne s'agit pas d'une erreur.

## 9. Récapitulatif des commandes

|Commande|Description|
|---|---|
|`git init`|Initialise un dépôt Git local|
|`git status`|Affiche l'état du dépôt|
|`git add .`|Ajoute les modifications|
|`git commit -m "message"`|Enregistre un commit|
|`git remote add origin URL`|Associe un dépôt distant|
|`git remote -v`|Affiche les dépôts distants|
|`git branch -M main`|Renomme la branche en main|
|`git push -u origin main`|Effectue le premier envoi|
|`git push`|Envoie les nouveaux commits|
|`git pull`|Récupère et intègre les modifications distantes|

## 10. Conclusion

Le dépôt GitHub est maintenant opérationnel et synchronisé avec le projet local.

Pour les prochaines modifications, les trois commandes principales sont :

```
git add .git commit -m "Description des modifications"git push
```

Ces commandes permettent de conserver un historique des changements et de sauvegarder le projet sur GitHub.

GitHub · Change is constant. GitHub keeps you ahead. · GitHub

Join the world's most widely adopted, AI-powered developer platform where millions of developers, businesses, and the largest open source community build software that advances humanity.