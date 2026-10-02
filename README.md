# People Scoop! N°1 · Spécial Estelle

Magazine feuilletable en ligne : les pages se tournent comme un vrai journal.

## Contenu du dossier

```
index.html            la page du site (tout le code est dedans)
pages/page-01.jpg …   les 16 pages du magazine en image
js/                   les deux bibliothèques utilisées (tournage des pages, confettis)
people-scoop-n1.pdf   le PDF, téléchargeable depuis le bouton du site
og-image.jpg          l'aperçu affiché quand on partage le lien (WhatsApp, Messenger…)
.nojekyll             fichier vide nécessaire à GitHub Pages
```

## Tester sur ton ordinateur

Double-clique sur `index.html`. Si les pages ne s'affichent pas, ouvre un terminal dans le dossier et lance :

```
python3 -m http.server 8000
```

puis va sur http://localhost:8000

## Mettre en ligne gratuitement avec GitHub Pages

1. Crée un compte sur https://github.com (gratuit).
2. Clique sur **New repository** (le bouton « + » en haut à droite).
   - Nom : par exemple `people-scoop`
   - Coche **Public** (GitHub Pages gratuit demande un dépôt public)
   - Clique sur **Create repository**
3. Sur la page du dépôt, clique sur **uploading an existing file**.
4. Glisse **tout le contenu du dossier** (index.html, les dossiers pages et js, le PDF, og-image.jpg, .nojekyll), puis clique sur **Commit changes**.
   - Glisse le contenu, pas le dossier lui-même : `index.html` doit être à la racine du dépôt.
   - Le fichier `.nojekyll` est caché sur Mac/Windows. S'il ne part pas, ce n'est pas grave, le site marche quand même.
5. Va dans **Settings → Pages**.
   - Source : **Deploy from a branch**
   - Branch : **main**, dossier **/(root)**, puis **Save**
6. Attends 1 à 2 minutes et recharge la page : l'adresse s'affiche en haut, du type
   `https://ton-pseudo.github.io/people-scoop/`

Pour modifier une page plus tard : remplace l'image dans `pages/` par une nouvelle avec le même nom, et le site se met à jour en une minute.

### Avec la ligne de commande (si tu connais git)

```
cd people-scoop
git init
git add .
git commit -m "People Scoop N°1"
git branch -M main
git remote add origin https://github.com/TON-PSEUDO/people-scoop.git
git push -u origin main
```

Puis active Pages comme à l'étape 5.

## Alternatives sans GitHub

- **Netlify Drop** : va sur https://app.netlify.com/drop et glisse le dossier entier. Le site est en ligne en 10 secondes (créer un compte gratuit permet de le garder).
- **Vercel** ou **Cloudflare Pages** : même principe, gratuit aussi.

## Confidentialité

- Le site contient des photos de vraies personnes. Sur GitHub Pages, toute personne qui a le lien peut le voir, et le dépôt public est visible sur ton profil GitHub.
- La balise `noindex` dans `index.html` demande à Google de ne pas le référencer.
- Pense à demander leur accord aux personnes photographiées, et supprime le dépôt après la fête si tu préfères.

## Personnaliser

En haut du `<script>` dans `index.html` :
- `PAGE_COUNT` : le nombre de pages
- `SOMMAIRE` : les entrées du sommaire (numéro de page, rubrique, titre)

Commandes du site :
- flèches du clavier, ou glisser/cliquer sur les coins pour tourner les pages
- bouton sommaire, plein écran, confettis, téléchargement du PDF
- des confettis partent aussi à l'ouverture et à la dernière page
