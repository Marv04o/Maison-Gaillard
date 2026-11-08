# Maison Gaillard — site web (maquette v1)

Site vitrine de Maison Gaillard, artisan burger & pokébowl, 74 quai du Général-Leclerc, 13500 Martigues.

**Statut : maquette en cours de validation par le client.** Les passages marqués d’un « ? » sont à confirmer. Le site est volontairement non indexé (`robots.txt`, balise `noindex` et en-tête `X-Robots-Tag`) jusqu’à validation.

## Contenu

- `index.html` — la page unique (HTML, CSS et JavaScript sans dépendance).
- `img/` — photos optimisées en WebP (photos produits du site de commande, photos Instagram du lieu), logo, favicon.
- `fonts/` — polices auto-hébergées (Archivo, Hanken Grotesk, Instrument Serif ; licence SIL Open Font License). Aucun appel à Google Fonts.
- `vercel.json` — URLs propres, cache long pour images et polices, en-têtes de sécurité, non-indexation.

## Lancer en local

Aucune installation n’est nécessaire :

```bash
npx serve .
```

puis ouvrir http://localhost:3000.

## Déploiement

Le dépôt est relié à Vercel : chaque `git push` sur `main` redéploie le site automatiquement.

## Modifications courantes

- **Un prix ou une recette** : chercher le nom du plat dans `index.html` (ex. `Le Truffe`) et modifier le texte ou le prix à côté.
- **Les horaires** : le tableau `horaires` dans `index.html`, et l’objet `H` en bas du fichier (heures en minutes) qui calcule « Ouvert maintenant ».
- **Une photo** : remplacer le fichier dans `img/` en gardant le même nom (format WebP, 720 px de large).
- **Avant la mise en ligne définitive** : retirer les marqueurs « ? » (classe `tbc`), supprimer `robots.txt`, la balise `noindex` et l’en-tête `X-Robots-Tag` de `vercel.json`, puis ajouter mentions légales et confidentialité.
