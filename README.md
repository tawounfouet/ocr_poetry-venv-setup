# ocr_poetry-venv-setup
Template pour Mettre en place votre environnement virtuel Python avec Poetry


```shell
# Installez Poetry et votre premier environnement

python --version


# Installation de Poetry
# Le site officiel de Poetry recommande d’utiliser  pipx  pour installer Poetry. Pour cela, dans votre terminal, entrez la commande suivante :
pip install pipx
python3 -m pipx ensurepath

pipx install poetry


# Déclaration des packages
# Lancez dans votre terminal la commande :  
poetry init


# Ajout des dépendances

# Vous pouvez très facilement rajouter un package manquant à votre environnement en utilisant la commande  poetry add

# Ajoutez les dépendances nécessaires à votre projet. Par exemple, si vous avez besoin de Flask et de Requests, exécutez la commande suivante :
poetry add flask requests

# Ajout de dépendances pour Jupyter Notebook
# Si vous souhaitez utiliser Jupyter Notebook, vous pouvez également ajouter ipykernel en tant que dépendance. Exécutez la commande suivante :
poetry add ipykernel

poetry add jupyterlab


# Activez votre environnement virtualisé
# Pour activer l'environnement virtuel créé par Poetry, utilisez la commande suivante :
poetry shell

# Note that the env activate command is not a direct replacement for shell command.
# It is used to activate the virtual environment in the current shell session.

# env activate
poetry env activate


# Désinstaller une dépendance :  
poetry remove  

# Poetry env list  pour regarder la liste des environnements que vous avez (pour le moment qu’un seul, mais au fil de la formation, vous en aurez plusieurs !).
poetry env list

# Si vous êtes curieux, vous pouvez regarder toutes les sous-dépendances d’un package avec la commande :  poetry show nom_du_package --tree
# Par exemple, pour voir les sous-dépendances de Flask :
poetry show pandas --tree

# Pour quitter l'environnement virtuel, utilisez la commande suivante :
deactivate


# Si vous êtes encore plus curieux, voici toutes les commandes possibles que vous pouvez réaliser avec Poetry.
https://python-poetry.org/docs/cli/ 



# poetry completions bash >> ~/.bash_completion
```


## New Demo Project - From Docs

```shell
# Create a new project
poetry new poetry-demo

# Change into the project directory
cd poetry-demo

# Install dependencies
poetry install
# Add a new dependency
poetry add requests
# Add a new development dependency
poetry add --dev pytest
# Add a new optional dependency
poetry add --optional requests[security]
# Add a new dependency with a specific version
poetry add requests@^2.25.1
# Add a new dependency with a specific version range
poetry add requests@^2.25.1,<3.0
# Add a new dependency with a specific version and extras
poetry add requests@^2.25.1[security]

```


## Initialising a pre-existing project

```shell
cd pre-existing-project
poetry init

```