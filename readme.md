OPENCLASSROOMS Gérer du code avec Git et GitHub (juillet 2025)







      on a créé un compte dur GitHub, puis installé Git sur notre ordinateur

      on initialise notre premier dépôt GIT dans la fenêtre Git Bash = création d'un dossier qui va accueillir notre projet Git = création du Working Directory (directory = dossier).

 		2 commande unix : **cd** pour se déplacer dans les dossiers de l'ordinateur. cd Documents => on va dans le dossier Documents.

 				  **mkdir** pour créer un nouveau dossier, dans Documents par exemple.







Configurer Git (une bonne fois pour toute = du code incompréhensible mais pas à comprendre… c'est fait!)

 				**git config --global user.name**

&nbsp;					        \*\*.email\*\*
						\*\*color.diff\*\*
						\*\*.status\*\*
                                                \*\*.branch\*\*
						\*\*core.editor vim\*\*
		 				**...**





Initialisation de notre projet Git

 	$ **cd** Documents/PremierProjet

 	$ **git init** : crée un dossier caché .git dans notre dossier courant ; il contient la config de notre projet Git, ses objets et son pointeur









Initialisation d'un premier dépôt (Travail sur premier dépôt et commandes de base Git

    	on crée 2 fichiers index.html et style.css dans le WORKING DIRECTORY. on écrit du code dedans.

 	Puis on les **indexe** cad les conserver dans une zone appelée STAGE ou INDEX (les 2 appellations s'entendent)

 	Quand on est prêt à valider nos fichiers modifiés, on les envoie dans le REPOSITORY = dépôt local (stockage de toutes les versions de mon code)= "**commiter** un fichier"

 	On peut alors en envoyer une version sur GitHub pour en avoir une version sur le Cloud = on "**push** son code"



 	en local

 		WORKING DIRECTORY

 		STAGE ou INDEX

 		REPOSITORY

 	dans le cloud

 		GITHUB







Les commandes de base (à utiliser très fréquemment , à chaque sauvegarde):

 	**cd** pour se replacer dans le bon dossier

\*\*git init\*\* : crée un dossier caché .git dans notre dossier courant 


 	**touch** index.html : création d'un fichier avecv la commande unix touch créatiuon dans le working directory

 	**git add** index.html : pour passer (ou indexer) ce nouveau fichier dans l'INDEX ou STAGE . Donc à utiliser à chaque modification de index.html

 	**git commit -m** "...commentaire..." pour passer le fichier indexé dans le REPERTORY (-m, comme message, est un argument)

 			Attention : bien mettre un message clair et explicite pour s'y retrouver dans les version (pas de v1 v2 v2.1 ...)







PROCEDURE DE "SAUVEGARDE" DE FICHIERS MODIFES OU CREES



 	1/ indexation du fichier :

 		Outil Git Bash / $ git add

 			ex pour 2 nouveaux fichiers index.html et styles.css : $ git add index.html styles.css



 	2/ création d'une nouvelle "version" du projet (dans REPOSITORY):

 		Outil Git Bash / $ git commit -m "Ajout des fichiers modifiés A et B"

 			ex pour nos 2 nouveaux fichiers : $ git commit -m "Ajout des fichiers html et css de base"



 	3/ envoi du commit vers le dépot distant (on push le code - suivant le protocole HTTPS ou SSH qui evite de s'identifier à chaque fois):

 		(travail préalable : généré une clé SSH, l'ajouté à ssh-agent si nécessaire, garder une copie de cette clé)







&nbsp;	4/ "push" le code dans GitHub



&nbsp;		POUR LA PRMEIER CONNEXION SEULEMENT

&nbsp;		4.1/ Création d'une (paire de ) clé(s) SSH = complexe , à suivre à la lettre . On arrive à la création d'une clé SSH dans GitHub

 			dans Git Bash ;  ssh-keygen -t ed25519 -C "pierreleoa@gmail.com"

&nbsp;			…

&nbsp;			Maintenant on peut "push" notre code.

&nbsp;		4.2/ relier le dépôt local au dépôt à distant (càd notre compte GitHub)

&nbsp;			ouvrir mon profil (haut à droite) / Your repositories / "cliquer sur "first-test" /SSH dans "Quick setup" et on copie le lien généré

&nbsp;			retour à Git Bash, 



&nbsp;		A CHAQUE NOUVELLE SAUVEGARDE

&nbsp;		4.3/ Reprenez le fichier HTML créé. Disons que vous allez modifier le titre “Un super titre” en “Un super titre !”.

&nbsp;			Pour créer une version du projet avec le fichier HTML à jour et l’envoyer sur le dépôt distant GitHub, vous allez :

&nbsp;			**Indexer le fichier HTML modifié grâce à la commande :** 

			**git add index.html**



			**Créer une nouvelle version grâce à la commande :**

			**git commit -m “Modification du titre H1”**



			**Envoyer la nouvelle version sur le dépôt distant grâce à la commande :**

			**git push origin main**



Et voilà ! Vous savez maintenant utiliser les commandes  git add  ,  git commit  et  git push





 

... 

