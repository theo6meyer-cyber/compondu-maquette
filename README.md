# Maquette Compondu — déploiement Vercel

Projet statique, deux fichiers. Rien à installer, rien à compiler.

```
index.html    la maquette complète (CSS, JS et illustrations intégrés)
vercel.json   en-tête X-Robots-Tag : la démo ne sera pas indexée
```

## Déployer — méthode ligne de commande

Dans ce dossier :

```bash
npx vercel
```

Vercel demande de vous connecter au premier lancement (GitHub, GitLab ou e-mail) : c'est vous qui vous authentifiez. Ensuite, quatre questions, toutes en gardant la valeur par défaut :

- *Set up and deploy?* → **oui**
- *Which scope?* → votre compte
- *Link to existing project?* → **non**
- *Project name?* → `maquette-compondu` (ce nom devient l'adresse)
- *In which directory is your code located?* → `./`

Vous obtenez une URL de prévisualisation. Pour l'adresse définitive :

```bash
npx vercel --prod
```

Résultat : `https://maquette-compondu.vercel.app`, publique, sans connexion requise.

## Déployer — méthode navigateur

1. Créez un dépôt GitHub et déposez-y ces deux fichiers
2. Sur `vercel.com/new`, importez le dépôt
3. Ne touchez à aucun réglage — Vercel détecte un site statique
4. *Deploy*

## Domaine personnalisé

Une fois un domaine acheté, dans le projet Vercel : *Settings* → *Domains* → ajoutez-le, puis suivez les enregistrements DNS indiqués. C'est ainsi que vous passerez de `.vercel.app` à `votrenom.ch/demo/compondu` ou `demo.votrenom.ch`.

## Mettre à jour la maquette

Remplacez `index.html`, puis relancez `npx vercel --prod`. L'URL ne change pas.

## Rappel

Le bandeau « projet de démonstration » doit rester : la page reprend le nom, l'adresse et le téléphone d'un commerce réel qui n'a pas commandé ce site. Les liens d'appel et le formulaire sont volontairement neutralisés.
