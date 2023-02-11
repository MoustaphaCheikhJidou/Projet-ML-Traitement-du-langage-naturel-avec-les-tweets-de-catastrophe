# Projet de traitement du langage naturel avec les tweets de catastrophe

## Introduction

Ce projet a pour objectif de construire un modèle de traitement du langage naturel capable de détecter les tweets relatifs à une catastrophe. Pour ce faire, nous utilisons une base de données de tweets qui ont été étiquetés comme étant relatifs à une catastrophe ou non. Le modèle est entraîné sur cette base de données et est ensuite utilisé pour prédire si un nouveau tweet est relatif à une catastrophe ou non.

## Préparation des données

La base de données utilisée pour ce projet contient des tweets en anglais qui ont été étiquetés comme étant relatifs à une catastrophe ou non. Les tweets ont été nettoyés pour enlever les liens, les mentions d'utilisateurs et les hashtags. Les données ont été divisées en deux ensembles : un ensemble d'entraînement et un ensemble de test.

## Modèle

Pour construire notre modèle, nous avons utilisé la bibliothèque Keras avec Tensorflow comme backend. Le modèle est basé sur un réseau de neurones à couches multiples (RNN) avec une couche d'embedding pour traiter les données textuelles, une couche LSTM pour capturer les dépendances à long terme dans les données et une couche dense pour la classification binaire. 

La fonction de coût utilisée est `binary_crossentropy` et l'algorithme d'optimisation est `Adam`.

## Evaluation

Notre modèle a été évalué en utilisant l'accuracy comme métrique. L'accuracy obtenue sur l'ensemble de test est de 84%.

## Utilisation

Pour utiliser notre modèle, vous pouvez utiliser la fonction `predict_disaster(tweet)` qui prend en entrée un tweet et retourne "Catastrophe" si le tweet est prédit comme étant relatif à une catastrophe, "Non Catastrophe" sinon.

Vous pouvez également utiliser l'interface utilisateur fournie par la bibliothèque Gradio pour interagir avec le modèle.

## Conclusion

Dans ce projet, nous avons construit un modèle de traitement du langage naturel capable de détecter les tweets relatifs à une catastrophe avec une accuracy de 84%. Ce modèle peut être utilisé pour détecter rapidement les tweets relatifs à une catastrophe lors d'une situation d'urgence, ce qui peut aider les organisations à prendre des décisions éclairées.
