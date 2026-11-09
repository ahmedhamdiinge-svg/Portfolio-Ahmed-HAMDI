# Publier ce portfolio sur GitHub Pages

Méthode la plus simple, sans ligne de commande, en 5 minutes.

## A. Créer le dépôt

1. Aller sur [github.com/new](https://github.com/new).
2. **Repository name** : `portfolio-v5`
3. **Public** (obligatoire pour GitHub Pages gratuit).
4. Ne rien cocher (pas de README, pas de .gitignore, pas de licence) → **Create repository**.

## B. Envoyer les fichiers

### Sans ligne de commande (recommandé)

1. Sur la page du dépôt vide : **uploading an existing file**.
2. Glisser **tout le contenu** du dossier `portfolio-v5-github/`
   (`index.html`, `assets/`, `README.md`, `.nojekyll`, `LICENSE`, `.gitignore`, les aperçus).
3. **Commit changes**.

> Glisser le dossier entier, pas le zip : GitHub Pages doit voir `index.html` à la racine.

### Avec Git

```bash
cd portfolio-v5-github
git init
git add .
git commit -m "Portfolio v5 — édition Atelier"
git branch -M main
git remote add origin https://github.com/VOTRE-COMPTE/portfolio-v5.git
git push -u origin main
```

## C. Activer GitHub Pages

1. Dépôt → **Settings** → **Pages**.
2. *Build and deployment* → **Source** : `Deploy from a branch`.
3. *Branch* : **main**, dossier **/(root)** → **Save**.
4. Attendre 1 à 2 minutes, puis recharger la page : l'adresse s'affiche en haut.

## D. Votre lien

```
https://VOTRE-COMPTE.github.io/portfolio-v5/
```

À mettre dans le CV, LinkedIn (section « Site web ») et les candidatures.

## Vérifications utiles

- Ouvrir le lien en navigation privée : le site doit s'afficher en entier.
- Tester la bascule jour/nuit, FR/EN, une vidéo, un plan PDF.
- Si une page s'affiche sans style : vérifier que le dossier `assets/` a bien été envoyé
  et que `.nojekyll` est présent à la racine.

## Mettre à jour plus tard

Modifier les fichiers localement, puis :

```bash
git add .
git commit -m "Mise à jour du portfolio"
git push
```

GitHub Pages republie automatiquement en une minute.

## Nom de domaine personnel (facultatif)

Acheter un domaine (ex. `ahmed-hamdi.fr`), puis dans **Settings → Pages → Custom domain**,
saisir le domaine et créer chez le registrar l'enregistrement `CNAME` vers
`VOTRE-COMPTE.github.io`. Cocher **Enforce HTTPS**.
