---
title: "Installation"
description: "Ce qu'il vous faut, l'avertissement du premier lancement, et comment arrivent les mises à jour."
section: start
---

## Ce qu'il vous faut

Un ordinateur capable d'exécuter des modèles de langage [quantifiés](doc:glossary#quantization). Une carte graphique est facultative. Elle rend en général les réponses plus rapides.

- Windows 10 ou 11, 64 bits.
- Mémoire : au moins 4 Go (Qwen 3.5 2B). Recommandé : 16 Go (Qwen 3.5 9B).
- Espace disque libre égal à 1,5 fois la taille du modèle : environ 0,8 Go pour le plus petit modèle, 9 Go pour Qwen 3.5 9B.
- Carte graphique : facultative. Recommandé : 8 Go de mémoire vidéo avec au moins 10 Go de mémoire système.

## Installer

Téléchargez le programme d'installation ou le paquet pour votre système d'exploitation sur [la page de téléchargement](site:download) ou sur [la page des versions GitHub](https://github.com/Lucki74/draggy/releases/latest) :

> [!PLATFORMS]
> - Windows: Lancez le `.exe` d'installation NSIS. Il s'installe uniquement pour votre compte utilisateur, dans `%LOCALAPPDATA%\Programs\Draggy`. SmartScreen peut bloquer le programme d'installation, car la build n'est pas encore signée avec un certificat d'éditeur. Sélectionnez Informations complémentaires, puis Exécuter quand même.
> - macOS: Téléchargez le zip pour Apple silicon, décompressez-le, faites un clic droit sur Draggy.app et sélectionnez Ouvrir la première fois.
> - Linux: Installez le paquet .deb avec votre gestionnaire de paquets ou dpkg, ou le paquet .rpm avec rpm ou dnf.

Chaque version contient un fichier `SHA256SUMS.txt`, si vous préférez vérifier plutôt que faire confiance.

## Le premier lancement

La configuration choisit un modèle adapté à votre matériel et vous demande de le confirmer. Le téléchargement démarre quand vous passez l'étape du modèle, depuis Hugging Face. Le premier modèle pèse entre environ 0,5 Go et 240 Go, selon le matériel.

Quand vous envoyez votre premier message, Draggy charge le modèle en mémoire. Lors des lancements ultérieurs, le modèle reste sur le disque jusqu'à l'envoi d'une invite, donc l'ouverture de l'application est instantanée.

## Mises à jour {#updates}

Draggy vérifie les mises à jour à chaque lancement, puis toutes les six heures. Sous Windows, une mise à jour trouvée se télécharge en arrière-plan. Une fois prête, un avis **Mise à jour prête** propose **Installer maintenant** ou **Plus tard**. Installer maintenant l'installe discrètement et redémarre Draggy. Il n'existe pas de réglage des mises à jour, et les mises à jour ne s'exécutent jamais depuis une build de développement.

Sous macOS, Draggy télécharge lui-même le zip, vérifie son SHA-256 et remplace le bundle de l'application après la fermeture. Si le dossier n'est pas accessible en écriture, la page de la version s'ouvre à la place. Sous Linux, Draggy télécharge et vérifie le paquet en arrière-plan, et l'avis de redémarrage installe le .deb ou le .rpm avec pkexec. Flatpak ne fait rien, et sans pkexec Draggy ouvre la page de la version. Lancé depuis les sources, les mises à jour sont désactivées.

Pour supprimer Draggy, voyez [Désinstaller](doc:privacy#désinstaller) sur la page confidentialité.
