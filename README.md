# Projet-Linux-Bash-HTML-
L'objectif de ce projet est d'afficher dans un tableau les groupes et leurs utilisateurs, l’espace occupé par chaque utilisateur et le nombre de répertoires ainsi que le nombre de fichiers de chaque utilisateur en utilisant HTML et Bash.

Etude du script :
On a créé un script nommé mip, dans ce scipt on a créé le code suivant :
![image](https://user-images.githubusercontent.com/122173924/211215168-c1ab58cf-2451-4daf-a13c-e7237bd907c8.png)
![image](https://user-images.githubusercontent.com/122173924/211215172-1935126a-b028-4759-9c70-c36f11959c37.png)
Dans ce code on va générer une page html nommée projet de linux grâce  à la commande echo, qui permet d’envoyer le code de la création d’une page html au fichier projet.html, après on va faire une boucle pour afficher  les noms des utilisateurs  qui existent dans le fichier /etc/passwd, ce dernier contient les informations sur les utilisateurs   sous forme suivant login : passwd : uid : gid : comment : home(le chemin d’accès à chaque utilisateur) : Shell
Comme montre cette figure :
![image](https://user-images.githubusercontent.com/122173924/211215268-bd803eb5-35a5-4bf6-8d32-78e61139d805.png)
 Pour  afficher les noms des utilisateurs  on récupère la première colonne de ce fichier, et pour connaitre le chemin d’accès à chaque utilisateur  on sélectionne la colonne 6, et grâce à la commande groups login on peut savoir le group de chaque utilisateur, et pour connaitre le nombre de répertoire et de fichiers, il suffit d’utilisé la commande find en spécifiant le type.
 
find le chemin d’utisateurs –type d pour chercher les répertoires
Et  find le chemin d’utilisateur –type f  pour chercher  les fichiers
Apres ceci on calcule le nombre de lignes de chaque résultat on utilisant une pipe et la commande 
wc –l
Concernant la taille totale des utilisateurs on a utilisé la commande du –sh le chemin d’utilisateur, cette commande renvoie l’espace mémoire totale.
et pour donner les droits d’exécution au fichier mip, on a utilisé la commande chmod a+x mip

Le résultat final:
![image](https://user-images.githubusercontent.com/122173924/211215421-830e00c2-f670-45ec-b661-3790927d352f.png)





