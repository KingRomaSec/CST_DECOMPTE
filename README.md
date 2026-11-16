# CST_DECOMPTE

Écran de décompte du **Pèlerinage de la Nativité** (Sèmè, 24 – 25 décembre) de l'Église du Christianisme Céleste, prévu pour un affichage plein écran sur une télé.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | La page (HTML, CSS et JavaScript dans un seul fichier, sans dépendance ni build) |
| `logo.png` | Logo Sèmè 26 |
| `vercel.json` | Configuration Vercel (en-têtes de sécurité, cache) |

## Fonctionnement

- Le décompte vise le 24 décembre à 00:00, **heure du Bénin (UTC+1)**, quel que soit le fuseau de l'appareil.
- Du 24 au 25 décembre, l'écran affiche « Le pèlerinage a commencé ».
- À partir du 26 décembre, le décompte repart vers l'année suivante (penser à remplacer `logo.png`).
- **Réglages** : lieu et heure d'ouverture, enregistrés dans le navigateur de l'appareil.
- **Plein écran** : passe en plein écran et empêche la mise en veille si le navigateur le permet.

## Déploiement sur Vercel

1. Sur [vercel.com](https://vercel.com), **Add New → Project**, puis importer ce dépôt GitHub.
2. Framework Preset : **Other**. Laisser vides Build Command et Output Directory.
3. **Deploy**. Chaque `git push` sur `main` redéploie ensuite le site automatiquement.

Ou en ligne de commande :

```bash
npm i -g vercel
vercel --prod
```

## Test en local

```bash
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Sur la télé

Ouvrir l'adresse Vercel dans le navigateur de la télé (ou d'un boîtier Android TV / mini-PC), cliquer sur **Plein écran**, et vérifier que l'horloge de l'appareil est synchronisée automatiquement.
