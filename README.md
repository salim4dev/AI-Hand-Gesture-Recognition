# 🤖 Hand Gesture Recognition with MediaPipe & OpenCV

## 📘 Description

Ce projet détecte et reconnaît en temps réel plusieurs gestes de la main à partir d’une webcam, en utilisant **MediaPipe** et **OpenCV**.  
Les gestes sont détectés en analysant la géométrie des doigts et les angles entre les articulations.


### Gestes reconnus
- 👍 **Good (Pouce vers le haut)**  
- 👎 **Bad (Pouce vers le bas)**  
- 👉 **Point (Index pointé)**  
- ✊ **Run (Poing fermé)**  
- 💞 **Korean Love (Index et pouce rapprochés)**  
- ✋ **Open (Main ouverte)**  
- 🛑 **Stop (Deux mains ouvertes)**  

---

##  Fonctionnement

1. Extraction des 21 points clés (landmarks) sur chaque main via **MediaPipe Hands**.  
2. Calcul des **angles** entre phalanges pour déterminer si un doigt est droit ou plié.  
3. Calcul de la **distance pouce-index** pour détecter certains gestes spécifiques (ex. “Korean Love”).  
4. Utilisation de la **largeur de la paume** pour normaliser les mesures.  
5. Mécanisme de **stabilité** (`STABLE_FRAMES`) pour confirmer un geste seulement s’il reste stable sur plusieurs frames.

---

##  Dépendances

Installe les librairies nécessaires avec :

```bash
pip install opencv-python mediapipe numpy math
```

## Examples
![open](c1.png)
![good](c2.png)
![bad](c3.png)

## 📚 Crédits
Ce projet est une adaptation/modification du code original de [vir727](https://github.com/vir727/Gesture-Recogonition-App).

