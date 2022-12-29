## **Justification des choix du modèle** : 
## 1. Type du modèle : Reseau de Neurones Convolutif (CNN)  
### Nous avons choisi les CNN pour leur : 
### a) Capacité à extraire des caractéristiques: Les CNN sont conçus pour extraire des caractéristiques des données d'entrée ou features (par exemple, contour, texture, couleur ...) en utilisant des filtres de convolution et des couches de pooling. Ces caractéristiques sont généralement utilisées comme entrées pour les couches de neurones fully-connected qui sont utilisées pour effectuer la classification ou la prédiction.
### b) Robustesse aux translations: Les CNN sont généralement robustes aux translations des données d'entrée, ce qui signifie qu'elles peuvent généraliser leurs performances sur des images qui ont été déplacées par rapport à celles sur lesquelles elles ont été entraînées. Cela les rend souvent utiles pour les tâches de vision où les objets peuvent être présents à différents endroits dans l'image.
### c) Efficacité : Les CNN sont souvent plus efficaces que les modèles linéaires en termes de temps de calcul et de mémoire, ce qui les rend souvent pratiques pour les tâches de vision à grande échelle.

                           -*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
## 2. Architecture du modèle : 
### 2.1 Backbone : ResNet18 
#### Nous avons choisi ResNet18 car il est efficace lorsqu'on dispose d'un petit dataset comme notre cas ici (90 images). Mais aussi, ResNet18 est la version plus petite de l'architecture ResNet, qui est connue pour sa capacité à entraîner des réseaux de neurones très profonds sans risque de surapprentissage.
                           -*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
## 3. Paramètres du modèle :
### 3.1 Fonction d'activation : ReLU (Unité Linéaire Rectifiée)
#### nous avons choisi  ReLU pour sa :
#### a) Simplicité: La fonction ReLU est simple à calculer et à dériver ce qui la rend facile à implémenter et à utiliser. 
#### b) Rapidité de convergence: La fonction ReLU permet souvent une convergence plus rapide des modèles par rapport à d'autres fonctions d'activation, ce qui peut réduire le temps nécessaire pour entraîner le modèle.

### 3.2 Optimiseur : SGD (Descente de Gradient Stochastique)
#### nous avons choisi SGD pour sa :
#### a) Simplicité: L'optimiseur SGD est un algorithme simple qui ne nécessite pas de calculer la dérivée de la fonction de coût en chaque étape. Cela le rend souvent plus rapide à implémenter et à exécuter que d'autres algorithmes d'optimisation.
#### b) Scalabilité: L'optimiseur SGD n'est relativement peu coûteux en termes de calculs et de mémoire ce qui fait il peut etre utilisé pour entraîner de grands modèles sur de grandes quantités de données.
#### c) Robustesse: L'optimiseur SGD est souvent robuste aux conditions initiales et aux paramètres choisis, ce qui le rend souvent moins sensible aux variations de ces paramètres que d'autres algorithmes d'optimisation.
#### d) Sélection de modèle: L'optimiseur SGD peut être utilisé pour sélectionner un modèle parmi une variété de modèles en comparant leurs performances sur un dataset de test.

                           -*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
## 4. Métriques d'évaluation du modèle : 
### 4.1 Fonction de coût / erreur : Entropie croisée ou fonction de coût logistique
#### nous avons choisi  l'entropie croisée car:
#### a) Elle est souvent bien adaptée aux tâches de classification: la fonction d'erreur entropie croisée est souvent utilisée dans les modèles de classification supervisée en raison de sa capacité à mesurer l'écart entre les prédictions du modèle et les valeurs cibles.
##### b) Elle est souvent facile à calculer et à optimiser.
####  c) L'entropie croisée est moins sensible aux outliers et ne les amplifie pas.

### 4.2 Précision (accuracy)
#### nous avons choisi  l'entropie croisée car:
#### a) Notre dataset est équilibré.
#### b) Elle est facile à comprendre et à interpréter.
                           -*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-