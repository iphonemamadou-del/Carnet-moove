# Carnet — PWA de notes hors-ligne

Une Progressive Web App minimaliste, prête à être packagée par PWABuilder.

## 📁 Contenu

```
pwa/
├── index.html       # L'application
├── manifest.json    # Métadonnées PWA
├── sw.js            # Service Worker (cache hors-ligne)
└── icons/
    ├── icon-192.png
    ├── icon-512.png
    └── icon-512-maskable.png
```

## 🚀 Déploiement sur GitHub Pages

1. **Créer un dépôt** sur github.com (ex. `carnet-pwa`), public.
2. **Téléverser tous les fichiers** de ce dossier à la racine du dépôt (depuis l'interface web GitHub : "Add file" → "Upload files", puis glisser-déposer le contenu).
3. Aller dans **Settings → Pages**.
4. Sous "Source", choisir la branche `main` et le dossier `/ (root)`. Sauvegarder.
5. Attendre 1–2 minutes. GitHub te donne une URL du type :
   ```
   https://TON-PSEUDO.github.io/carnet-pwa/
   ```

## 📦 Packager avec PWABuilder

1. Aller sur [pwabuilder.com](https://www.pwabuilder.com/)
2. Coller ton URL GitHub Pages dans le champ "Enter the URL to your PWA".
3. Cliquer **Start**. L'outil vérifie le manifest, le service worker et les icônes.
4. Une fois validé, cliquer sur **Package For Stores** et choisir Android, iOS ou Windows.

## ✅ Vérifications avant packaging

- L'URL doit être en **HTTPS** (GitHub Pages le fait automatiquement).
- L'app doit s'ouvrir sans erreur dans un navigateur.
- En mode avion, recharger la page : elle doit continuer à fonctionner.

## 🔧 Personnalisation rapide

- **Nom** : modifier `name` et `short_name` dans `manifest.json` + le `<title>` dans `index.html`.
- **Couleurs** : modifier les variables `--bg`, `--ink`, `--accent` en haut de `<style>` dans `index.html`, et `theme_color` / `background_color` dans `manifest.json`.
- **Icônes** : remplacer les 3 fichiers dans `icons/` par tes propres PNG aux mêmes dimensions.
