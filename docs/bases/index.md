# Les bases du réseau

Pour des raisons évidentes je ne vais pas passer par les bases à partir de zéro, voici les prérequis afin de comprendre correctement le contenu de ce site :

* Savoir ce qu'est une adresse IP (v4 et/ou v6)
* Connaître le modèle OSI (avec la couche 8 en bonus, l'interface chaise-clavier)
* Avoir des bases en administration de système (invite de commandes...)
* Savoir ce que sont les différents 'appareils' réseau (routeur, commutateur...)
* Savoir qu'on ne croise pas les flux (utilisation de câble droit et croisé)

## Conventions

Afin de garder un réseau cohérent il est préférable de maintenir une unique convention tout au long de la vie du réseau.

> Je propose ici une convention fonctionnant bien par expérience, permettant de guider les nouvelles installations, mais elle n'est en aucun cas à prendre en tant que telle au pied de la lettre, libre à l'administrateur de faire ce qu'il souhaite.

* Utiliser l'adresse IP `x.x.x.254` pour un routeur, ou la plus grande adresse disponible sur le sous-réseau
* Utiliser l'adresse IP `x.x.x.1` pour les appareils, ou la plus petite adresse disponible sur le sous-réseau
* Utiliser le numéro d'interface le plus bas possible en suivant :
    * Utiliser la _meilleure_ interface pour les liens importants
        * Utiliser un lien Gigabit-Ethernet pour une liaison **routeur - routeur** et pas pour une liaison **ordinateur - commutateur**
    * Utiliser le numéro d'interface **le plus bas** en lisant le schéma réseau de gauche à droite et de haut en bas
    * Utiliser le numéro d'interface **le plus haut** pour les liaisons de sortie (ex: Gigabit-Ethernet 0/4 pour le WAN)

## PacketTracer

Pour l'émulation de réseau j'utilise PacketTracer de Cisco.

[Installer PacketTracer](/bases/installer-packettracer){ .md-button }

