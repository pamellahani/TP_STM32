# TP_STM32
Systemes, Processeurs et Cartes

Albin Horlaville
Pamella Hani 
Asmae El Kanbi

Projet de SPC

Idée générale:  
Nous disposons d’au moins 4 lampes et de 4 interrupteurs 
Le jeu se déroule de la manière suivante: 
Les lampes s’allument en série dans un ordre aléatoire.
L’utilisateur doit retenir cette série et cliquer sur les boutons relatifs à chaque lampe afin de gagner le jeu. 
Si l’utilisateur gagne, les 4 lampes s’allument de manière synchrone pendant 1 seconde pour annoncer la victoire.
Sinon, les 4 LED clignotent 2 fois.
Améliorations :
Recommencer la partie si le joueur gagne;
Plus les victoires s’enchaînent, plus la série à reproduire est longue et complexe, ou rapide.

Schéma des LEDs associées à leur boutons poussoirs respectifs
La disposition exacte des LEDs et des boutons reste à définir pour optimiser l’espace sur la carte et éviter que le doigt du joueur n’interagisse sans le vouloir avec plusieurs boutons en même temps.

Pseudo Algo :
Choisir l’ordre d’allumage des LEDs (aléatoire idéalement)
Pour i allant de 1 au nombre d’élément de la série:
Attendre que le ième bouton soit pressé
Si un autre bouton est pressé, déclenchement de traitant d’interruption -> clignotement de toutes les LEDs deux fois, fin de la partie
Allumer toutes les LEDs 1 fois, synonyme de victoire, et de fin de partie

L’algorithme paraît simple mais nous préférons viser quelque chose de faisable puis améliorer notre programme si le temps nous est favorable. En axe d’amélioration, nous pourrions instaurer un affichage dans la console, une boucle de jeu dont la difficulté s’intensifie de partie en partie, ou encore un score du plus grand nombre de parties gagnées d'affilées.
