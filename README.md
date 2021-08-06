# 
Que signifie le DOM ? Comment est-il organisé?

Le Document Object Model (DOM) est une interface de programmation pour les documents HTML et XML.
Il fournit une page dont des programmes peuvent modifier la structure, son style et son contenu.
Cette représentation du document permet de le voir comme un groupe structuré de nœuds et d'objets possédant
différentes propriétés et méthodes. Fondamentalement, il relie les pages Web aux scripts ou langages de programmation

Les méthodes permettant d’accéder aux éléments du DOM
document.getElementById(ID)
document.getElementsByClassName(nomDeClasse)
document.getElementsByTagName(nomDeBalise(retourne plussieurs élements)
document.querySelector(selecteurCSS)
document.querySelectorAll(selecteurCSS)

document.getElementById(ID):La méthode getElementById() de Document renvoie un objet  Élément représentant l'élément dont la propriété 
id correspond à la chaîne de caractères spécifiée. Étant donné que les ID d'élément doivent être uniques, s'ils sont spécifiés, 
ils constituent un moyen utile d'accéder rapidement à un élément spécifique.Son syntaxe est: var element = document.getElementById(id)
document.getElementsByClassName(nomDeClasse):Renvoie un objet de type tableau de tous les éléments enfants qui ont tous les noms de classe donnés.
Lorsqu'il est appelé sur l'objet document, le document complet est recherché, y compris le nœud racine. Vous pouvez également
appeler getElementsByClassName () sur n'importe quel élément; il retournera uniquement les éléments qui sont les descendants de l'élément racine spécifié avec les noms de classes donnés.
document.getElementsByTagName(nomDeBalise): Renvoie une HTMLCollection des éléments avec le nom de balise donné. Le document complet est recherché, 
y compris le nœud racine. 
Le HTMLCollection renvoyée est en direct, ce qui signifie qu'elle se met à jour automatiquement pour rester synchronisée
avec l'arborescence DOM sans avoir à rappeler document.getElementsByTagName ().
document.querySelector(selecteurCSS): La méthode querySelector() de l'interface Document retourne le premier Element dans le document correspondant
au sélecteur - ou groupe de sélecteurs - spécifié(s), ou null si aucune correspondance n'est trouvée.
document.querySelector(selecteurCSS): La méthode querySelectorAll()  de Élément renvoie une NodeList statique représentant
une liste des éléments du document qui correspondent au groupe de sélecteurs spécifiés.
Quels sont les événements en JQuery? 


Les événements de Windows? scroll mouse clic

Un événement correspond à une action qu’on va pouvoir intercepter et à laquelle on va pouvoir réagir.
Un événement est un signal qui indique que “quelque chose vient de se passer”.
Ces actions vont généralement provenir soit du navigateur lui même, soit des utilisateurs. 
Les événements load et DOMContentLoaded par exemple qui se déclenchent lorsque la page complète
est chargée ou lorsque le DOM de la page est chargée tandis que l’événement click se déclenche lorsqu’un utilisateur 
clique sur un élément de la page.
Au moment où une telle action se produit, on dit que l’événement associée à l’action est déclenché (“fired” en anglais). 
Nous allons alors pouvoir “écouter” ou “intercepter” l’événement et y répondre en indiquant quoi faire dans une fonction
gestionnaire d’événements.
.resize() redimensionnement de la fenêtre du navigateur :sert à écouter l'événement de redimensionnement du navigateur.
Exemple:

$(window).resize(function() {
   alert('Je redimensionne mon navigateur');
});
méthode sera bien utile pour adapter certains de vos scripts au responsive webdesign. 
Par exemple, lors du calcul de hauteur de certains éléments. Nous le verrons d'ailleurs
dans la partie expliquant la manipulation de dimensions.
scroll() au scroll dans un élément:sert à écouter l'événement de scroll dans un élément
Exemple: ajout d’un message dans la console lors du scroll dans le navigateur
$(window).scroll(function() {
    console.log('Je scroll dans ma page');
});
