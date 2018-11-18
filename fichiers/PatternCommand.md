# Son but ?

Ce pattern répond au besoin d’émettre des requêtes sur n'importe quel objet, sans connaitre, ni ses caractéristiques, ni ses fonctions. Pour cela nous utilisons l’encapsulation des requêtes.

_Petit rappel :_ l’encapsulation consiste à cacher l'implémentation de l'objet, en empêchant l'accès aux données par un autre moyen que les services proposés. L'encapsulation permet donc de garantir l'intégrité des données contenues dans l'objet.

Comme vous l’aurez compris ce pattern a, tout d’abord, un but de sécurité dans les applications. Plus encore, ce pattern permet de supprimer toutes duplications de code, d’avoir une meilleure maintenance du code mais a aussi quelques fonctionnalités sympathiques que nous verrons à la fin de la présentation.

# Son implémentation ?

![Uml of Design Pattern Command](../images/DesignCommand_UML.png)  
Cela peut paraitre un peu barbare comme diagramme mais nous allons voir par la suite que le principe est très facile à comprendre.

Détaillons ce pattern :
-	Le client va déclencher une requete, role _d'invoker_
-	À cette action est associée une commande, une _concreteCommande_ implémentant l'interface _Commande_,
-	La _concreteCommande_ va ensuite déclencher la méthode de l'objet associée, il est le _receiver_.

# Parce qu'un exemple vaut mieux qu'un long discours...

**Sans pattern command :** 
Le client commande une salade composée. Il crée une nouvelle assiette, sur laquelle il exécute les méthodes : addSalade(), addPate() et addPoulet().

**Avec le pattern command :**
Le client actionne _l’Invoker_ de la salade césar (un bouton souvent).  
La _ConcreteCommande_ « PreparerSaladeCesar » est exécutée et va créer une nouvelle assiette.  
Ce qui permet d'invoquer les méthodes _addSalade()_, _addPate()_ et _addPoulet()_ de l’assiette.

![Uml of exemple PatternCommand](../images/DesignCommand_exCooking.PNG)

Ainsi, nous pouvons voir ici le rôle majeur de l'encapsulation. En effet, le client n’a pas connaissance ; ni de l’objet assiette, ni des méthodes qui lui sont appliquées.



