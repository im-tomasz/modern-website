# 💻 Modern Website

## 🚀 Description

Ce projet est un exercice afin d'apprendre à maîtriser React, et notamment TailwindCSS pour le style. L’objectif est aussi d’appliquer de bonnes pratiques pour le responsive design.

---

## 🛠️ Stack technique

- **JavaScript** : utilisé avec React.
- **React** : pour construire l’interface utilisateur de façon dynamique et modulaire.
- **TailwindCSS** : pour le style, avec gestion du responsive.
- **CSS** : utilisé en complément.
- **HTML** : structure de base des composants React.

---

## 🗂️ Structure & parties importantes

- **src/App.jsx** : point d’entrée de l’application, organise la navigation et appelle les composants principaux.
- **src/components/** : contient tous les composants réutilisables du site.
- **src/styles/** : configuration de Tailwind et fichiers CSS additionnels.
- **public/** : fichiers statiques et point d’entrée HTML (`index.html`).

---

## 🎯 Compétences mises en application

- Utilisation de React pour décomposer l’interface en petits modules réutilisables.
- Mise en place de TailwindCSS pour un style cohérent.
- Adaptation de la mise en page pour le responsive design.
- Utilisation de props, state et gestion des events dans React.

---

## ✨ Exemples de code pertinents




---

**1. Responsive design avec Tailwind (src/components/Hero.jsx)**

```jsx name=src/components/Hero.jsx
<div className="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-3 sm:gap-4 mb-8 sm:mb-12 animate-in slide-in-from-bottom duration-700 delay-300">
  <button className="group w-full sm:w-auto px-6 sm:px-8 py-3 sm:py-4 bg-gradient-to-b from-blue-600 to-blue-400 rounded-lg font-semibold text-sm sm:-text-base transition-all duration-300 hover:scale-102 flex items-center justify-center space-x-2">
    <span>Start Coding Free</span>
    <ArrowRight className="w-4 h-4 sm:w-5 sm:h-5 group-hover:translate-x-1 transition-transform duration-100 "/>
  </button>

  <button className="group w-full sm:w-auto px-6 sm:px-8 py-3 sm:py-4 bg-white/5 backdrop-blur-sm border border-white/10 rounded-lg font-semibold text-sm sm:-text-base transition-all duration-300 hover:bg-white/10 flex items-center justify-center space-x-2">
    <div className="p-2 bg-white/10 rounded-full group-hover:bg-white/20 duration-300 transition-colors">
      <Play className="w-4 h-4 sm:w-5 sm:h-5 fill-white"/>
    </div>
    <span>Watch Demo</span>
  </button>
</div>

```
> style responsive et réactif grâce à TailwindCSS.

---

**2. Carte flottante adaptative (src/components/Hero.jsx)**

```jsx name=src/components/Hero.jsx
const [activeTab, setActiveTab] = useState("App.jsx")


<button
  onClick={() => setActiveTab("App.jsx")}
  >App.jsx
</button>

<button
  onClick={() => setActiveTab("Hero.jsx")}
  >Hero.jsx
</button>

<button
  onClick={() => setActiveTab("Navbar.jsx")}
  >Navbar.jsx
</button>


<div className={`${floatingCards[activeTab].bgColor}`}>
  <div className="flex items-center">
    <div className={`${currentFloatingCard.iconColor}`}>
      {currentFloatingCard.icon}
    </div>
    <span className={`${currentFloatingCard.textColor}`}>
      {currentFloatingCard.title}
    </span>
  </div>
  <div className={`${currentFloatingCard.contentColor}`}>
    {currentFloatingCard.content}
  </div>
</div>
```
> cette carte affichant du contenu est rendue réactive au clic sur différents boutons (que j'ai simplifiés ici pour faciliter la lecture).

---

**3. Contenu des cartes stocké dans un fichier (src/components/Hero.jsx)**

```jsx name=src/data/CodeExamples.js

export const floatingCards = {
    "App.jsx": {
        bgColor : "bg-blue-500/20",
        iconColor: "text-blue-400",
        textColor: "text-blue-200",
        contentColor: "text-blue-300",
        icon: "AI",
        title: "Smart Completion",
        content: "AI-powered code suggestions in real time" 
    },
    "Hero.jsx": {
        bgColor : "bg-purple-500/20",
        iconColor: "text-purple-400",
        textColor: "text-purple-200",
        contentColor: "text-purple-300",
        icon: "⚡",
        title: "Auto Animation",
        content: "Dynamic typing effects generated automatically" 
    },
    "Navbar.jsx": {
        bgColor : "bg-emerald-500/20",
        iconColor: "text-emerald-400",
        textColor: "text-emerald-200",
        contentColor: "text-emerald-300",
        icon: "🔍",
        title: "Smart search",
        content: "Intelligent code search accross your project" 
    }

}
```
> ce contenu délocalisé dans un fichier permet d'optimiser la maintenabilité du code, ainsi que sa lecture.
