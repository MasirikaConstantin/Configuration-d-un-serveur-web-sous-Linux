# Groupe_26
Le Sujet est : Installation d'un serveur web sous Unix

Dans ce fichier nous allons expliciter tous les processus poursouivis pour arriver à installer le server Web Sous linux
Pour notre projet nous avons choisit la distribution Ubuntu pour réaliser ce travail. 

Un serveur Web est un ensemble de programmes de gestions d’Internet et d’intranet chargés d’acheminer les requêtes de la machine client et dereconstituer et de publier des pages Web. Tous les ordinateurs qui hébergent des sites web doivent disposer de programmes serveurs. Les plus répandus est le serveur Apache, IIS (internet Information Server) de Microsoft et bien d’autre serveur qui existe actuellement. 
Pour notre cas nous allons configurer notre serveur Web avec le serveur Apache qui est un outils Open Sources et qui répond aux certaines caractéristiques :

- Compatibilité avec le Système d’Exploitation, 
- Capacités à prendre en charge la programmation coté serveur, 
- Les mécanismes de sécurité et
- Les outils particuliers fournis pour la publication etc.

 Dans cette section nous allons élaborer les étapes nécessaires de la configuration du serveur Apache sous Linux avec la distribution Ubuntu 22.0.LTS.
 
1. Lancement de la fenêtre du terminal : Le tout commence avec le terminal (la console), ouvrir le
terminal avec la combinaison des touches `Ctrl + Alt +T `.

2. Installation du serveur
Le serveur web après avoir l’ouverture du terminal de commande. La commande `sudo apt-get update` pour la mise à jour des paquets du système.
Et ensuite on installe le serveur Web Apache avec la commande `sudo apt-get install apache2`

3. Configuration de la sécurité : Le serveur est une partie cruciale des applications web. Apache Web Server est souvent placé à la vue du réseau qui le rend plus vulnérables aux attaques. Ainsi il est plus important de configurer la sécurité de notre serveur pour paliers à ses attaques.
- Les applications autorisées La commande permet de voir la liste des applications autorisées par le parefeu : `sudo ufw app list`
- Autorisée le serveur Apache via le pare-feu on fait la commande : `sudo ufw app allow Apache`

4. Configuration du nom de domaine : Un nom de domaine est un identifiant de domaine Internet. Il agit comme une adresse que les gens utilisent pour trouver un site web.
- La configuration du nom de domaine se fait avec un fichier qui sera éditer avec `nano`. La commande suivante créée un fichier de configuration pour le nom de domaine : `sudo nano /etc/apache2/sitesavaillable/exampe.com.com`
- Après la configuration du fichier on tape la commande `sudo a2ensite example.com.conf` pour activer la configuration du nom de domaine.

5. Configuration du dossier racine : La commande sudo mkdir /var/www/example.com crée un dossier racine de notre serveur. Et la commande `sudo chown -R $user :$user /var/www/groupe26.com` donne les droits d’accès.

6. Redémarrage du serveur Apache http : Le redémarrage permettra de vérifier si la configuration se bien passé. La commande `sudo systemctl restart apache2` redémarre le serveur.

          Dans ce travail nous avons utiliser les bibliographies telles que:
1. Ubuntu-fr.org : site officiel de la communauté de Ubuntu (Site Web);
2. Ubuntu - Mettez en place et administrez un votre serveur Linux (Edition Eryrolles, 2ème edition);
3. Configuration de la sécurité d’un serveur Apache http : www.geekflare.com (Site Web des tutoriels pratique)

                                                                       Merci beaucoup
