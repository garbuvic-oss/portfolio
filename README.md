# Portfolio de Victor Garbugli

Site web personnel présentant mon parcours, mes réalisations et mes compétences en informatique.
Je suis étudiant en **BUT Informatique** à l'IUT de Clermont-Ferrand.

Le site est statique : il est écrit uniquement en **HTML5** et **CSS3**, sans framework ni JavaScript.

---

## Sommaire

- [Aperçu](#aperçu)
- [Pages du site](#pages-du-site)
- [Structure du projet](#structure-du-projet)
- [Lancer le site](#lancer-le-site)
- [Choix de conception](#choix-de-conception)
- [Personnaliser le contenu](#personnaliser-le-contenu)
- [Crédits](#crédits)

---

## Aperçu

Le site a trois objectifs : se présenter, montrer les projets réalisés et permettre de télécharger mon CV.
Le design reste sobre et professionnel : palette bleu marine, typographie soignée et animations discrètes.

## Pages du site

| Page | Fichier | Contenu |
| --- | --- | --- |
| Accueil | `src/index.html` | Présentation, projet professionnel et valeurs |
| Mes réalisations | `src/realisations.html` | Projet Quixo : description, rôle dans le projet et captures d'écran |
| Mes compétences | `src/competencesInfo.html` | Compétences regroupées par domaine, avec les logos des langages |
| Mon CV | `src/cv.html` | Téléchargement du CV au format PDF |
| Mes centres d'intérêt | `src/interets.html` | Basket-ball et valeurs développées |

## Structure du projet

```text
portfolio/
├── README.md
├── src/                         # Pages HTML
│   ├── index.html
│   ├── realisations.html
│   ├── competencesInfo.html
│   ├── cv.html
│   └── interets.html
├── styles/                      # Feuilles de style
│   ├── index.css                # Base commune à toutes les pages
│   ├── realisations.css
│   ├── competencesInfo.css
│   ├── cv.css
│   └── interets.css
├── images/                      # Photo, logos et captures d'écran
│   ├── moi.png
│   ├── LogoClermontBasket.png
│   ├── espritD'equipe.jpg
│   ├── CONFIG.png
│   └── PlateauPage.png
└── docs/
    └── CV_Victor_GARBUGLI.pdf   # CV téléchargeable
```

Chaque page charge `index.css` (variables, navigation, mise en page), puis sa propre feuille de style si elle en a une.

## Lancer le site

Aucune installation n'est nécessaire.

1. Récupérer le dossier du projet.
2. Ouvrir `src/index.html` dans un navigateur.

Les polices (Google Fonts) et les logos de la page Compétences (Devicon) sont chargés en ligne : une connexion internet est donc nécessaire pour les voir s'afficher.

## Choix de conception

- **Palette :** bleu marine `#0f2557` pour la navigation et les titres, bleu `#2557d6` pour les accents, fond gris clair `#f3f5f9`.
- **Typographie :** *IBM Plex Serif* pour les titres, *IBM Plex Sans* pour le texte.
- **Navigation :** barre fixe en haut de page, avec la page courante soulignée.
- **Animations :** une apparition douce du contenu au chargement et de légers effets au survol. Elles sont désactivées automatiquement si le système demande de réduire les animations.
- **Responsive :** la mise en page s'adapte aux téléphones et aux tablettes.
- **Accessibilité :** textes alternatifs sur les images, focus clavier visible, contrastes suffisants.

Les couleurs et la police sont définies comme variables CSS au début de `styles/index.css`. Les modifier suffit à changer l'apparence de tout le site.

## Personnaliser le contenu

**Ajouter une compétence.** Dans `src/competencesInfo.html`, ajouter une ligne dans la liste `logos` du bloc concerné :

```html
<li><img src="URL_DU_LOGO.svg" alt="" loading="lazy"><span>Nom</span></li>
```

**Ajouter un projet.** Dans `src/realisations.html`, dupliquer le bloc `<article class="projet">` et adapter le texte et les images.

**Mettre à jour le CV.** Remplacer le fichier `docs/CV_Victor_GARBUGLI.pdf` en conservant le même nom, ou modifier le lien dans `src/cv.html`.

**Ajouter une page.** Copier une page existante dans `src/`, puis ajouter son lien dans la barre de navigation de chaque page.

## Crédits

- Logos des langages : [Devicon](https://devicon.dev)
- Polices : [IBM Plex](https://fonts.google.com/specimen/IBM+Plex+Sans) via Google Fonts
- Conception et contenu : Victor Garbugli, BUT Informatique, IUT de Clermont-Ferrand
