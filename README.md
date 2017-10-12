# keylogger
Projet sécurité - S4 - IUT A Lille

SURMONT Nicolas, Surmont.Nicolas@gmail.com
HIRSON Florian, Flohirson@gmail.com

Codé en C# sous Visual Studio Code

https://github.com/surmontn/keylogger.git

--------------------------------------------------

⚠ fonctionne uniquement sous windows ⚠

Pour complier : C:\Windows\Microsoft.NET\Framework\v3.5\csc.exe /t:exe /out:Executable.exe CodeSource.cs

-  l'emplacement de csc.exe ainsi que la version du framework 
   peuvent varier d'un environement à l'autre mais de base le compliteur 
   se trouve à l'emplacement C:\Windows\Microsoft.NET\Framework\v3.5\csc.exe
   (ou dans Framework\v3.5\bin\csc.exe)
   
-  Remplacer CodeSource.cs par le ficher à complier (ici Logger.cs)

-  Remplacer Executable.exe par le nom souhaité pour le programme compilé

--------------------------------------------------

Le programme un fois lancé, il ouvre (ou créé si innexistant) le ficher log.txt et y 
inscrit la dâte ainsi que l'heure du lancement. A son execution le programme masque 
la console anfin d'être le plus discret possible mais en revanche il est toujours 
affiché dans la liste des programmes en cours dans le gestionnaire des tâches. Il 
est donc conseillé de complier le code avec un nom discret que l'utilisateur n'osera
pas tuer (quelque chose comme "sysWin86" ou "Windows Local Host Process"). Lorsque 
que le programme tourne en arriere plan à chaque touche tapée par l'utilisateur le
programme va ouvrir log.txt y écrire la dernière touche puis le refermer. Ce n'est
pas le plus optimiser mais cela permet d'être sûr qu'on enregistre toutes les entrées.
Si on créé un buffer pour enregistrer toutes les x touches on riques de perdre des
données si l'utilisateur ferme le programme ou éteint sa machine.

Nous avons essayer de coder une fonction qui envoie les données par mail à une adresse
donnée mais cela demande l'acces aux services windows afin de fonctionner en arriere
plan. L'utilisateur devrait donc donner des droits au programme mais il perdrait toute
discretion.

--------------------------------------------------

source :

-  https://null-byte.wonderhowto.com
-  https://www.fortisfio.com/reperer-efficacement-un-keylogger-sur-sa-machine/
