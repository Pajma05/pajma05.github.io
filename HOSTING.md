# Héberger ton portfolio

Ton site est **100 % statique** : 2 fichiers (`index.html` + `photo.png`), aucune
dépendance, aucun serveur à faire tourner. Tu peux donc l'ouvrir en local
(double-clic sur `index.html`) et l'héberger n'importe où.

## Le plus simple, gratuit, avec ta propre URL

Pour un site statique, c'est ce que fait la quasi-totalité des devs. Tu gardes le
contrôle du code, c'est gratuit, HTTPS automatique.

### Option A — Cloudflare Pages ou Netlify (glisser-déposer, 2 min)
1. Crée un compte sur **Netlify** (netlify.com) ou **Cloudflare Pages**.
2. Glisse le dossier `portfolio/` dans la zone de dépôt.
3. Tu obtiens une URL du type `marie-caze.netlify.app`. Terminé.

### Option B — GitHub Pages (versionné, pro)
1. Crée un dépôt GitHub `portfolio` (ça te fait au passage un projet public !).
2. Pousse `index.html` et `photo.png` à la racine.
3. Repo → **Settings → Pages** → Source = branche `main` / dossier `/root`.
4. URL : `https://<ton-pseudo>.github.io/portfolio/`.

## Avoir une adresse pro : `mariecaze.dev`
Achète un domaine (~10 €/an) chez **OVH**, **Namecheap** ou **Cloudflare Registrar**
(`mariecaze.fr`, `.dev`, `.me`…), puis branche-le sur l'hébergeur choisi ci-dessus
(chacun a une doc « custom domain » en 3 clics). C'est ce qui fait le plus sérieux
sur un CV.

## Le vrai « self-host » (plus tard, si tu veux)
Un site statique n'en a pas besoin, mais si tu veux tout maîtriser :
- **VPS** (Hetzner ~4 €/mois, OVH…) : installe **Caddy** (HTTPS auto) ou nginx,
  copie les fichiers dans le dossier servi. ~15 lignes de config.
- **Raspberry Pi à la maison** + un domaine + DDNS : le plus « self-host », mais
  dépend de ta connexion et demande un peu d'administration.

👉 **Ma reco** : commence par **GitHub Pages** (Option B) — gratuit, et ça te crée
en plus un repo public à montrer. Tu ajoutes un domaine perso quand tu veux.

## Mettre à jour le site
- **Ajouter/modifier un projet** : édite le tableau `PROJECTS` dans `index.html`
  (tout en bas). Un objet = un projet.
- **Boutons d'un projet** : dans `links`, chaque lien a un `type` :
  - `demo` → bouton turquoise (site en ligne),
  - `download` → bouton rose (fichier à télécharger),
  - `code` → bouton contour rose (dépôt de code).
- **Fichiers à télécharger** : dépose-les dans le dossier **`files/`** et pointe le
  lien dessus, ex. `url:"files/hidden-world.zip"`. (Les jeux ont déjà un bouton
  Télécharger qui attend son fichier dans `files/`.)
- **Changer ta photo** : remplace `photo.png`.
- **Ajouter ton CV** : mets `cv.pdf` à côté de `index.html` et décommente la ligne
  `<a class="btn" href="cv.pdf">CV (PDF)</a>` dans le hero.

## À compléter (infos qui me manquaient)
- **Sidequest** : la stack technique (tag `[À COMPLÉTER]`).
- **PPEX 4** : le moteur utilisé (tag `[À COMPLÉTER]`).
- **Builds des jeux** : ajoute `hidden-world.zip` / `tower-of-time.zip` dans `files/`,
  ou remplace ces liens `download` par des liens `demo`/`code`, sinon supprime-les.
- Liens **démo / code** pour GOAT, JWS, 42sh, etc. si tu veux les rendre publics.
