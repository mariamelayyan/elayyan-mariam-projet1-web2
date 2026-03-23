# DOCUMENTATION

## 1. Démarche 

1. **Préparation**  
   - Créer un répertoire GitHub avec tous les documents requis.  
   - Importer les images, icônes et typographies nécessaires depuis la maquette reçue.  
   - Identifier les unités et couleurs utilisées dans la maquette pour définir les variables CSS.  

2. **Planification de la structure HTML**  
   - Identifier les sections principales : Hero, About, Opening Hours, Testimonials, Footer, Navbar.  
   - Utiliser la méthodologie **BEM** pour nommer les classes, afin d’assurer clarté et cohérence.  

3. **Construction du layout**  
   - Mettre en place les containers et sous-containers pour chaque section.  
   - Préparer les différents éléments répétés pour pouvoir les réutiliser facilement.  

4. **Stylisation avec CSS**  
   - Utiliser **Flexbox** pour gérer la disposition et la responsivité.  
   - Convertir les unités en valeurs responsive (%, vw, vh) au lieu de px fixes.  
   - Gérer les icônes et images dans des conteneurs pour qu’elles restent à la bonne position sur différents écrans.  

---

## 2. Choix techniques

- **BEM pour les classes CSS** :  
  - Facilite la lecture et la maintenance du code.  
  - Permet de réutiliser des blocs et d’ajouter facilement des modificateurs (`hero__title--highlight`, `about-card--full-width`).  

- **Flexbox** :  
  - Pour les alignements horizontaux et verticaux.  

- **Images et icônes** :  
  - Utilisation de `<img>` pour les images qui doivent rester proportionnelles et permettre le positionnement exact des icônes.  
  - Pour les icônes, utilisation d’emojis ou d’images SVG dans des conteneurs pour un meilleur contrôle.  

- **Responsivité** :  
  - Pour les textes et icônes, utilisation d’unités relatives (`%, vw, vh`) pour que tout s’adapte aux écrans.  
  - Les containers principaux ont des `max-width` et `aspect-ratio` pour conserver les proportions correctes.  

---

## 3. Défis rencontrés

1. **Positionnement d'un icônes sur l'image de la carte**  
   Certaines méthodes de positionnement comme `position: relative` ne permettaient pas à l’icône de rester au bon endroit lorsque l’image changeait de dimension.  
   Pour régler ce problème, j’ai utilisé deux images en `background-image` dans un conteneur et appliqué les mêmes pourcentages pour le positionnement. J’ai aussi utilisé `calc()` pour que l’icône s’agrandisse proportionnellement à la taille de l’écran.  

2. **Maintenir la cohérence BEM**  
   Plusieurs sections avaient des noms incohérents (ex. `navbar__brand__logo`) ou des erreurs d’orthographe (ex. `oppenings`).  
   J’ai donc renommé les classes pour avoir une **structure uniforme et compréhensible**.  

3. **Scroll horizontal**  
   L’utilisation de `vw: 100` faisait apparaître un scroll horizontal à cause de l’espace occupé par le scroll vertical.  
   Pour corriger ce problème, j’ai utilisé d’autres unités et ajusté la mise en page.  

