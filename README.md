# Site Build (serveurs Minecraft)

## 1. Mettre en ligne sur GitHub Pages
1. Crée un dépôt GitHub public (ex. `build-minecraft`).
2. Envoie-y **tout le contenu** de ce dossier (y compris `.nojekyll`).
3. Settings > Pages > Source : *Deploy from a branch* > `main` / `(root)` > Save.
4. Ton site sera sur `https://TON-PSEUDO.github.io/build-minecraft/`.

## 2. Référencement Google (obligatoire pour être trouvé)
1. Remplace `https://VOTRE-PSEUDO.github.io/NOM-DU-REPO` par ta vraie URL dans : `index.html`, `robots.txt`, `sitemap.xml`.
2. Va sur https://search.google.com/search-console, ajoute ton URL (propriété « Préfixe d’URL »).
3. Menu Sitemaps > ajoute `sitemap.xml`, puis « Inspection de l’URL » > « Demander une indexation ».
Compte quelques jours à quelques semaines pour apparaître.

## 3. Activer /admin (modifier le site pour tout le monde)
Adresse : `https://TON-URL/admin/` — code d’accès : `Build2026`.
Pour que « Enregistrer » modifie le site de tout le monde, crée un token (une seule fois) :
1. GitHub > Settings > Developer settings > Personal access tokens > **Fine-grained tokens** > Generate new token.
2. Repository access : *Only select repositories* > ton dépôt.
3. Permissions > Repository permissions > **Contents : Read and write**.
4. Copie le token (`github_pat_...`) dans /admin > « Connexion GitHub ». Il reste dans ton navigateur uniquement.
Les modifications apparaissent 1 à 2 minutes après l’enregistrement.

## Sécurité
Le code `Build2026` est vérifié dans le navigateur : il sert de barrière d’accès, pas de vraie sécurité. La vraie protection, c’est le token GitHub : sans lui, personne ne peut modifier le site. Ne le partage jamais.

## Boutique et règles
Pages `/boutique/` et `/regles/`, modifiables depuis /admin (grades, prix, avantages, liens de paiement, règlement).
Attention : Aternos n’autorise pas de gagner de l’argent réel avec un serveur, et Mojang interdit de vendre des avantages en jeu (cosmétique uniquement).
Garde donc des prix en monnaie du jeu tant que tu es sur Aternos. Si tu passes sur un hébergeur payant, mets un prix en euros et colle un lien de paiement (Tebex, Stripe, PayPal) dans /admin. Pense aussi aux obligations légales de la vente en ligne (CGV, statut).
