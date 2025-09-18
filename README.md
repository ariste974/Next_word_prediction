# Prédiction de Texte avec Sherlock Holmes

## Description
Ce projet consiste à développer un modèle de prédiction de texte capable de suggérer le prochain mot d'une phrase. Plusieurs approches ont été explorées, allant des réseaux de neurones récurrents (RNN) et des LSTM classiques aux Transformers modernes, ainsi qu'à des modèles pré-entraînés comme DistilGPT2.

## Auteurs
- Ariste Mathiot

## Données
Le projet utilise le dataset **"Sherlock Holmes Book Text Data"**, qui contient le texte complet des histoires de détective écrites par Sir Arthur Conan Doyle mettant en scène Sherlock Holmes. Ce jeu de données est idéal pour des tâches de prédiction de texte et de modélisation du mot suivant.

## Technologies Utilisées
- **Langage** : Python
- **Bibliothèques** :
  - TensorFlow/Keras
  - Transformers (Hugging Face)
  - Pandas, NumPy
  - Matplotlib/Seaborn pour la visualisation

## Modèles Implémentés
1. **RNN Simple** : Utilisation d'un RNN avec early stopping sur la perte de validation.
2. **RNN avec Dropout** : Ajout de dropout pour améliorer la généralisation et éviter l'overfitting.
3. **LSTM Simple** : Implémentation d'un modèle LSTM de base.
4. **Transformers** : Utilisation d'architectures Transformer pour capturer des dépendances à long terme.
5. **DistilGPT2** : Utilisation d'un modèle pré-entraîné pour évaluer les performances sur la tâche de prédiction de texte.


## Réflexions
- **RNN et LSTM** : Les modèles RNN et LSTM ont montré des performances acceptables, mais ils sont limités par leur capacité à capturer des dépendances à très long terme. L'ajout de dropout a aidé à réduire l'overfitting, mais n'a pas suffi pour surpasser les architectures plus avancées.

- **Transformers** : Les Transformers ont démontré une capacité supérieure à modéliser les dépendances complexes dans le texte, grâce à leur mécanisme d'attention. Cependant, ils nécessitent plus de données et de ressources computationnelles.

- **DistilGPT2** : Ce modèle pré-entraîné a offert les meilleures performances, grâce à son architecture avancée et son pré-entraînement sur de vastes corpus de texte. Cependant, il est important de noter que son utilisation nécessite un fine-tuning adapté pour éviter le surapprentissage sur des données spécifiques.

## Comment Exécuter le Projet
1. **Installer les dépendances** :
   ```bash
   pip install tensorflow numpy pandas matplotlib seaborn transformers
