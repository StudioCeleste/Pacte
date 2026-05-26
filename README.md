# Pacte

Prototype d'interface pour **Pacte**, une application de suivi de santé
destinée aux patients atteints de maladie chronique, entre deux consultations.

Stack : **React 18 + Vite**. Aucune dépendance externe (icônes, styles et
animations sont intégrés au composant).

## Développement local

Prérequis : Node.js 18 ou plus récent.

```bash
npm install
npm run dev
```

Le prototype est servi sur `http://localhost:5173`.

## Build de production

```bash
npm run build      # génère le dossier dist/
npm run preview    # prévisualise le build
```

## Déploiement sur Vercel

Vercel détecte automatiquement un projet Vite. Deux options :

### Option A — via Git (recommandé)
1. Pousser ce dossier sur un dépôt GitHub / GitLab / Bitbucket.
2. Sur vercel.com : **Add New → Project**, puis importer le dépôt.
3. Laisser les réglages par défaut et cliquer sur **Deploy**.

### Option B — via la CLI
```bash
npm i -g vercel
vercel
```

Réglages attendus (normalement détectés seuls) :

| Paramètre        | Valeur          |
|------------------|-----------------|
| Framework Preset | Vite            |
| Build Command    | `npm run build` |
| Output Directory | `dist`          |
| Install Command  | `npm install`   |

## Structure

```
pacte-app/
├── index.html          # point d'entrée + polices
├── package.json
├── vite.config.js
└── src/
    ├── main.jsx        # montage React
    └── App.jsx         # l'application Pacte (5 écrans)
```

---

Note : ceci est un prototype d'interface. Il ne stocke aucune donnée et ne
remplace pas un avis médical.
