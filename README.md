# Monster Hunter Ultimate Quiz - Application Windows

![Monster Hunter Ultimate Quiz](https://raw.githubusercontent.com/wyverndescaverne-ship-it/mh-quiz-app-full/full-app/public/images/logo.png)

> 🎮 **Une application Windows immersive** inspirée de l'univers **Monster Hunter**, avec **200 questions FR/EN**, sons, animations et build en `.exe`.

---

## 📌 **Fonctionnalités**

✅ **200 questions vérifiées** (FR/EN) avec sources officielles et explications détaillées
✅ **Système de quiz interactif** : Timer, score, statistiques, succès à débloquer
✅ **Multilingue** : Français / Anglais (bouton de changement instantané)
✅ **Audio immersif** : Musique de fond, effets sonores et voix
✅ **Design original** : Inspiré de Monster Hunter (métal, cuir, bois, feu, parchemins)
✅ **Build en `.exe`** : Pour une distribution facile sous Windows
✅ **Responsive** : Compatible PC, tablette et téléphone
✅ **Sauvegarde locale** : Mémorisation des préférences et statistiques
✅ **Validation automatique** des questions via script dédié

---

## 📂 **Structure du projet**

```
mh-quiz-app-full/
├── src/                    # Code source (React + TypeScript + Tailwind)
│   ├── components/         # Composants réutilisables (Navbar, Footer, QuizCard, etc.)
│   ├── pages/              # Pages principales (Home, Quiz, Results, Settings, Achievements)
│   ├── data/               # Données structurées (200 questions FR/EN, catégories, succès)
│   │   ├── questions.json  # 200 questions vérifiées avec sources
│   │   ├── categories.json # Catégories de questions
│   │   ├── achievements.json # Succès à débloquer
│   │   └── translations.json # Traductions FR/EN
│   ├── hooks/              # Hooks personnalisés (useQuiz, useAudio, etc.)
│   ├── services/           # Services (AudioService, StorageService)
│   ├── utils/              # Utilitaires (validation, calculs de score, etc.)
│   ├── types/              # Types TypeScript
│   ├── i18n/               # Internationalisation (FR/EN)
│   └── styles/             # Styles globaux et thèmes
│
├── public/                 # Assets statiques
│   ├── audio/              # Musique de fond et effets sonores
│   ├── images/             # Logos, icônes et images originales
│   └── favicon.ico         # Icône de l'application
│
├── electron/               # Configuration pour le build .exe (Electron)
├── scripts/                # Scripts utilitaires
│   └── validateQuestions.ts # Script de validation des questions
│
├── package.json            # Dépendances et scripts (npm run dev, build, package)
├── tsconfig.json           # Configuration TypeScript
├── vite.config.ts          # Configuration Vite (build)
├── electron-builder.json   # Configuration Electron Builder
└── README.md               # Ce fichier
```

---

## 🚀 **Installation & Lancement**

### **1. Prérequis**
- **Node.js** (version LTS) : [Télécharger Node.js](https://nodejs.org/fr/download/)
  → **Cochez "Add to PATH" pendant l'installation !**

### **2. Cloner le dépôt**
```bash
git clone https://github.com/wyverndescaverne-ship-it/mh-quiz-app-full.git
cd mh-quiz-app-full
```

### **3. Installer les dépendances**
```bash
npm install
```

### **4. Lancer en mode développement**
```bash
npm run dev
```
→ L'application s'ouvre **automatiquement dans ton navigateur** (http://localhost:5173).

### **5. Générer le `.exe` (pour distribuer)**
```bash
npm run build
npm run package
```
- Le `.exe` sera généré dans :
  `dist/win-unpacked/MonsterHunterUltimateQuiz.exe`
- **Double-clique** sur le fichier pour lancer l'application.

---

## 📖 **Comment ajouter/modifier les questions ?**

1. **Édite le fichier** `src/data/questions.json` :
   ```json
   {
     "id": 1,
     "question": "Quel est le premier Monster Hunter sorti ?",
     "options": ["Monster Hunter", "Monster Hunter G", "Monster Hunter Freedom", "Monster Hunter World"],
     "correctAnswer": 0,
     "explanation": "Le premier jeu de la série est sorti en 2004 sur PlayStation 2.",
     "game": "Monster Hunter",
     "category": "Histoire",
     "source": "Wikipedia",
     "language": "fr"
   }
   ```

2. **Valide les questions** avec le script :
   ```bash
   npx tsx scripts/validateQuestions.ts
   ```

3. **Relance l'application** pour voir les changements.

---

## 🎨 **Direction Artistique**

- **Inspiration** : Monster Hunter, guildes de chasseurs, nature sauvage, équipement de chasseur.
- **Éléments visuels** :
  - Textures bois et métal
  - Parchemins et bordures tribales
  - Animations fluides (particules, fumée, effets lumineux)
  - Palette de couleurs : Or, marron, vert forêt, rouge sang
- **Assets originaux** : Aucune violation de copyright (créés pour le projet).

---

## 🔊 **Assets Audio**

- **Musique de fond** : Ambiance immersive (forêt, combat).
- **Effets sonores** : Réponses, succès, transitions.
- **Voix** (optionnel) : Instructions et feedback.

---

## 📊 **Statistiques & Succès**

- **Score** : Calculé en temps réel (bonus pour les combos).
- **Succès** : 20 succès à débloquer (ex: "Répondre correctement à 10 questions d'affilée").
- **Historique** : Sauvegarde des sessions.

---

## 🛠 **Personnalisation**

- **Changer les couleurs** : Édite `src/styles/theme.css`.
- **Ajouter des sons** : Place-les dans `public/audio/` et référence-les dans `src/services/AudioService.ts`.
- **Modifier les traductions** : Édite `src/data/translations.json`.

---

## 📜 **Licence**

Ce projet est **open-source** sous licence **MIT**. Vous êtes libre de l'utiliser, le modifier et le distribuer.

---

## 🤝 **Contribuer**

Les contributions sont les bienvenues ! Ouvrez une **issue** ou soumettez une **pull request**.

---

## 📧 **Contact**

Pour toute question ou feedback :
- **GitHub** : [wyverndescaverne-ship-it](https://github.com/wyverndescaverne-ship-it)
- **Email** : (à ajouter si nécessaire)

---

## 🎮 **Capture d'écran**

![Capture d'écran de l'application](https://raw.githubusercontent.com/wyverndescaverne-ship-it/mh-quiz-app-full/full-app/public/images/screenshot.png)

---

**🎉 Bonne chasse, et profitez bien de votre Monster Hunter Ultimate Quiz !** 🔥
