# Git & GitHub – Guide des commandes essentielles

## Introduction

Git est un système de gestion de versions qui permet de suivre les modifications d'un projet. Il est utilisé avec GitHub pour sauvegarder le code en ligne, collaborer avec d'autres développeurs et gérer les différentes versions d'un projet.

---

# 1. Configuration de Git

## Vérifier la version de Git

```bash
git --version
```

**Rôle :** Affiche la version de Git installée.

---

## Configurer son nom

```bash
git config --global user.name "Votre Nom"
```

**Rôle :** Définit le nom qui apparaîtra dans les commits.

---

## Configurer son adresse e-mail

```bash
git config --global user.email "vous@example.com"
```

**Rôle :** Définit l'adresse e-mail utilisée dans les commits.

---

## Vérifier la configuration

```bash
git config --list
```

**Rôle :** Affiche tous les paramètres de configuration Git.

---

# 2. Créer un dépôt Git

## Initialiser un dépôt

```bash
git init
```

**Rôle :** Transforme le dossier courant en dépôt Git.

---

## Cloner un dépôt

```bash
git clone <url_du_depot>
```

Exemple :

```bash
git clone https://github.com/utilisateur/projet.git
```

**Rôle :** Télécharge un dépôt GitHub sur votre ordinateur.

---

# 3. Vérifier l'état du projet

## Voir l'état du dépôt

```bash
git status
```

**Rôle :**

* Affiche les fichiers modifiés.
* Affiche les fichiers non suivis.
* Indique les fichiers prêts à être validés.

---

## Voir les branches

```bash
git branch
```

**Rôle :** Affiche toutes les branches locales.

---

## Voir les branches distantes

```bash
git branch -r
```

**Rôle :** Affiche les branches présentes sur GitHub.

---

## Voir toutes les branches

```bash
git branch -a
```

**Rôle :** Affiche les branches locales et distantes.

---

# 4. Ajouter des fichiers

## Ajouter un fichier

```bash
git add fichier.txt
```

**Rôle :** Prépare un fichier pour le prochain commit.

---

## Ajouter tous les fichiers

```bash
git add .
```

**Rôle :** Prépare tous les fichiers modifiés.

---

# 5. Enregistrer les modifications

## Créer un commit

```bash
git commit -m "Message du commit"
```

**Rôle :** Enregistre définitivement les modifications dans l'historique Git.

Exemple :

```bash
git commit -m "Ajout de la page contact"
```

---

# 6. Historique

## Voir les commits

```bash
git log
```

**Rôle :** Affiche tout l'historique.

---

## Historique résumé

```bash
git log --oneline
```

**Rôle :** Affiche les commits sur une seule ligne.

---

## Historique graphique

```bash
git log --oneline --graph --all
```

**Rôle :** Affiche l'historique sous forme d'arbre.

---

# 7. Les branches

## Créer une branche

```bash
git branch nouvelle-branche
```

**Rôle :** Crée une branche sans changer de branche.

---

## Créer une branche et basculer dessus

```bash
git switch -c nouvelle-branche
```

ou

```bash
git checkout -b nouvelle-branche
```

**Rôle :** Crée une branche puis s'y place.

---

## Changer de branche

```bash
git switch main
```

ou

```bash
git checkout main
```

**Rôle :** Bascule vers une autre branche.

---

## Supprimer une branche

```bash
git branch -d nom-branche
```

**Rôle :** Supprime une branche déjà fusionnée.

---

## Supprimer une branche distante

```bash
git push origin --delete nom-branche
```

**Rôle :** Supprime une branche sur GitHub.

---

# 8. Envoyer le code sur GitHub

## Ajouter un dépôt distant

```bash
git remote add origin <url_du_depot>
```

Exemple :

```bash
git remote add origin https://github.com/utilisateur/projet.git
```

**Rôle :** Associe le dépôt local au dépôt GitHub.

---

## Vérifier les dépôts distants

```bash
git remote -v
```

**Rôle :** Affiche les URL des dépôts distants.

---

## Premier envoi

```bash
git push -u origin main
```

**Rôle :**

* Envoie la branche `main`.
* Associe la branche locale à la branche distante.

---

## Envoyer les modifications

```bash
git push
```

**Rôle :** Envoie les nouveaux commits vers GitHub.

---

# 9. Télécharger les modifications

## Récupérer les nouveautés

```bash
git fetch
```

**Rôle :**

Télécharge les nouvelles informations depuis GitHub sans modifier votre branche.

---

## Télécharger et fusionner

```bash
git pull
```

**Rôle :**

Équivaut à :

```bash
git fetch
git merge
```

Télécharge puis fusionne les modifications.

---

# 10. Fusionner des branches

## Fusion

```bash
git merge nom-branche
```

Exemple :

```bash
git merge feature/login
```

**Rôle :** Intègre une branche dans la branche courante.

---

## Rebase

```bash
git rebase main
```

**Rôle :** Replace les commits de la branche courante après les derniers commits de `main`.

---

# 11. Résoudre un conflit

Après un conflit :

```bash
git add README.md
```

Puis :

```bash
git commit -m "Resolve merge conflict"
```

**Rôle :** Valide la résolution du conflit.

---

# 12. Annuler des modifications

## Restaurer un fichier

```bash
git restore fichier.txt
```

**Rôle :** Annule les modifications non validées.

---

## Retirer un fichier de la zone de préparation

```bash
git restore --staged fichier.txt
```

**Rôle :** Retire un fichier ajouté avec `git add`.

---

# 13. Mettre des modifications de côté

## Sauvegarder temporairement

```bash
git stash
```

**Rôle :** Met les modifications de côté sans créer de commit.

---

## Récupérer les modifications

```bash
git stash pop
```

**Rôle :** Restaure les modifications sauvegardées.

---

# 14. Ignorer des fichiers

Créer un fichier :

```bash
touch .gitignore
```

Exemple :

```
.env
node_modules/
*.log
```

**Rôle :** Empêche Git de suivre certains fichiers ou dossiers.

---

# 15. Fork

Le Fork se fait sur GitHub.

**Rôle :**

Créer une copie d'un dépôt dans votre propre compte GitHub afin de pouvoir travailler dessus sans modifier le dépôt original.

---

# 16. Clone

```bash
git clone <url>
```

**Rôle :**

Télécharger un dépôt GitHub sur votre ordinateur.

---

# 17. Pull Request

Une Pull Request permet de demander la fusion d'une branche dans une autre.

Exemple :

```
feature/login
        │
        ▼
Pull Request
        │
        ▼
main
```

Elle permet :

* la relecture du code ;
* les commentaires ;
* les tests ;
* la validation avant la fusion.

---

# 18. Merge

Le Merge intègre les modifications d'une branche dans une autre.

Exemple :

```bash
git merge feature/login
```

---

# 19. Issue

Une Issue représente une tâche ou un problème.

Exemple :

```
#12 Ajouter une page Contact
```

Elle sert à :

* organiser le travail ;
* suivre les bugs ;
* demander une amélioration.

---

# 20. Wiki

Le Wiki est un espace de documentation du projet.

Il permet d'écrire :

* les guides d'installation ;
* l'architecture ;
* les guides utilisateurs ;
* les guides développeurs.

---

# 21. Workflow Git recommandé

```text
Créer un dépôt
        │
        ▼
git clone
        │
        ▼
Créer une branche
        │
        ▼
Modifier les fichiers
        │
        ▼
git add
        │
        ▼
git commit
        │
        ▼
git push
        │
        ▼
Créer une Pull Request
        │
        ▼
Relecture
        │
        ▼
Merge
        │
        ▼
git pull sur les autres machines
```

---

# Résumé des commandes les plus utilisées

| Commande        | Rôle                                              |
| --------------- | ------------------------------------------------- |
| `git init`      | Initialiser un dépôt                              |
| `git clone`     | Télécharger un dépôt                              |
| `git status`    | Voir l'état du projet                             |
| `git add`       | Préparer les fichiers                             |
| `git commit`    | Enregistrer les modifications                     |
| `git push`      | Envoyer les commits vers GitHub                   |
| `git pull`      | Télécharger et fusionner les modifications        |
| `git fetch`     | Télécharger les nouveautés sans les fusionner     |
| `git branch`    | Afficher les branches                             |
| `git switch`    | Changer de branche                                |
| `git switch -c` | Créer et changer de branche                       |
| `git merge`     | Fusionner une branche                             |
| `git rebase`    | Réorganiser les commits sur une base plus récente |
| `git remote -v` | Afficher les dépôts distants                      |
| `git stash`     | Mettre des modifications de côté                  |
| `git restore`   | Annuler des modifications locales                 |
| `git log`       | Consulter l'historique des commits                |
