# Configuration du workspace

> Environment de travail : ```Windows 10, version 21H2``` avec ```WSL2``` activé pour ```Ubuntu 20.04 LTS```\
> Bash : ```MobaXterm``` + ```Windows Terminal```\
> IDE : ```Visual Studio Code```

Installer et configurer WSL2 ([ici](https://github.com/matritz-pro/share/tree/main/systemes_reseaux/wsl#readme))

> Toutes les commandes qui suivent ont été éxecutées sous ubuntu

Obtenir la dernière mise-à-jour du système
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

Obtenir la dernière mise-à-jour de python3
```bash
sudo apt-get upgrade python3
```

> Purger les fichiers systèmes obsolètes
```bash
sudo apt-get purge --autoremove
```

Créer un répertoire de projet et se placer dedans
```bash
mkdir django-web-app && cd django-web-app
```

Créer un dépot [Github](https://github.com/new) (le dépot est gérée pour ma part grâce à l'application ```Github Desktop```)

Créer les fichiers ```README.md``` et ```.gitignore```
```bash
echo "# django-web-app" > README.md
touch .gitignore
```

Installer le gestionnaire de paquets ```pip```
```bash
sudo apt-get install python3-pip
```

Installer le paquet ```venv```
```bash
pip install venv
```

Créer un environnement virtuel
```bash
python3 -m venv .venv
```

Activer l'environnement virtuel crée précédement
```bash
source .venv/bin/activate
```

> Désactiver l'environnement virtuel
```bash
deactivate
```
> Supprimer l'environnement virtuel
```bash
rm -Rf .venv/
```

Ecarter l'environnement virtuel du dépot Github
```bash
echo ".venv" >> .gitignore
```

Installer un paquet
```bash
pip install {package_name}
```

Enregistrer les paquets requis par l'application dans le fichier ```requirements.txt```
```bash
pip freeze > requirements.txt
```

> Installer les paquets répertoriés dans le fichier ```requirements.txt```
```bash
pip install -r requirements.txt
```
> Afficher la liste des paquets installés
```bash
pip list
```
> Afficher plus d'informations sur un paquet installé
```bash
pip show {package_name}
```
