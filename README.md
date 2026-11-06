# El Cielo Cozumel Tours — Fichiers de traduction

Ce dépôt contient les fichiers de traduction PHP pour [elcielocozumeltours.com](https://elcielocozumeltours.com).

## Structure

Chaque sous-dossier correspond à une version linguistique du site :

| Code | Langue        |
|------|---------------|
| bg   | Bulgare       |
| cs   | Tchèque       |
| da   | Danois        |
| el   | Grec          |
| fi   | Finnois       |
| ga   | Irlandais     |
| hu   | Hongrois      |
| ja   | Japonais      |
| ko   | Coréen        |
| no   | Norvégien     |
| pl   | Polonais      |
| ro   | Roumain       |
| sk   | Slovaque      |
| sv   | Suédois       |
| uk   | Ukrainien     |
| zh   | Chinois       |

## Fonctionnement

Chaque `{lang}/index.php` utilise le pattern `ob_start()` / `include('../index.php')` / `str_replace()` pour remplacer le contenu français par la langue cible.

## ⚠️ Fichier manquant : `index.php`

Le fichier source principal `index.php` (page française, ~63 Ko) n'est pas inclus dans ce dépôt car il ne peut pas être téléchargé via l'API (filtré par l'extension Chrome). Pour compléter la sauvegarde :

1. Télécharger `index.php` depuis le gestionnaire de fichiers Hostinger
2. L'ajouter à la racine du dépôt
3. Faire `git add index.php && git commit -m "Add main index.php source file"`

## Fichiers serveur

- `.htaccess` — Règles de réécriture Apache (24 langues + cache + gzip)
- `sitemap.xml` — Sitemap avec hreflang pour toutes les versions linguistiques
- `robots.txt` — Autorisation crawl + référence sitemap
