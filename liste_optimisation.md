Voici la liste classée du plus rapide au plus compliqué à réaliser :

### Rapide à faire
1. **Balises de langue** :
   - Ajouter l'attribut `lang="fr"` à la balise `<html>` pour indiquer la langue de la page. ✓

2. **Balises de titre et méta descriptions** :
   - Ajouter une balise `<title>` et une méta description `<meta name="description" content="...">` pour améliorer le SEO. ✓

3. **Balises alt pour les images** :
   - Ajouter des balises `alt` descriptives aux images. ✓

4. **Favicon** :
   - Ajouter une balise `<link rel="icon" href="path/to/favicon.ico">` pour inclure un favicon. ✓

5. **Labels pour les formulaires** :
   - Associer les labels des champs de formulaire aux champs via l'attribut `for`. ✓

6. **Contraste des couleurs** :
   - Vérifier et ajuster le contraste des couleurs pour s'assurer qu'il est suffisant pour les utilisateurs malvoyants. ✓

7. **Navigation au clavier** :
   - S'assurer que la navigation au clavier est possible et intuitive. ✓

### Moyennement rapide à faire
8. **Chargement asynchrone des scripts** :
   - Utiliser `async` ou `defer` pour les scripts externes. ✓

9. **Balises de titre hiérarchiques** :
    - Utiliser des balises de titre hiérarchiques (`<h1>`, `<h2>`, etc.) de manière appropriée pour structurer le contenu. ✓

10. **Balises Open Graph et Twitter Cards** :
    - Ajouter des balises Open Graph et Twitter Cards pour améliorer le partage sur les réseaux sociaux. ✓

11. **Liens internes** :
    - Utiliser des liens internes pour améliorer la navigation et le SEO. ✓

### Plus compliqué à faire

12. **Utilisation de balises sémantiques** :
    - Utiliser des balises HTML5 sémantiques comme `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, et `<footer>` pour améliorer la structure du document. ✓

13. **Optimisation des images** :
    - Utiliser des formats modernes comme WebP et compresser les images pour réduire leur taille. ✓

14. **Suppression des CSS inutilisés** :
    - Supprimer les styles CSS non utilisés pour réduire la taille des fichiers CSS. ✓

15. **Ajout du SEO local** :
    - Ajouter les informations de SEO local ✓
    - Vérification avec Google Search Central ✓

16. **Suppressions des balises inutiles** :
    - <link> flaticon ✓

17. **Corriger l'affichage des filtres** ✓

18. **Minification des fichiers CSS et JavaScript** : (A faire en dernier)
    - Minifier les fichiers CSS et JavaScript pour réduire le temps de chargement.

--------------------------------------------

**Rendre la navigation modale fonctionnelle**

- **Initialisation de l’index à -1**  
  La variable « index » est initialisée à -1 afin de détecter correctement l’index de l'image active dans le tableau (imagesCollection). Si l'image n'est pas trouvée, la fonction quitte sans rien faire.

- **Recherche de l'image active**  
  La boucle sur « imagesCollection » compare les sources des images pour trouver l'image actuellement affichée dans la lightbox et calcule son index.

- **Calcul de l’index précédent et suivant avec "wrap-around"**  
  Pour la navigation circulaire, l’index précédent est calculé avec la formule  
  (index - 1 + imagesCollection.length) % imagesCollection.length  
  et l’index suivant avec  
  (index + 1) % imagesCollection.length.  
  Cela permet de revenir de la première à la dernière image et inversement.

- **Mise à jour de la source de l'image affichée**  
  Une fois le nouvel index déterminé, on met à jour la source de l'image de la lightbox avec l'attribut « src » de l'image correspondante dans le tableau.

- **Amélioration de la navigation** (la modal n'était pas centrée)