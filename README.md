# Hello World — Vercel + GitHub

Petit site statique déployé via Vercel, sources sur GitHub.

## Structure

```
hello-world-vercel/
├── index.html      # Page d'accueil
├── style.css       # Styles
├── .gitignore      # Fichiers ignorés par git
└── README.md       # Ce fichier
```

## Tester localement

Ouvre simplement `index.html` dans ton navigateur (double-clic), ou sers le dossier avec :

```bash
# Python (préinstallé sur macOS)
python3 -m http.server 8000
# puis ouvre http://localhost:8000
```

## Mettre en ligne (étapes)

### 1. Initialiser Git et pousser sur GitHub

```bash
cd ~/Documents/cowork/hello-world-vercel
git init
git add .
git commit -m "Initial commit"
git branch -M main
```

Crée ensuite un repo sur https://github.com/new (nomme-le `hello-world-vercel`, laisse-le vide, sans README), puis :

```bash
git remote add origin https://github.com/TON_USERNAME/hello-world-vercel.git
git push -u origin main
```

### 2. Connecter Vercel

1. Va sur https://vercel.com et connecte-toi avec ton compte GitHub.
2. Clique sur **Add New → Project**.
3. Sélectionne le repo `hello-world-vercel`.
4. Laisse tous les paramètres par défaut (Vercel détecte tout seul que c'est statique).
5. Clique **Deploy**.

En ~30 secondes, tu as une URL publique du type `hello-world-vercel.vercel.app`.

### 3. Itérer

Pour modifier le site :

```bash
# Edite index.html ou style.css
git add .
git commit -m "Description du changement"
git push
```

Vercel redéploie automatiquement à chaque push sur `main`.

## Prochaines étapes possibles

- Ajouter un domaine personnalisé dans Vercel (onglet Settings → Domains).
- Ajouter plusieurs pages (`about.html`, `contact.html`).
- Passer à Tailwind CSS via CDN pour styliser plus vite.
- Migrer vers un framework comme Astro ou Next.js quand le site grossit.
