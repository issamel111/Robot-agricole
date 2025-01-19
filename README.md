# Robot-agricole
Conception et développement d'un robot agricole automatisé pour le semis précis.

## Description
Ce projet consiste en la conception et la programmation d'un **robot agricole automatisé** contrôlé via Bluetooth. Le robot est conçu pour effectuer des tâches de semis avec une grande précision, en utilisant un capteur ultrason pour éviter les obstacles, et un module Bluetooth pour la commande à distance.

L'objectif du projet est de créer un robot durable, léger et autonome pour améliorer l'efficacité des semis dans l'agriculture.

---

## Fonctionnalités

### Commandes Bluetooth
- **Avancer** (`w`): Déplace le robot vers l'avant.
- **Reculer** (`s`): Déplace le robot vers l'arrière.
- **Tourner à gauche** (`a`): Tourne le robot vers la gauche.
- **Tourner à droite** (`d`): Tourne le robot vers la droite.
- **Arrêter** (`q`): Arrête le robot immédiatement.
- **Mode manuel** (`m`): Basculer en mode de contrôle manuel via Bluetooth.
- **Mode automatique** (`u`): Basculer en mode autonome où le robot évite les obstacles.
- **Vitesse élevée** (`+`): Augmenter la vitesse des moteurs.
- **Vitesse réduite** (`-`): Réduire la vitesse des moteurs.

### Comportement Automatique
Le robot passe en mode automatique où il :
- Utilise un **capteur ultrason** pour détecter des obstacles à moins de 20 cm.
- Arrête le robot et effectue un léger mouvement en arrière, puis un virage pour éviter l'obstacle.
- Le robot reprend ses déplacements lorsque l'environnement est dégagé.

---

## Matériel Nécessaire

- **Arduino Uno** ou une carte compatible.
- **Module Bluetooth HC-05** ou HC-06.
- **Moteurs DC** avec un **pont en H** (par exemple, L298N).
- **Capteur ultrason HC-SR04** pour la détection d'obstacles.
- **Capteur infrarouge** pour la détection d'obstacles supplémentaires.
- **Buzzer** pour les alertes sonores.
- **Câbles** et **alimentation** pour Arduino.

---

## Installation

### 1. Connecter les composants :
1. **Module Bluetooth HC-05** :
   - RX → broche 10 sur Arduino.
   - TX → broche 11 sur Arduino.

2. **Capteur ultrason HC-SR04** :
   - Trig → broche 2 sur Arduino.
   - Echo → broche 3 sur Arduino.

3. **Moteurs DC** :
   - Utilisez un pont en H (L298N) pour contrôler les moteurs.
   - Connectez les moteurs aux broches appropriées comme spécifié dans le code.

4. **Capteur infrarouge** :
   - Connectez le capteur à la broche 4 pour détecter des obstacles supplémentaires.

5. **Buzzer** :
   - Connectez le buzzer à la broche 12 pour les alertes sonores.

### 2. Télécharger et charger le code sur Arduino :
- Téléchargez le fichier **robot_bluetooth_control.ino** dans l’IDE Arduino et téléchargez-le sur votre carte Arduino.

### 3. Se connecter via Bluetooth :
- Connectez votre ordinateur ou smartphone au module Bluetooth **HC-05**.
- Utilisez une application de terminal Bluetooth (comme **Serial Bluetooth Terminal** sur Android) pour envoyer des commandes (w, s, a, d, q).

---

## Utilisation

1. **Démarrer le robot** :
   - Allumez le robot et ouvrez une connexion Bluetooth avec votre appareil.
   - Vous pouvez envoyer des commandes pour contrôler les moteurs manuellement (`w`, `s`, `a`, `d`) ou activer le mode automatique (`u`).

2. **Surveiller les diagnostics** :
   - Vous pouvez envoyer une commande pour obtenir un diagnostic complet du robot, incluant la distance mesurée par le capteur ultrason et l’état des capteurs infrarouge et de vitesse.

---

## Résultats et Performances

- **Réduction de la masse du robot** : Réduction de 15% par rapport aux prototypes initiaux pour une meilleure efficacité énergétique.
- **Précision** : Le robot atteint une précision de semis de **95%** en mode automatique.
- **Mode autonome efficace** : Le robot peut se déplacer de manière autonome en évitant les obstacles détectés par le capteur ultrason.

---

## Vidéo de Démonstration

🎥 **[Voir la vidéo de démonstration sur YouTube]((https://youtu.be/-gz4ryi8BaI))**

---

## Remerciements

Merci à **Polytechnique Montréal** pour le soutien et les ressources tout au long du projet.

