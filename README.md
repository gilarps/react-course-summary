# React Udemy Course Summary

React - The Complete Guide 2025 (incl. Next.js, Redux)  
Dive in and learn React.js from scratch! Learn React, Hooks, Redux, React Router, Next.js, Best Practices and way more!  
https://www.udemy.com/course/react-the-complete-guide-incl-redux

## Table of Contents

1. [Getting Started](#getting-started)
2. [JavaScript Refresher](#javascript-refresher)
3. [React Essentials - Components, JSX, Props, State & More](#components)

---

## Getting Started

### What Is React?

**JavaScript library** for web and native _UI_

### Why Not Just JavaScript (Vanilla)?

- Cumbersome (complex, large, inefficient)
- Error-prone potential (for complex code)
- Huge pain

### Why Use React?

- Extremely **popular**
- **Strong ecosystem** -> Rich libraries, tools, and community support (e.g., Redux, React Router, Next.js)
- From building complex, interactive UI to **breeze**
- **Declarative** UI programming -> Define the goal, not steps -> Describe what the UI should look like, and React handles updates efficiently
- **Component-based** –> UIs are built from small, reusable pieces, making code easier to manage and scale
- **Virtual DOM** –> React updates the UI quickly and efficiently by minimizing direct DOM manipulations
- **One-way data flow** –> Predictable data flow makes debugging and understanding state changes easier
- **Reusable logic** via hooks –> Logic like fetching data or handling state can be reused cleanly across components
- **Cross-platform support** –> You can use **React Native** to build mobile apps using the same concepts

### Editing First React App

Adding new tab (React vs JS) https://codesandbox.io/p/devbox/first-react-app-forked-kw5gjr?workspaceId=ws_MMuSc8CCLjTZ5cZf5rfU4B

### Course Resources

https://github.com/academind/react-complete-guide-course-resources?tab=readme-ov-file

### About This Course

**Modular Course**. Splitted into these parts:

- **Getting Started**
- **JavaScript Refresher** -> If needed
- **React Essentials** -> Must learn
- **Deep dive & advanced concepts** -> Can jump to other section that interesting for you

### Two Ways (Path) of Taking This Course

- Standard Path -> **Recommended**
  - Complete the course by lecture and **section by section**
  - Learn **step by step**
- Summary Path -> If you got **limited time**
  - Complete the **summary section** (https://www.udemy.com/course/react-the-complete-guide-incl-redux/learn/lecture/35734460#overview)
  - Get a good **overview** of basic and advanced React concepts
  - Great **refresher** after finishing the course

### Join Academind Community on Discord

https://academind.com/community/

### Creating React Projects

🧪 Two Ways to Set Up a React Project:

- Quick Start with **CodeSandbox** (react.new):
  - Visit **react.new** to instantly create a new React project in your browser using CodeSandbox.
  - **No local installation needed** — ideal for beginners or if you can't install software (e.g., on a company computer).
  - Used throughout the course for hands-on practice.
  - CodeSandbox includes a file editor and live preview in one browser window.
- **Local** React Project Setup:
  - Recommended for **more control, performance, and use of tools** like Visual Studio Code.
  - Requires **Node.js** installed from nodejs.org.
  - Two common tools to set up a project:
    - **Vite** (recommended, modern, fast)
    - **Create React App** (older, still common)
  - Example setup with **Vite**:
    - Run: **npm create vite@latest project-name**
    - Choose "React"
    - Install dependencies with: npm install
    - Start dev server with: npm run dev
  - Example setup with Create React App: - Run: **npx create-react-app project-name**
    > This setup provides a local development server that auto-updates the preview when you save changes.

### Why We Need Tools Like Vite or CodeSandbox for React

You can't just use a plain HTML and JS file to write React code because:

- React uses **JSX** – a **special syntax** that looks like HTML in JavaScript.
- Browsers don't understand JSX, so the code **must be transformed** first.
- Build tools like **Vite** are needed to:
  - **Convert JSX** into browser-compatible JavaScript.
  - **Optimize** the code (e.g., minify, remove whitespace, shorten names) for better performance.
- Tools like CodeSandbox and Vite **automate** all of this:
  - They make **setup easy**.
  - CodeSandbox needs **no installation**.
  - Vite gives you **fast local development**.

## JavaScript Refresher

### Introduction

- It's **optional**. you can skip it or return later if needed.
- Recommended if:
  - You haven't used JavaScript for a while
  - You have limited JavaScript experience.
- Not suitable for complete JavaScript beginners — if you’ve never used JavaScript before, learn the basics first.
- What this section covers:
  - **Core JavaScript concepts** needed for React.
  - **Modern JavaScript features** (like let, const, arrow functions, etc.).
  - **Syntax and rules essential** for writing React code.

### Starting Project

https://codesandbox.io/p/sandbox/javascript-refresher-start-rytt3j?file=%2Findex.html

### Adding JavaScript & How React Projects Differ

- JavaScript runs in many environments:
  - Originally built for the browser.
  - Now also runs outside the browser (e.g., with Node.js, Deno, React Native).
- How JavaScript is added to a website:
  - With the <script> tag in HTML.
    - Option 1: Write JavaScript inline between <script> tags (not recommended for large projects).
    - Option 2: Link to external .js files (recommended for real-world use).
- Script tag options:
  - defer: delays script execution until HTML is fully parsed.
  - type="module": treats the file as an ES module, enabling use of import/export syntax between files.
- JavaScript modules:
  - Allow splitting code across multiple files.
  - Useful for reusability and maintainability.
- In React projects:
  - You don’t manually add <script> tags.
  - A build process (like Vite or Webpack) automatically injects necessary scripts into the HTML.

### React Projects Use a Build Process

- **No Script Tags in HTML**
  - React projects don’t include <script> tags manually in index.html.
- **Build Process Handles Injection**
  - Tools like **React Scripts** automatically inject script tags during build or development.
- **JSX Requires Transformation**
  - JSX (HTML-like syntax in JavaScript) isn’t valid JavaScript and must be compiled.
- **Build Process Transforms JSX**
  - The build tool converts JSX into browser-compatible JavaScript.
- **Code Optimization**
  - The build also minifies and optimizes the code for better performance.
- **Development Server**
  - A dev server (like in CodeSandbox or Create React App) watches your code, builds it, and serves it with injected scripts.
- **Node.js is Required**
  - Node.js powers these tools and is needed to run and build React projects locally.
- **Vanilla JS Projects Can’t Use JSX**
  - Without a build process, JSX won’t work in plain JavaScript projects.

### "import" & "export"

- Named Exports
  - Export multiple items with specific names:
    ```js
    // util.js
    export const apiKey = "ABC123";
    export const abc = "Some Value";
    ```
