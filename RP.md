<h1>🤔 RP - 323 - Programmation fonctionnelle</h1>

>[!TIP]
>**Référence Javascript:** <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference>  
>**Tester du code JS** : <https://runjs.app/play>  
>**Convertir en PDF** : <https://marketplace.visualstudio.com/items?itemName=manuth.markdown-converter>

<h1>Table des matières</h1>

- [Introduction](#introduction)
- [Opérateurs javascript super-cooool 😎](#opérateurs-javascript-super-cooool-)
  - [opérateur `?:`](#opérateur-)
  - [opérateur `??`](#opérateur--1)
  - [opérateur `??=`](#opérateur--2)
  - [opérateur de décomposition 'spread' `...`](#opérateur-de-décomposition-spread-)
  - [Déstructuration](#déstructuration)
- [Date et Heure](#date-et-heure)
  - [Obtenir la date et/ou heure actuelle](#obtenir-la-date-etou-heure-actuelle)
- [Math](#math)
  - [`Math.PI` - la constante π](#mathpi---la-constante-π)
  - [`Math.abs()` - la |valeur absolue| d'un nombre](#mathabs---la-valeur-absolue-dun-nombre)
  - [`Math.pow()` - élever à une puissance](#mathpow---élever-à-une-puissance)
  - [`Math.min()` - plus petite valeur](#mathmin---plus-petite-valeur)
  - [`Math.max()` - plus grande valeur](#mathmax---plus-grande-valeur)
  - [`Math.ceil()` - arrondir à la prochaine valeur entière la plus proche](#mathceil---arrondir-à-la-prochaine-valeur-entière-la-plus-proche)
  - [`Math.floor()` - arrondir à la précédente valeur entière la plus proche](#mathfloor---arrondir-à-la-précédente-valeur-entière-la-plus-proche)
  - [`Math.round()` - arrondir à la valeur entière la plus proche](#mathround---arrondir-à-la-valeur-entière-la-plus-proche)
  - [`Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre](#mathtrunc---supprime-la-virgule-et-retourne-la-partie-entière-dun-nombre)
  - [`Math.sqrt()` - la raçine carrée d'un nombre](#mathsqrt---la-raçine-carrée-dun-nombre)
  - [`Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)](#mathrandom---générer-un-nombre-aléatoire-entre-00-compris-et-10-non-compris)
- [JSON](#json)
  - [`JSON.stringify()` - transformer un objet Javascript en JSON](#jsonstringify---transformer-un-objet-javascript-en-json)
  - [`JSON.parse()` - transformer du JSON en objet Javascript](#jsonparse---transformer-du-json-en-objet-javascript)
- [Chaînes de caractères](#chaînes-de-caractères)
  - [`split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau](#split---un-ciseau-qui-coupe-une-chaîne-là-où-un-caractère-apparaît-et-produit-un-tableau)
  - [`trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)](#trim-trimstart-et-trimend---épuration-des-espaces-en-trop-dans-une-chaîne-trimming)
  - [`padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères](#padstart-et-padend---aligner-le-contenu-dans-une-chaîne-de-caractères)
- [Console](#console)
  - [`console.log()` - Afficher un message sur la console](#consolelog---afficher-un-message-sur-la-console)
  - [`console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)](#consoleinfo-warn-et-error---afficher-un-message-sur-la-console-filtrables)
  - [`console.table()` - Afficher tout un tableau ou un objet sur la console](#consoletable---afficher-tout-un-tableau-ou-un-objet-sur-la-console)
  - [`console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution](#consoletime-timelog-et-timeend---chronométrer-une-durée-dexécution)
- [Tableaux](#tableaux)
  - [`forEach` - parcourir les éléments d'un tableau](#foreach---parcourir-les-éléments-dun-tableau)
  - [`entries()` - parcourir les couples index/valeurs d'un tableau](#entries---parcourir-les-couples-indexvaleurs-dun-tableau)
  - [`in` - parcourir les clés d'un tableau](#in---parcourir-les-clés-dun-tableau)
  - [`of` - parcourir les valeurs d'un tableau](#of---parcourir-les-valeurs-dun-tableau)
  - [`find()` - premier élément qui satisfait une condition](#find---premier-élément-qui-satisfait-une-condition)
  - [`findIndex()` - premier index qui satisfait une condition](#findindex---premier-index-qui-satisfait-une-condition)
  - [`indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond](#indexof-et-lastindexof---premierdernier-élément-qui-correspond)
  - [`push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau](#push-pop-shift-et-unshift---ajoutersupprime-au-débutfin-dans-un-tableau)
  - [`slice()` - ne conserver que certaines lignes d'un tableau](#slice---ne-conserver-que-certaines-lignes-dun-tableau)
  - [`splice()` - supprimer/insérer/remplacer des valeurs dans un tableau](#splice---supprimerinsérerremplacer-des-valeurs-dans-un-tableau)
  - [`concat()` - joindre deux tableaux](#concat---joindre-deux-tableaux)
  - [`join()` - joindre des chaînes de caractères](#join---joindre-des-chaînes-de-caractères)
  - [`keys()` et `values()` - les clés/valeurs d'un objet](#keys-et-values---les-clésvaleurs-dun-objet)
  - [`includes()` - vérifier si une valeur est présente dans un tableau](#includes---vérifier-si-une-valeur-est-présente-dans-un-tableau)
  - [`every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau](#every-et-some---vérifier-si-plusieurs-valeurs-sont-toutesquelques-présentes-dans-un-tableau)
  - [`fill()` - remplir un tableau avec des valeurs](#fill---remplir-un-tableau-avec-des-valeurs)
  - [`flat()` - aplatir un tableau](#flat---aplatir-un-tableau)
  - [`sort()` - pour trier un tableau](#sort---pour-trier-un-tableau)
  - [`map()` - tableau avec les résultats d'une fonction](#map---tableau-avec-les-résultats-dune-fonction)
  - [`filter()` - tableau avec les éléments passant un test](#filter---tableau-avec-les-éléments-passant-un-test)
  - [`groupBy()` - regroupe les éléments d'un tableau selon un règle](#groupby---regroupe-les-éléments-dun-tableau-selon-un-règle)
  - [`flatMap()` - chaînage de map() et flat()](#flatmap---chaînage-de-map-et-flat)
  - [`reduce()` et `reduceRight()` - réduire un tableau à une seule valeur](#reduce-et-reduceright---réduire-un-tableau-à-une-seule-valeur)
  - [`reverse()` - inverser l'ordre du tableau](#reverse---inverser-lordre-du-tableau)
- [Techniques](#techniques)
  - [\`\`(backticks) - pour des expressions intelligentes](#backticks---pour-des-expressions-intelligentes)
  - [`new Set()` - pour supprimer les doublons](#new-set---pour-supprimer-les-doublons)
- [Fonctions](#fonctions)
  - [Déclaration de fonction](#déclaration-de-fonction)
  - [Fonctions immédiatement invoquées (IIFE)](#fonctions-immédiatement-invoquées-iife)
- [Conclusion](#conclusion)

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Introduction

> Dans ce module, nous allons apprendre comment programmer de manière fonctionnelle avec les différents opérateurs, les différentes chaînes de caractères, etc...  
Voici les objectifs du module :
> - Analyser et décrire les exigences en vue de la réalisation d'une programmation fonctionnelle.
> - Implémenter de manière efficiente des algorithmes et des problèmes d'applications selon le paradigne de programmmation fonctionnelle et les exigences données.
> - Améliorer et optimiser le code impératif implémenté en utilisant la programmation fonctionnelle (refactorisation).
> - Vérifier l'exactitude et la qualité de l'implémentation. 

# Opérateurs javascript super-cooool 😎

## opérateur `?:`

> L'expression `question?valeur1:valeur2` retournera `valeur1` si `question` vaut `true` sinon elle retournera `valeur2`.

```javascript
const age = 15;
const resultat = age >= 18 ? 'majeur' : 'mineur'; // 'mineur'
```

## opérateur `??`

Cet opérateur logique se nomme l'opérateur de "coalescence des nuls".

> Renvoie son opérande de droite lorsque son opérande de gauche vaut `null` ou `undefined` et qui renvoie son opérande de gauche sinon.

```javascript
const foo1 = null ?? 'default'; // "default"
const foo2 = 0 ?? 42; // 0
```

>[!CAUTION]
>Contrairement à l'opérateur logique OU (`||`), l'opérande de gauche sera également renvoyé s'il s'agit d'une valeur équivalente à `false` et pas seulement `null` et `undefined`.
>
>⚠️ En d'autres termes **ATTENTION** ‼️ lors de l'utilisation de `||` pour fournir une valeur par défaut à une variable, car on peut rencontrer des comportements inattendus lorsqu'on considère certaines valeurs comme correctes et utilisables (par exemple une chaine vide `''` ou `0`) ‼️

```javascript
const foo3 = 0 || 42; // 42 => ATTENTION !
const foo4 = 1 || 42; // 1
const foo5 = null || 'salut !'; // 'salut !'
const foo6 = '' || 'salut !'; // 'salut !' => ATTENTION !
```

## opérateur `??=`

Cet opérateur logique se nomme l'opérateur d'affectation de "coalescence des nuls", également connu sous le nom d'opérateur affectation logique nulle.

> Évalue l'opérande de droite et l'attribue à gauche **UNIQUEMENT si l'opérande de gauche est nulle** (`null` ou `undefined`).

```javascript
const a = { duration: 50 };
a.duration ??= 10; // pas fait
a.speed ??= 25; // fait => { duration: 50, speed: 25 }
```

## opérateur de décomposition 'spread' `...`

L'opérateur de décomposition spread `...` permet de décomposer un itérable (comme un tableau) en en ses éléments distincts. Cela permet de rapidement copier tout ou une partie d'un tableau existant dans un autre tableau ou d'en extraire facilement des parties.

```javascript
// Combiner des valeurs existantes dans un nouveau tableau
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

// Extraire uniquement ce qui est utile d'un tableau
const numbers = [1, 2, 3, 4, 5, 6];
const [one, two, ...rest] = numbers;

// Mariage d'objets avec mise à jour :-)
const myVehicle = {
    brand: 'Ford',
    model: 'Mustang',
    color: 'red',
};
const updateMyVehicle = {
    type: 'car',
    year: 2021,
    color: 'yellow',
};
const myUpdatedVehicle = { ...myVehicle, ...updateMyVehicle };
```

## Déstructuration

L'opérateur de décomposition spread `...` sert aussi à isoler certains éléments afin de les utiliser ensuite, et de **mettre le reste** d'un coup ailleurs.

```javascript
const valeurs = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const [a, b, ...c] = valeurs;
console.log(a); // 1
console.log(b); // 2
console.log(c); // [3, 4, 5, 6, 7, 8, 9, 10]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Date et Heure

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date)

## Obtenir la date et/ou heure actuelle

```javascript
const maintenant = new Date(); // Obtenir l'un comme l'autre

console.log(maintenant.toLocaleDateString()); // ex: "06.06.2025"
console.log(maintenant.toLocaleTimeString()); // ex: "15:23:42"

const jour = maintenant.getDate();
const mois = maintenant.getMonth() + 1; // Attention : janvier = 0
const annee = maintenant.getFullYear();
const heure = maintenant.getHours();
const minute = maintenant.getMinutes();
const seconde = maintenant.getSeconds();
console.log(`${jour}/${mois}/${annee} - ${heure}h${minute}`);

// Au format ISO (standard international)
console.log(maintenant.toISOString()); // ex: "2025-06-06T13:23:42.123Z"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Math

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math)

## `Math.PI` - la constante π

Math.PI est une constante qui représente la valeur de π (≈ 3.14159) et sert pour les calculs en lien avec les cercles ou les ang

```javascript
const aireCercle = (rayon) => {
  return Math.round((Math.PI * rayon * rayon) * 100) / 100;  
};
```

## `Math.abs()` - la \|valeur absolue\| d'un nombre

Math.abs() retourne la valeur absolue d’un nombre, c’est-à-dire le nombre sans son signe (transforme un négatif en positif).

```javascript
console.log(Math.abs(-7)); 
```

## `Math.pow()` - élever à une puissance

Math.pow() permet de calculer une puissance, en élevant un nombre à la puissance d'une autre. Voici l'exemple ci-dessous :

```javascript
console.log(Math.pow(2, 3));
```

## `Math.min()` - plus petite valeur

Math.min() a comme but de renvoyer le plus petit nombre d'une liste de valeurs donnnées. Voici l'exemple ci-dessous :

```javascript
console.log(Math.min(4, 9, -2, 7));
```

## `Math.max()` - plus grande valeur

Math.max() a comme but de renvoyer la plus grande valeur d'une liste de valeurs de données. Voici l'exemple ci-dessous :

```javascript
console.log(Math.max(4, 9, -2, 7));
```

## `Math.ceil()` - arrondir à la prochaine valeur entière la plus proche

Math.ceil() permet d'arrondir un nombre à l'entier supérieur, même si la décimale est faible :

```javascript
console.log(Math.ceil(4.1));
```

## `Math.floor()` - arrondir à la précédente valeur entière la plus proche

Math.floor() permet d'arrondir un nombre à l'entier inférieur, en supprimant la partie décimale :

```javascript
console.log(Math.floor(4.9));
```

## `Math.round()` - arrondir à la valeur entière la plus proche

Méthode utilisée pour arrondir des nombres, dans l'exemple ci-dessous nous avons arrondi au demi-point :

```javascript
    const note = (pointsMax) => (points) => {
      return  Math.round(((points / pointsMax) * 5 + 1)* 2 ) /2;
    };
```

## `Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre

Math.trunc() permet de supprimer la partie décimale d'un nombre et renvoie uniquement sa partie entière, sans arrondir :

```javascript
console.log(Math.trunc(4.9));  
console.log(Math.trunc(-3.7));
```

## `Math.sqrt()` - la raçine carrée d'un nombre

Math.sqrt() renvoie la racine carrée d'un nombre :

```javascript
console.log(Math.sqrt(25));
```

## `Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)

Math.random est une méthode qui renvoie une valeur entre 0 et 0.99999999999 et ensuite vous la multipliez pour avoir quelque chose entre un min et un max
Voici l'exemple ci-dessous :

```javascript
public static void main(String[] args) {
  int nombre = (int) (Math.random() * (max - min + 1)) + min;        
  System.out.println("b");
};
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# JSON

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON)

## `JSON.stringify()` - transformer un objet Javascript en JSON

JSON.stringify() sert à convertir un objet JavaScript en chaîne de texte JSON. Voici l'exemple ci-dessous :

```javascript
const user = { name: "Emma", age: 20};
const jsonText = JSON.stringify(user);
console.log(jsonText);
```

## `JSON.parse()` - transformer du JSON en objet Javascript

JSON.parse() sert à convertir une chaîne JSON en objet JavaScript, c'est l'inverse de JSON.stringify. Voici l'exemple ci-dessous :

```javascript
const jsonText = '{"name: "Emma", "age": 20}';
const user = JSON.parse(jsonText);
console.log(user.name);
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Chaînes de caractères

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String)

## `split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau

split() sert à couper une chaîne de caractères en un tableau, selon un séparateur choisi. Voici l'exemple ci-dessous :

```javascript
const phrase = "salut, au revoir, bonjour";
const separer = phrase.split(",");
console.log(separer);
```

## `trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)

trim(), trimStart(), trimEnd() servent à supprimer les espaces inutiles dans une chaîne de caractères. Voici l'exemple ci-dessous :


```javascript
const text = "   Salut ça va?   ";
console.log(text.trim()); // enlève les espaces au début et à la fin
console.log(text.trimStart()); // enlève seulement au début
console.log(text.trimEnd()) // enlève seulement à la fin
```

## `padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères

padStart() et padEnd() servent à compléter une chaîne avec des caractères (souvent des zéros ou espaces) jusqu'à une longueur donnée. Voici l'exemple ci-dessous :

```javascript
const num = "7";
console.log(num.padStart(3, "0")); // ajoute des 0 au début (007)
console.log(num.padEnd(4, ".")) // ajoute des points à la fin (7...)
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Console

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/API/console](https://developer.mozilla.org/fr/docs/Web/API/console)

## `console.log()` - Afficher un message sur la console

```javascript
console.log('Coucou !'); // Coucou !
```

## `console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `console.table()` - Afficher tout un tableau ou un objet sur la console

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Tableaux

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array)

## `forEach` - parcourir les éléments d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `entries()` - parcourir les couples index/valeurs d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `in` - parcourir les clés d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `of` - parcourir les valeurs d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `find()` - premier élément qui satisfait une condition

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `findIndex()` - premier index qui satisfait une condition

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprime au début/fin dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `slice()` - ne conserver que certaines lignes d'un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `splice()` - supprimer/insérer/remplacer des valeurs dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `concat()` - joindre deux tableaux

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `join()` - joindre des chaînes de caractères

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `keys()` et `values()` - les clés/valeurs d'un objet

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `includes()` - vérifier si une valeur est présente dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `fill()` - remplir un tableau avec des valeurs

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `flat()` - aplatir un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `sort()` - pour trier un tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `map()` - tableau avec les résultats d'une fonction

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `filter()` - tableau avec les éléments passant un test

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `groupBy()` - regroupe les éléments d'un tableau selon un règle

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `flatMap()` - chaînage de map() et flat()

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `reduce()` et `reduceRight()` - réduire un tableau à une seule valeur

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `reverse()` - inverser l'ordre du tableau

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Techniques

## ``(backticks) - pour des expressions intelligentes

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

## `new Set()` - pour supprimer les doublons

Description à faire par vos soins...

```javascript
A FAIRE PAR VOS SOINS...
SIMPLE, DROIT AU BUT, UTILE, STYLE PENSE-BÊTE
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Fonctions

## Déclaration de fonction

**Standard**

```javascript
function doStuff(a, b, c) {
    return a + b + c;
}
```

**Sous forme d'expression de fonction**

```javascript
const doStuff = function (a, b, c) {
    return a + b + c;
};
```

**Sous forme d'expression de fonction anonyme**

```javascript
const doStuff = (a, b, c) => {
    return a + b + c;
};
```

**Sous forme raccourcie**

S'il n'y a qu'un seul argument et que son corps n'a qu'une seule expression, on peut omettre le return et le corps de la fonction :

```javascript
const doStuff = (a) => `Salut ${a} !`;
```

## Fonctions immédiatement invoquées (IIFE)

IIFE = Immediately Invoked Function Expressions.

Ces fonctions sont définies et **exécutées immédiatement**. Elles sont souvent utilisées pour créer un **contexte isolé** ou encapsuler du code sans polluer l’espace global.

```javascript
(function(){ ... })()
```

ou

```javascript
(() => { ... })()
```

# Conclusion

> Votre conclusion avec les éléments usuels
