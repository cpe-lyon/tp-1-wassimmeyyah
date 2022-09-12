Wassim MEYYAH- 3ICS

# TP1 – Installation d’Ubuntu Server et prise en main du shell

## Exercice 2 - Prise en main de l’interpréteur de commandes 

Manuel
1.	  La commande which produit le chemin complet des commandes du shell. Si elle ne peut pas reconnaitre la commande donnée.
2.	  Pour consulter une page du manuel on utilise : man + nom de la commande, en l’occurrence « man which »
3.	  Il est possible de quitter le manuel en appuyant sur la touche « q »
4.	  Pour afficher la première page de la section 6 du manuel on utilise la commande : man 6 intro
	    Cette section a pour description : « Section 6 of the manual describes the games and funny little programs available on the system. »

Navigation dans l’arborescence
1.	  cd /var/log 
2.	  cd ..
3.	  cd ~
4.	  cd -
5.	  Nous n’avons pas les droits pour accéder au dossier root 
6.	  La commande sudo n’est pas disponible, car nous n’avons pas installé le package
7.	
      ```bash
      cd ..
      mkdir Dossier1 Dossier2
      cd Dossier1
      touch Fichier1
      cd Dossier2
      mkdir Dossier2.1
      mkdir Dossier 2.2
      cd Dossier2.2
      touch Fichier2
      touch Fichier3
      ```

8.	  Il est impossible de les supprimer : fichier1 car nous ne sommes pas au bon emplacement, dossier1 car la commande rm permet de supprimer des fichiers et non des dossiers
9.	  « rmdir » permet de supprimer un dossier
10.	  La suppression échoue : le dossier doit être vide pour être supprimé de cette manière
11.	  rm –r Dossier2 est la commande qui permet de supprimer le dossier2 et ce qu'il contient

Commandes importantes
1.	  Pour afficher l’heure on utilise la commande : date. La commande time est un chronomètre qui calcule le temps lors de l’exécution d’un logiciel.
2.	  Les fichiers débutants par un point sont des fichiers cachés.
3.	  /usr/bin/ls
4.	  La commande ll permet de connaitre les droits de chaque utilisateur (lecture/modification/exécution). La commande manuelle de ll est ls -alF
5.	  Pour afficher le contenu du dossier /bin on utilise: ls /bin 
6.	  ls .. affiche les dossiers et fichers parents
7.	  Pour afficher le chemin complet du dossier courant on utilise pwd et on optient ce chemin : /home/User
8.	  La commande echo ‘bip’ > plop exécutée 2 fois affiche une fois le mot bip dans le fichier plop même si on réitère la commande plusieurs fois.
9.	  La commande echo ‘bip’ >> plop exécutée 2 fois affiche le mot bip 3 fois dans le fichier plop, le mot sera donc affiché autant de fois que l’on exécute la commande.
10.	  Cette commande affiche toto et bloque l’utilisation de la ligne de commande durant le temps spécifié
11.	  La commande file affiche le type du fichier choisie (vidéo, photo, texte ...)
12.	  echo ‘Hello Toto !’ > original et pour modifier le contenu de original on fait echo ‘Hello Toto Modif !’ > original et pour afficher le contenu de lien_phy on fait cat lien_phy. Le contenu est le même dans les deux fichiers. Pour supprimer original on fait rm original et le fichier orignal est supprimé mais le fichier lien_phy et son contenu existe toujours.
13.	  Pour modifier lien_phy on fait : echo ‘Hello Toto Modif Bis !’ > lien_phy et si on modifie lien_phy la modifiction se fait aussi dans lien_sym. Et si on supprime lien_phy avec la commande rm lien_phy cela supprime aussi le lien symbolique. 
14.	  Pour afficher le fichier syslog on fait la commande cd /var/log puis CTRL + S et pour arreter le défilement et le reprendre on fait la commande CTRL + Q
15.	  head -5 syslog pour afficher les 5 premières lignes du fichiers et tail -15 syslog pour afficher les 15 dernières lignes. Pour afficher les lignes 10 à 20 on utilise : cat syslog | tail –n +10 | head –n 10
16.	  Cela affiche les logs dans un lecteur de fichier afin d'en faciliter la lecture.
17.	  Ce fichier contient les noms de tous les utilisateurs. man -5 psswd
18. 	cat /etc/passwd | awk '{ print $1 }' | sort -r
19. 	cat /etc/passwd | wc -l
20. 	man -k conversion | wc -l
21. 	find / -name passwd
22. 	find / -name passed 2>/dev /null > ˜/list_passwd_files.txt
23. 	grep « alias ll=«  -r ˜, il se trouve dans «˜/.bashrc »
24. 	Impossible d’installer locate
25. 	Impossible d’installer locate
 
## Exercice 3 - Découverte de l’éditeur de texte nano 
1.	  touch log.txt -> cp /var/log/syslog log.txt -> nano log.txt
2.	  Ctrl \ kernel noyau A
3. 	  Alt + A puis Ctrl + K et au bas du fichier on fait Ctrl + U 	 
4.	  Alt U permet d’annuler l’action précédente

## Exercice 4 - Personnalisation du shell 

Questions 1 à 3 : tests commandes 
4.    \A[\033[01;35m] - \u@\h[\033[32m]:[\033[01;34m]\w[\033[36m]$

