# C'est quoi react?
React est une librairie javascript créée par Facebook pour aider à construire des pages web avec l'approche par composante.
## C'est quoi une composante?
C'est un découpage d'une page web en morceaux réutilisables. Chaque morceau est une composante.
Ces composantes vont être codées dans des fichiers jsx
## C'est quoi un fichier jsx (Javascript syntax extension)?
Ça permet d'écrire du code dans ce style : 
```js
function Greet(){
  return <h1>Hello World!</h1>;
}
```
Babel se chargera de compilier le code (yep, un compilateur en javascript!)
```js
import {jsx as _jsx} from 'react/jsx-runtime';

function App() {
  return _jsx('h1', { children: 'Hello world' });
}
```
Il y a 5 règles à respecter avec les jsx
1. Return ne peut retourner qu'un seul élément (pas comme ne python)
2. Tous les tags, doivent être fermés (par exemple &lt;br&gt; doit être &lt;br/&gt;)
3. Si on ajoute un veut afficher un autre component dans un component existant, on doit toujous utilser la lettre majuscule au début. Exemple : &lt;Navigation&gt;
4. Pout utiliser du javascript, on doit utilise les accolades {}.
5. en react, on utilise className au lieu de class.

# Okay, nice, mais on commence quand?
Premièrement, il faut installer nodejs (voir le site). C'est supposé être fait.
Ensuite, tu fais `npx create-next-app`. NPX c'est l'utilitaire global de téléchargement de librarie pour npm.
Tu réponds aux questions :
nom : test
Utiliser TypeScript? :  Non (pour l'instant)
ESLint? : Oui!
Tailwind? : Non (sad face)
src : Oui
App router : Oui
Import alias : Non
Tadahhhhh

# C'est quoi npm?
Npm est un gestionnaire de librarie. On va s'en servir pour ajouter des utilitaires qui ont été codés par d'autres personnes beaucoup plus talentueuses que nous.

# Nice! Heu. Je fais quoi maintenant, c'est quoi tous ces fichiers dans le dossier test?

- eslintrc.json : Ça fait de la magie! Ça te permet de formatter ton code automatiquement. Avec vs code, ça peut se faire à chaque fois que tu sauvegardes!
- .gitignore : Ça rapport à git. Tu es supposé connaître ça.
- jsconfig.json : Ta configuration pour la compilation
- next.config.json : Ta configuration de next (Le framework qu'on va prendre avec React.js)
- package.json : C'est ta liste de package et tes scripts. Ça vient avec un package.lock (Pacakges que tu as installé) et le dossier node_module (Tous les packages installés.)
- Ton code va dans /src/app
- les fichiers publiques (comme le favico), ça va dans le dossier public.

Pour démarrer le serveur, tu dois faire `npm run dev` dans le dossier avec le fichier package.json. Si tu regardes, on voit dev dans le ficher package.json. Ça appelle cette commande.

visite localhost:3000. Tu vas voir la page!

Essayons de déduire comment fonctionne React.js...