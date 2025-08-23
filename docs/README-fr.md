# Podcast Generator
[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-FFDD00?style=flat&logo=buy-me-a-coffee&logoColor=000000)](https://www.buymeacoffee.com/laurentftech)

Si vous appréciez ce projet et souhaitez soutenir mon travail, vous pouvez [m’offrir un café](https://www.buymeacoffee.com/laurentftech) ☕. Merci pour votre soutien !

---

## 📖 Présentation

Une application légère en Python qui vous permet de générer des podcasts multi-intervenants à partir de n’importe quel script grâce à la nouvelle API ElevenLabs v3 — simple, rapide et efficace.

### 🔑 Pour commencer
Obtenez votre clé API gratuite sur [ElevenLabs](https://try.elevenlabs.io/zobct2wsp98z) (ou Google Gemini).
Ajoutez-la de manière sécurisée dans l’application.
Commencez à créer vos podcasts en quelques minutes.

💡 Remarque : Je suis **affilié** à ElevenLabs. L’utilisation de ce lien peut me rapporter une commission, sans coût supplémentaire pour vous. ElevenLabs propose également un **niveau gratuit** avec des limites mensuelles de caractères pour les voix premium.

![Capture d'écran de l'application](../podcast_creator_screenshot.png)

---

## ✨ Fonctionnalités

- **Génération audio** : Créez des podcasts multi-locuteurs avec des voix de haute qualité grâce à l’API Google Gemini.
- **Interface intuitive** : Interface graphique claire et simple à utiliser.
- **Formats flexibles** : Export en **MP3** (par défaut) ou **WAV**.
- **Personnalisation** : Sauvegarde des voix et paramètres pour chaque locuteur.
- **Lecture intégrée** : Écoutez et arrêtez vos créations directement depuis l’application (**FFmpeg requis**).
- **Stockage sécurisé de la clé API** : Votre clé API Google Gemini est demandée une seule fois et enregistrée de manière sécurisée dans le trousseau du système (`keyring`).
- **Version automatique** : Synchronisation de la version de l’application avec les tags Git du projet.

---

## 🌍 Support multilingue

Grâce à l’API Google Gemini, **Podcast Generator** permet :

- De créer des podcasts multilingues avec des voix distinctes.
- De produire du contenu pour un public international.
- De faciliter l’apprentissage des langues avec des dialogues réalistes.
- D’améliorer l’accessibilité grâce à l’audio.

---

## 💡 Exemples d’utilisation

### Script simple
```txt
John: Bonjour à tous, bienvenue dans ce nouvel épisode.
Samantha: Aujourd'hui, nous allons explorer les bases de l’intelligence artificielle.
John: Restez avec nous pour en savoir plus !
Samantha: N'oubliez pas de vous abonner.
```

⚠️ Important : Les noms des locuteurs dans votre script (ex: John:, Samantha:) doivent correspondre exactement aux noms définis dans la fenêtre "Réglages des voix". L'application n'effectue aucune vérification, et une non-concordance entraînera une erreur de génération ou une mauvaise attribution des voix.

### Script multilingue
```txt
John (fr): Bonjour à tous, bienvenue dans ce nouvel épisode.
Samantha (en): Hello everyone, welcome to this new episode.
John (es): Hola a todos, bienvenidos a este nuevo episodio.
```

---

## 📦 Installation

### 1. Dépendance externe : FFmpeg (obligatoire)

Pour la conversion et la lecture audio, **FFmpeg** doit être installé sur votre système.

#### **macOS**
Installer via [Homebrew](https://brew.sh/) :
```bash
brew install ffmpeg
```

#### **Linux**
Installer via le gestionnaire de paquets :
```bash
sudo apt install ffmpeg        # Debian/Ubuntu
sudo dnf install ffmpeg        # Fedora
sudo pacman -S ffmpeg          # Arch
```

#### **Windows (guide détaillé)**

1. **Télécharger FFmpeg**  
   Rendez-vous sur la page officielle des builds :  
   👉 [https://www.gyan.dev/ffmpeg/builds/](https://www.gyan.dev/ffmpeg/builds/)  
   Téléchargez l’archive **"release full"** (ex. `ffmpeg-release-full.7z` ou `.zip`).

2. **Extraire l’archive**  
   - Clic droit → **Extraire tout…**  
   - Vous obtenez un dossier du type `ffmpeg-2025-xx-xx-full_build`.

3. **Déplacer le dossier**  
   - Déplacez le dossier `ffmpeg` dans un emplacement permanent, par exemple :  
     `C:\ffmpeg`

4. **Ajouter FFmpeg au PATH**  
   - Appuyez sur **Windows + R**, tapez :
     ```
     sysdm.cpl
     ```
     puis **Entrée**.
   - Onglet **Avancé** → **Variables d’environnement**.
   - Dans **Variables système**, sélectionnez **Path** → **Modifier**.
   - Cliquez sur **Nouveau** et ajoutez :
     ```
     C:\ffmpeg\bin
     ```
   - Validez avec **OK**.

5. **Vérifier l’installation**  
   - Ouvrez **Invite de commandes** et tapez :
     ```
     ffmpeg -version
     ```
     Vous devez voir la version installée.

---

### 2. Installation de l’application

1. Rendez-vous sur la page **Releases** du projet.  
2. Téléchargez l’archive adaptée à votre système :
    - **macOS/Linux** : `.tar.gz`
    - **Windows** : `.zip` ou `.tar.gz`
3. **Extraire** l’archive :
    - macOS/Linux : double-clic ou `tar -xzf fichier.tar.gz`
    - Windows : clic droit → **Extraire tout…**
4. **Placer** le dossier où vous le souhaitez.

---

### 💡 Note pour macOS

Au premier lancement, macOS affichera un avertissement de sécurité car l’application n’est pas signée.

1. Double-cliquez sur l’application (un message bloquera l’ouverture).  
2. Ouvrez **Réglages Système → Confidentialité et sécurité**.  
3. Cliquez sur **Ouvrir quand même**.  
4. Confirmez.

---

### 💡 Note pour Windows (Windows 10 / 11)

Lors du premier lancement, **Windows SmartScreen** peut bloquer l’application.

1. Message *"Windows a protégé votre ordinateur"*.
2. Cliquez sur **Informations complémentaires**.
3. Cliquez sur **Exécuter quand même**.

Une fois validé, Windows ne vous le demandera plus.

---

### Premier lancement : clé API

Lors du premier démarrage, l’application vous demandera votre clé **API ElevenLabs** (et éventuellement votre clé **API Google Gemini**).  
Elle sera stockée de manière sécurisée.

---

## 👨‍💻 Pour les développeurs

Voir **DEVELOPERS-fr.md** pour exécuter le code ou contribuer au projet.

---

## 📜 Licence

Ce projet est sous licence MIT — voir le fichier [LICENSE](../LICENSE) pour plus de détails.

---

## 🤝 Contributions

Les contributions sont les bienvenues ! Consultez le fichier [DEVELOPERS-fr.md](DEVELOPERS-fr.md) pour les règles de contribution.

---

Merci d’utiliser **Podcast Generator** ! ☕
