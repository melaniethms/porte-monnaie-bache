# Porte-monnaie origami en bâche recyclée

Tutoriel pas à pas du FabLab La Chaux-de-Fonds : patron à télécharger (A3, A4 à assembler, source), illustrations, extraits vidéo et vidéo complète.

Conception et tutoriel : Mélanie Thomas. Contenu sous licence CC BY-SA 4.0.

## Contenu du dépôt

```
index.html            la page (HTML + CSS + JS dans un seul fichier, sans dépendance externe)
img/                  logo, couverture, illustrations, photos d'atelier, aperçu SVG du patron
clips/                10 extraits vidéo muets (MP4, ~150 Ko) + leurs vignettes
patron/               patron A3, patron A4 en 4 feuilles, PDF source
.nojekyll             indique à GitHub Pages de servir les fichiers tels quels
```

La vidéo complète reste sur YouTube (`ExNKUP6Dmn8`). Elle se charge en mode sans cookies, et seulement au clic.

## Mise en ligne avec GitHub Pages

1. Crée un dépôt (par exemple `porte-monnaie-bache`) et pousse-y le contenu de ce dossier.
2. Dans le dépôt, ouvre **Settings → Pages**, choisis la source **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`.
3. Au bout d'une minute, la page est en ligne à l'adresse `https://<ton-compte>.github.io/porte-monnaie-bache/`.

## Modifier

- **Chapitres et liens « Voir dans la vidéo »** : ce sont les attributs `data-t="…"` (en secondes) dans `index.html`.
- **Extraits** : recoupe-les depuis la vidéo source, par exemple avec :
  `ffmpeg -ss 1:48 -i video.mp4 -t 7 -an -vf scale=360:640 -c:v libx264 -crf 30 -movflags +faststart clips/poche-1.mp4`
- **Police** : la page utilise *GT Pressura* si elle est installée sur l'appareil, sinon la police système. Pour l'imposer partout, ajoute les fichiers `.woff2` (si la licence le permet) et une règle `@font-face`.
