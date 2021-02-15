
# Introduction

L'objectif du document est la création d'une *cheat sheet* ou "feuille de triche". 

L'ensemble des fonctions que vous devez documenter se trouvent dans ce document, à vous de  remplir les espaces vides 😉

Ce document pourra vous suivre tout au long de vos études, n'hésitez à le compléter au fur et à mesure.

---

Pour compléter le document, vous utiliserez la fonction **fork** de GitHub pour copier ce projet dans votre espace personnel.

[Si besoin, rendez-vous dans ce dépôt pour revoir les bases de Javascript](https://github.com/Maxence-Machu/javascript-basic-memo)

---

## La fonction GetElementByID()

### Que fait la fonction ?
La méthode getElementById() renvoie un objet qui représente l'élément dont la propriété  id correspond à la chaîne de caractères spécifiée.
Étant donné que les ID d'élément doivent être uniques, s'ils sont spécifiés, ils constituent un moyen utile d'accéder rapidement à un élément spécifique.

### Pourquoi l'utiliser ?
La fonction getElementById doit être utilisée si l'on veut utiliser un élément du DOM en HTML grâce à Javascript 

#### Note supplémentaire
La fonction getElementByID est à ne pas confondre avec la fonction *getElementsByClassName*. 
Les ID dans une page web sont uniques, on ne peut donc pas récupérer plusieurs éléments avec cette fonction. 

### Exemple de code:
```javascript
let element = document.getElementByID('mon-element');
console.log(element);
```

## La fonction GetElementsByClassName()

### Que fait la fonction ?
Renvoie un objet de type tableau de tous les éléments enfants qui ont tous les noms de classe donnés.  Lorsqu'il est appelé sur l'objet document, le document complet est recherché, y compris le nœud racine. classes donnés.

### Pourquoi l'utiliser ?
La fonction getElementByClassName doit être utilisée si l'on veut utiliser tous les éléments ayant le nom de classe donnés.

### Exemple de code:
```javascript
var elements = document.getElementsByClassName(_names_);
console.log(elements);
```

## La fonction querySelector() et querySelectorAll()

### Que fait la fonction ?
L'[API Selectors](http://www.w3.org/TR/selectors-api2/) définit des méthodes pour accéder aux noeuds DOM, c'est-à-dire aux éléments HTML présents, à l'aide de fonctions de recherche.

### Pourquoi l'utiliser ?
Leur intérêt est de faciliter la manipulation des noeuds en JavaScript, et d'aller bien au-delà des quelques fonctions qui équipaient les premières versions de l'interface DOM

### Exemple de code:
```javascript
document.querySelector(".example");

var x =  document.querySelectorAll(".example");
```
## La fonction addEventListener()

### Que fait la fonction ?
La fonction addEventListener() attache un gestionnaire d'événements à l'élément spécifié.

### Pourquoi l'utiliser ?
`addEventListener`  est la manière d'enregistrer un écouteur d'évènements telle que spécifiée dans le DOM du W3C. Ses avantages sont les suivants :

-   Elle permet d'ajouter plus d'un seul gestionnaire pour un évènement. Cela peut s'avérer particulièrement utile pour les bibliothèques  [AJAX](https://developer.mozilla.org/fr/docs/Glossaire/AJAX), les modules JavaScript ou tout autre sorte de code qui a besoin de fonctionner correctement avec d'autres bibliothèques/extensions.
-   Elle donne un contrôle plus fin sur la phase d'activation de l'écouteur (capture contre propagation)
-   Elle fonctionne avec tout élément DOM, pas seulement avec les éléments HTML.

### Exemple de code:
```javascript
_target_.addEventListener(_type_, _écouteur [,_ _options_]);
_target_.addEventListener(_type_, _écouteur [, utiliserCapture_]);
```

## La fonction stopPropagation()

### Que fait la fonction ?
Évite que l'évènement courant ne se propage plus loin dans les phases de capture et de déploiement.

### Pourquoi l'utiliser ?
Pour ne pas qu'un évènement se répète plus loins.
### Exemple de code:
```javascript
_event_.stopPropagation();
```

## La fonction addEventListener('mousemove', maFonction)

### Que fait la fonction ?
L'évènement `mousemove` est déclenché à partir d'un élément lorsqu'un dispositif de pointage (ex. une souris) est déplacé lorsque le curseur est à l'intérieur de l'élément.

### Pourquoi l'utiliser ?
Pour indiquer qu'un élément est cliquable ou déclencher un évènement par exemple
### Exemple de code:
```javascript
document.addEventListener("click", myFunction);  
document.addEventListener("click", someOtherFunction);```
```
## La fonction parseInt()

### Que fait la fonction ?
La fonction `parseInt()` convertit le premier argument en une chaîne, l'analyse et renvoie un entier ou `NaN`. Si la valeur renvoyée n'est pas `NaN`, ce sera l'entier représentant le nombre contenu dans la chaîne dans la base donnée.

### Pourquoi l'utiliser ?
...

### Exemple de code:
```javascript
function roughScale(x, base) {
  const parsed = parseInt(x, base);
  if (isNaN(parsed)) { return 0; }
  return parsed * 100;
}

console.log(roughScale(' 0xF', 16));
// expected output: 1500

console.log(roughScale('321', 2));
// expected output: 0
```


## La variable "event" dans le code suivant:

### Code:
```javascript
element.addEventListener('event-name', function(event) {
  console.log(event);
});
```

### Qu'est-ce que cette variable ?
...

### Pourquoi l'utiliser ?
...


