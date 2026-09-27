# CRP-5 face vent : installer l'app sur iPhone

Le dossier contient 8 fichiers, tous à la racine (pas de sous-dossier, pour pouvoir tout déposer d'un coup, même depuis un iPhone) :

| Fichier | Rôle |
|---|---|
| `index.html` | L'outil complet, polices incluses |
| `manifest.webmanifest` | Nom, icône, ouverture en plein écran |
| `sw.js` | Mise en cache pour le fonctionnement hors connexion |
| `icon-180.png`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Icônes |
| `LISEZMOI.md` | Ce guide |

## 1. Créer le compte et le dépôt GitHub

1. Crée un compte gratuit sur github.com si tu n'en as pas.
2. En haut à droite, bouton **+**, puis **New repository**.
3. Nom du dépôt : `crp5` (il apparaîtra dans l'adresse de l'app).
4. Coche **Public**. GitHub Pages gratuit ne fonctionne qu'avec un dépôt public.
5. Ne coche aucune option d'initialisation, puis **Create repository**.

## 2. Déposer les fichiers

1. Sur la page du dépôt vide, clique **uploading an existing file** (ou **Add file**, puis **Upload files**).
2. Sélectionne les 8 fichiers décompressés de l'archive. Sur iPhone : décompresse d'abord l'archive dans l'app Fichiers (un appui dessus suffit), puis sélectionne les fichiers depuis ce dossier.
3. En bas de page, **Commit changes**.

C'est plus confortable depuis un ordinateur (glisser-déposer), mais tout se fait aussi depuis Safari sur iPhone.

## 3. Activer GitHub Pages

1. Dans le dépôt : **Settings**, puis **Pages** dans le menu de gauche.
2. Section **Build and deployment**, **Source** : *Deploy from a branch*.
3. **Branch** : `main`, dossier `/ (root)`, puis **Save**.
4. Attends 1 à 2 minutes, puis recharge la page. L'adresse s'affiche en haut, sous la forme :
   `https://TON-PSEUDO.github.io/crp5/`

## 4. Installer sur l'iPhone

1. Ouvre cette adresse dans **Safari** (pas dans une autre app).
2. Bouton **Partager**, puis **Sur l'écran d'accueil**, puis **Ajouter**.
3. Lance l'app une première fois avec du réseau : elle se met en cache.
4. Test : passe en mode avion et rouvre l'app. Elle doit s'afficher normalement.

## Mettre à jour l'app plus tard

1. Remplace `index.html` dans le dépôt (**Add file**, puis **Upload files**, même nom de fichier).
2. Ouvre `sw.js` dans le dépôt, clique le crayon, change `crp5-v1` en `crp5-v2` (puis v3, etc.) et valide.
3. Sur l'iPhone, ouvre l'app avec du réseau, ferme-la et rouvre-la : la nouvelle version est chargée.

Sans l'étape 2, l'iPhone peut continuer à afficher l'ancienne version depuis son cache.

## Bon à savoir

- **Visibilité** : l'adresse est publique. Toute personne qui la connaît peut ouvrir l'outil. Il ne contient que des exercices et des calculs, aucune donnée personnelle.
- **Scores** : ils sont stockés dans l'app sur le téléphone. Ils sont distincts de ceux de la version claude.ai et de Safari.
- **Cache** : si tu n'ouvres pas l'app pendant longtemps, iOS peut vider son cache. Il suffit alors de la rouvrir une fois avec du réseau.
