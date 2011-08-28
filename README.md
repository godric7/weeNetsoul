weeNetsoul
========
Module Netsoul pour WeeChat

Comment installer weeNetsoul ?
----------------------------
1. Télécharger la dernière version du script.
2. La copier dans ~/.weechat/python/autoload ou pas autoload si on veut le lancer à la main.
3. Lancer weechat ou creer le fichier de conf ~/.weechat/weeNetsoul.conf

Configuration
------------------
Le fichier de configuration doit ressembler à ceci :
<pre>
[server]
  host = "ns-server.epita.fr"
  port = "4242"
  login = "login_x"
  password = "pass socks"
  data = "-"
  location = "-"
  contacts = "login_1,login_2,...,login_n"
</pre>
Bien sur, /set weeNetsoul.server.option value ca marche aussi

Fonctionnement
------------------
Dans weechat
<pre>/ns connect | disconnect | send &lt;login|:fd&gt; &lt;msg&gt; | state &lt;status&gt; | who &lt;login&gt;
  connect    : Connection
  disconnect : Deconnection
  send       : Envoyer &lt;msg&gt; à &lt;login&gt; (tous ses clients) ou à &lt;:fd&gt; (client unique)
  state      : Changer son status pour &lt;status&gt; (en ligne/actif/whatever)
  who        : Afficher les infos sur &lt;login&gt;
</pre>

Wahoo c'est so powerfull, quoi d'autre ?
------------------

* Le buffer weeNetsoul contient une nicklist des contacts définis dans les options. Si ils sont connectés, on voit des infos sur leur clients : c'est magique.
* Toute ce qui est reçu/envoyé par le client s'affiche dans le buffer weeNetsoul préfixé par une petite flèche comme dans le module IRC, comme ça vous pouvez admirer le super protocole : c'est ludique.
* Tout ce qui est tapé dans le buffer weeNetsoul est envoyé au serveur Netsoul, comme ça vous pouvez faire planter les clients de vos amis et meme utiliser des cheat-codes : c'est triptique.

Qui à commis ça ?
------------
C'est [godric][home]

[home]:http://www.0x3f.fr
