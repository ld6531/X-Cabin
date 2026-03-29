# 🏕️ X Cabin

**Votre atelier de création de contenu X** — tweets, threads, notes et brouillons. App web mobile-first, déployable en un push.

![X Cabin](assets/icon-192.png)

## Features

- ✏️ **Compositeur** — 7 styles (Alpha, DeFi, Viral, Hook, Insight, Thread, Neutre)
- 🧵 **Mode Thread** — construction tweet par tweet
- 🤖 **IA intégrée** — amélioration via Claude API (Anthropic)
- 📝 **Notes** — capture d'idées avec tags
- 📁 **Brouillons** — sauvegarde persistante via localStorage
- 📱 **PWA** — installable sur Android & iOS

## Déploiement

### GitHub Pages (automatique)

1. Fork ou push ce repo sur GitHub
2. Aller dans **Settings → Pages**
3. Source : **GitHub Actions**
4. Le workflow `.github/workflows/deploy.yml` se déclenche à chaque push sur `main`
5. L'app est disponible sur `https://<username>.github.io/<repo>/`

### Domaine custom (optionnel)

Créer un fichier `CNAME` à la racine :
```
xcabin.votredomaine.com
```

Puis configurer le DNS :
```
CNAME  xcabin  <username>.github.io
```

## Clé API

Pour activer les suggestions IA réelles, ajoute ta clé Anthropic dans **Réglages → Clé API Anthropic** (`sk-ant-...`). Elle est stockée uniquement en localStorage, jamais envoyée ailleurs.

## Structure

```
xcabin/
├── index.html          ← App complète (single file)
├── manifest.json       ← PWA manifest
├── assets/
│   ├── favicon.ico
│   ├── apple-touch-icon.png
│   ├── icon-192.png
│   └── icon-512.png
└── .github/
    └── workflows/
        └── deploy.yml
```

## Stack

HTML · CSS · JS vanilla · Claude API (Anthropic) · GitHub Pages

---

*Made for [@GodCandleGroup](https://x.com/GodCandleGroup)*
