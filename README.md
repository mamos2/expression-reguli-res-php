# expression-reguli-res-php


Les expressions régulières

Les expressions régulières constituent un système très puissant et très rapide pour faire des recherches dans des chaînes de caractères (des phrases, par exemple). C'est une sorte de fonctionnalité Rechercher / Remplacer

il existe deux types d'expressions régulières :

    POSIX :  son principal et gros défaut je dirais, c'est que ce « langage » est plus lent que PCRE ; 
	Il faut savoir cependant que MySQL ne comprend que les regex en langage POSIX, et pas PCRE

    PCRE : ces expressions régulières sont issues d'un autre langage (le Perl). 
	Considérées comme un peu plus complexes, elles sont surtout bien plus rapides et performantes.


Les fonctions qui nous intéressent:

	 Il existe plusieurs fonctions utilisant le « langage PCRE » et qui commencent toutes parpreg_ :

    
    preg_match : cette fonction renvoie un booléen : VRAI ou FAUX. 
		Elle renvoie true si elle a trouvé le mot que vous cherchiez dans la chaîne,false si elle ne l'a pas trouvé.
		Vous devez lui donner deux informations : 	
		
		 votre regex  et la chaîne dans laquelle vous faites une recherche.
		 chose importante à savoir : 
		 une regex (Expression régulière) est toujours entourée de caractères spéciaux appelés délimiteurs.
		 
			    	exemple: 		
					<?php
					if (preg_match("** Votre REGEX **", "Ce dans quoi vous faites la recherche"))
					{
						echo 'Le mot que vous cherchez se trouve dans la chaîne';
					}
					else
					{
						echo 'Le mot que vous cherchez ne se trouve pas dans la chaîne';
					}
					?>

    preg_replace ;	Rechercher et remplacer par expression rationnelle standard. 
		Analyse subject pour trouver l'expression rationnelle pattern et remplace les résultats par replacement.
		pattern est Le motif à chercher, sous la forme d'une chaîne de caractères.



    preg_grep ; 	preg_grep — Retourne un tableau avec les résultats de la recherche


    preg_split ;	preg_split — Éclate une chaîne par expression rationnelle


    preg_quote ;	 Protection des caractères spéciaux des expressions rationnelles. 
		les caractères spéciaux qui seront protégés sont les 				 suivants : . \ + * ? [ ^ ] $ ( ) { } = ! < > | : -


 
  


