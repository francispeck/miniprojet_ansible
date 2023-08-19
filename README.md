# Installation d'apache via ansible

- Sur ce mini projet, il etait question d'ecrire un rôle ansible pour ensuite l'appeler dans un playbook

- Le but était d'installer une application apache, pas de l'installer from scratch mais de le conteneuriser i-e de deployer un conteneur docker d'apache

- Pour ce mini projet, j'ai deployé une machine virtuelle ansible comme master qui pilote deux autres machines qui sont des workers en utilisant centos 7
- J'ai un worker appelé Client1 qui est dans un environnement de developpement Prod et l'autre Client2 en staging.

- Dans un premier temps, il faut installer docker avec ses dépendances à l'aide de ansible et aussi installer python avec la librairie pip mais aussi 
  toutes les frameworks python qui va permettre de piloter docker à l'aide d'ansible en l'occurance une librairie python appelé docker.py

  En résumé, la librairie python docker-py qui est sur l'un des workers va permettre à ansible qui est sur la machine hôte de piloter le demon docker pour
  déployer le conteneur applicatif apache.
