# Bootcamp pyspark

Ce répertoire contient les énoncés des TP de la formation Data Science destinée à un public technique.
Une version de python >=3.9,<3.11 est nécessaire pour réaliser ces TP.

## Installation de python via `pyenv`

Il est possible de gérer différentes versions de python via `pyenv`.

Installer les dépendances nécessaires à `pyenv`:

Sur WSL :
```
make install-pyenv-dependencies-wsl
```

Sur MacOS:
```
make install-pyenv-dependencies-mac
```

Installer `pyenv`:
```
make install-pyenv
```

Ajouter les lignes suivantes dans `~/.bashrc` ou `~/.zshrc` puis redémarrer le terminal:
```
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

Installation de d'une version de python via `pyenv` (ici 3.9.13) et utilisation de cette version dans le projet `formation-ds-for-tech`:
```
pyenv install -v 3.9.13
pyenv virtualenv 3.9.13 bootcamp-pyspark
cd bootcamp-pyspark
pyenv local bootcamp-pyspark
```

## Installation de `poetry`

Avant de démarrer, il faut d'abord installer `poetry` (voir la [documentation officielle](https://python-poetry.org/docs/#installation)).
L'installation peut se faire via la commande suivante :

```
make install-poetry
```
Ajouter la ligne suivante dans `~/.bashrc` ou `~/.zshrc` puis redémarrer le terminal:
```
export export PATH="$HOME/.local/bin:$PATH"
```

Si l'installation s'est correctement déroulée, la commande `poetry --version` doit renvoyer la version installée.

L'environnement virtuel peut ensuite être installé.

```
cd bootcamp-pyspark
make install
```

## Démarrage des TP

Pour consulter les TP via Jupyter Notebook, se mettre dans le dossier `bootcamp-pyspark` et utiliser la commande suivante :
```
poetry shell
jupyter notebook
```
