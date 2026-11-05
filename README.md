# Koumagoto Mboitam Patrick — Portfolio professionnel

**Administration systèmes · Réseaux · Sécurité informatique**  
Libreville, Gabon

[Consulter le portfolio](https://koumagoto.github.io/) · [Consulter le CV](./CV-Koumagoto-Mboitam-Patrick.pdf) · [Prendre contact](mailto:koumagotomboitampat@gmail.com)

> Prévenir les risques, tenir la continuité de service et protéger les données, en coordination avec les équipes techniques.

## Présentation

Ce dépôt contient le portfolio professionnel de **Koumagoto Mboitam Patrick**, consacré à l’administration des systèmes et réseaux, à la sécurisation des infrastructures et à la gestion opérationnelle des services informatiques.

Le site présente les compétences techniques, les réalisations, le parcours professionnel, la formation et les moyens de contact. Il décrit notamment des interventions sur Windows Server, Active Directory, DNS et DHCP, la supervision des infrastructures, le diagnostic réseau et la sécurité des applications web dans un cadre autorisé.

Le parcours présenté comprend des expériences à la CEEAC, chez Huawei Enterprise Tchad, à Coris Bank Tchad et dans la numérisation documentaire au ministère de l’Urbanisme et de l’Aménagement du territoire du Tchad, ainsi que des activités de formation.

## Architecture : un seul fichier de code

Le site est une page statique en français. **Le HTML, le CSS et le JavaScript sont regroupés dans `index.html`.**

Les styles sont intégrés dans `<style id="styles-integres">`. Le script de navigation et d’animation se trouve dans `<script id="script-integre">`, en fin de page. Un autre script intégré actualise l’année du pied de page.

**Aucun fichier `style.css` ou `main.js` n’est nécessaire. Aucun dossier `assets/` n’est utilisé par cette version.**

La photo, le favicon et le CV PDF restent des fichiers séparés, placés à côté de `index.html`. Les polices Fraunces et Outfit sont chargées depuis Google Fonts. Le fichier de code est donc unique, mais le site n’est pas entièrement autonome hors connexion.

Le projet ne nécessite ni framework, ni dépendance JavaScript externe, ni compilation, ni serveur applicatif, ni base de données.

## Organisation des fichiers

```text
racine-du-depot/
├── index.html                         # Page complète : HTML, CSS et JavaScript
├── README.md                          # Documentation du portfolio
├── patrick-koumagoto.png               # Photo de profil
├── favicon.svg                        # Icône du site
└── CV-Koumagoto-Mboitam-Patrick.pdf     # CV accessible depuis la page
```

Cette arborescence décrit les fichiers attendus. La photo, le favicon et le CV doivent être présents séparément dans le dépôt : ils ne sont pas incorporés au HTML.

### Chemins utilisés dans la page

| Ressource | Chemin relatif |
| --- | --- |
| Photo de profil | `./patrick-koumagoto.png` |
| Favicon | `./favicon.svg` |
| CV PDF | `./CV-Koumagoto-Mboitam-Patrick.pdf` |

Conserver exactement les noms, les extensions et les majuscules indiqués. Le chemin de la photo figure dans la balise `<img>` et dans les données structurées JSON-LD. Le lien vers le CV apparaît dans l’accueil et dans la section Contact.

## Rubriques du portfolio

| Rubrique | Identifiant HTML | Contenu |
| --- | --- | --- |
| Accueil | `accueil` | Identité, spécialité, fiche professionnelle, disponibilité et accès au CV. |
| Profil | `profil` | Positionnement professionnel, pratique opérationnelle et ligne de conduite. |
| Compétences | `competences` | Systèmes, réseaux, cybersécurité, supervision, cloud et terrain, projets et transmission. |
| Réalisations | `realisations` | Huit réalisations : Windows Server et Active Directory, migration DHCP/DNS, remise en service de serveurs, supervision, diagnostic réseau, sécurité web, réseau de la CEEAC et numérisation cadastrale. |
| Parcours | `parcours` | Expériences professionnelles, missions institutionnelles et autres activités. |
| Formation | `formation` | Diplômes, certificats et attestations, langues et compétences comportementales. |
| Contact | `contact` | E-mail, téléphones, WhatsApp, CV, localisation et références professionnelles. |

La page est rédigée en français. Les langues mentionnées dans le profil décrivent des compétences linguistiques ; elles ne correspondent pas à des versions traduites du site.

## Fonctionnalités

### Navigation et interactions

L’en-tête reste fixé en haut de page et change d’apparence lors du défilement. Les liens permettent de rejoindre les différentes sections ; le script met en évidence la section observée à l’écran.

Sur petit écran, un bouton ouvre et ferme le menu. Celui-ci se referme après la sélection d’un lien ou avec la touche `Échap`. L’état d’ouverture est transmis par l’attribut `aria-expanded`.

Les blocs concernés apparaissent progressivement au défilement grâce à `IntersectionObserver`. L’année du pied de page est mise à jour automatiquement.

### Affichage et lecture

La mise en page utilise CSS Grid, Flexbox et des règles adaptatives, avec des points de rupture à **980 px** et **680 px**. Des styles spécifiques sont prévus pour l’impression.

Le code comprend un lien « Aller au contenu », un texte alternatif pour le portrait, des indicateurs de focus et une adaptation à la préférence de réduction des animations (`prefers-reduced-motion`).

Le contenu n’est masqué pour les animations qu’après l’initialisation du script. Sans JavaScript, les textes restent visibles, mais les interactions du menu mobile et les animations ne fonctionnent pas. En l’absence de prise en charge d’`IntersectionObserver`, le script conserve l’affichage des blocs sans ces animations.

### Présentation dans les moteurs et les partages

L’en-tête contient un titre, une description, une couleur de thème et des métadonnées Open Graph. Un bloc JSON-LD de type `Person` décrit l’identité professionnelle, les coordonnées, la localisation, les langues et l’établissement de formation.

### Contact et documents

La prise de contact repose sur des liens e-mail, téléphone et WhatsApp. **Aucun formulaire d’envoi ni traitement côté serveur n’est intégré.** Deux liens donnent accès au même fichier CV PDF.

## Consultation locale

Rassembler `index.html`, la photo, le favicon et le CV dans un même dossier, puis ouvrir `index.html` dans un navigateur. Aucune installation de paquets n’est requise.

Une connexion Internet est nécessaire pour charger les polices Google Fonts et utiliser les services externes. En l’absence des polices distantes, les familles de remplacement déclarées dans le CSS sont utilisées. Le CV reste accessible localement lorsque le PDF est présent au chemin attendu.

## Publication et mises à jour

Pour l’organisation de publication à la racine retenue pour ce projet, déposer les fichiers de l’arborescence dans le dossier effectivement publié par GitHub Pages. Conserver `index.html` comme fichier d’entrée et remplacer l’ancienne version complète lors d’une mise à jour du code.

Le `README.md` documente le dépôt ; il ne remplace pas la page HTML et ne nécessite aucun ajout de lien dans celle-ci. Les réglages de publication du dépôt sont distincts du contenu de `index.html`.

La version documentée contient ce repère dans son en-tête :

```html
<meta name="build-version" content="html-unique-racine-v3">
```

Ce repère permet de reconnaître cette version dans le code source de la page publiée. Il ne constitue pas un mécanisme automatique de mise à jour ou de gestion du cache.

## Personnalisation

Toutes les modifications de contenu, de présentation et de comportement s’effectuent dans `index.html`.

| Élément à modifier | Emplacement à mettre à jour |
| --- | --- |
| Identité et spécialité | Accueil, titre de page, descriptions, pied de page et JSON-LD. |
| Photo | Fichier PNG, attribut `src` de l’image et propriété `image` du JSON-LD. |
| CV | Fichier PDF et les deux liens de téléchargement en cas de changement de nom. |
| Expériences, compétences et formation | Sections HTML correspondantes. |
| E-mail et téléphones | Section Contact et données structurées JSON-LD ; vérifier aussi le lien WhatsApp. |
| Couleurs, polices et mise en page | Bloc `<style id="styles-integres">`. |
| Menu et animations | Bloc `<script id="script-integre">`. |

Les principales couleurs sont définies dans `:root` :

```css
--forest: #12241f;
--green: #0c5c4a;
--gold: #e4c27a;
--paper: #f3efe6;
--ink: #1a1814;
```

La police **Fraunces** est utilisée pour les titres et **Outfit** pour le texte courant. Les outils professionnels cités dans le portfolio — Nagios, SolarWinds, Wireshark, Nmap, OWASP ZAP ou Microsoft Project — décrivent les compétences présentées ; ils ne sont pas des dépendances du site.

## Vérifications et dépannage

Après une modification, contrôler l’affichage sur grand et petit écran, la navigation, les deux accès au CV et les liens de contact. Vérifier également la cohérence entre le contenu visible et les métadonnées.

| Symptôme | Points à vérifier |
| --- | --- |
| Photo ou favicon introuvable | Présence du fichier à la racine publiée ; correspondance exacte du nom, de l’extension et du chemin relatif. |
| CV inaccessible | Présence du PDF et correspondance des deux liens avec son nom exact. |
| Requête vers `assets/js/main.js` ou `assets/css/style.css` | Le document chargé ne correspond pas à cette version. Comparer son code source et son repère de version, puis contrôler le fichier publié, le déploiement et le cache du navigateur. |
| Certains blocs restent invisibles | Vérifier les erreurs JavaScript et les règles `.js .reveal`. Ne pas déplacer l’ajout de la classe `js` avant l’initialisation des observateurs. |
| Polices différentes de celles attendues | Vérifier le chargement de Google Fonts ; les polices de remplacement peuvent s’afficher lorsque les ressources distantes sont indisponibles. |

## Contact

**Koumagoto Mboitam Patrick**  
Administrateur systèmes, réseaux et sécurité informatique  
Libreville, Gabon

**E-mail :** [koumagotomboitampat@gmail.com](mailto:koumagotomboitampat@gmail.com)  
**Téléphones :** +241 76 55 02 75 / +241 65 62 43 43  
**WhatsApp :** [Écrire au +241 76 55 02 75](https://wa.me/24176550275)

Les références professionnelles sont présentées dans la section Contact du portfolio. Leurs coordonnées détaillées sont transmises sur demande.

---

Documentation de la version `html-unique-racine-v3` de [`index.html`](./index.html).
