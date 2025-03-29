# 🎨 Styling in React — A Quick Overview

Welcome to the **Styling in React** guide!  
In React, styling is done a little differently than in traditional HTML/CSS projects. There is no single "correct" way to style components — developers have a variety of tools and techniques to choose from, and the best approach often depends on the project requirements or existing team conventions.

This repository provides an overview of the most popular methods used to style React components, with explanations and examples.

---

## 📄 Overview

React gives developers flexibility when it comes to styling. There are several well-known approaches, each with its pros and cons.  
In a real-world job setting, the styling approach is often predetermined by the existing codebase or team preference. However, as a React developer, it’s essential to be familiar with multiple options.

This repo introduces the following common styling methods:

- Imported CSS Stylesheets
- Inline Styling
- Styled Components
- CSS Modules
- SASS

---

## Styling Options

### 1. **Imported CSS Stylesheets**
The classic way of styling — writing styles in a `.css` file and importing them into your component.

**Example:**
```jsx
import './App.css';

function App() {
  return <h1 className="title">Hello World</h1>;
}
```

**Use case:**  
Quick, simple projects or when migrating older CSS.

---

### 2. **Inline Styling**
You can use the `style` prop to apply styles directly to elements.

**Example:**
```jsx
function App() {
  return <h1 style={{ color: 'blue', fontSize: '24px' }}>Hello World</h1>;
}
```

**Use case:**  
Dynamic styling based on props or state; one-off styles.

---

### 3. **Styled Components**
Styled Components is a popular **CSS-in-JS** library that allows you to write actual CSS inside your JavaScript.

**Installation:**
```bash
npm install styled-components
```

**Example:**
```jsx
import styled from 'styled-components';

const Title = styled.h1`
  color: blue;
  font-size: 24px;
`;

function App() {
  return <Title>Hello World</Title>;
}
```

**Use case:**  
Component-scoped styling, dynamic theming, or when building modern, scalable UIs.

---

### 4. **CSS Modules**
CSS Modules allow you to write CSS that is **scoped locally** to a specific component, preventing class name collisions in large applications.

**Example:**
```jsx
import styles from './App.module.css';

function App() {
  return <h1 className={styles.title}>Hello World</h1>;
}
```

**Use case:**  
When working on medium to large-scale applications and want to avoid global CSS conflicts.

---

### 5. **SASS / SCSS**
**SASS** is a powerful CSS preprocessor that extends CSS with features like variables, nested rules, mixins, and more.

**Installation:**
```bash
npm install sass
```

**Example:**
Create a `.scss` file:
```scss
$title-color: blue;

.title {
  color: $title-color;
  font-size: 24px;
}
```

Import and use in your component:
```jsx
import './App.scss';

function App() {
  return <h1 className="title">Hello World</h1>;
}
```

**Use case:**  
When you want advanced CSS features and better structure for large and complex projects.

---

## Summary

| Method               | Pros                                         | Cons                                      |
|---------------------|----------------------------------------------|-------------------------------------------|
| Imported CSS        | Simple, easy to start                        | Global scope, possible class collisions   |
| Inline Styling      | Quick, dynamic                               | No pseudo-classes, lacks full CSS power   |
| Styled Components   | Scoped, dynamic, supports themes             | Adds dependency, slightly larger bundle   |
| CSS Modules        | Local scoping, no class name conflicts       | Slightly more setup                      |
| SASS / SCSS         | Powerful, advanced CSS features              | Needs compilation, learning curve         |

---

## 🧩 In a Real-World Project

In professional environments, you will often use a combination of these methods. Many large-scale apps use **CSS Modules** or **Styled Components** alongside regular CSS for global styles.

---
