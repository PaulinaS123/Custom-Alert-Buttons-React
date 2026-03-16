
# Custom Alert Buttons in React

## Student: Victoria Salomon

## Overview

This project is a React application created using Vite.
The application demonstrates how to create reusable components, pass data using props, use the special children prop, and handle events using onClick.

The app includes a Toolbar component that contains multiple AlertButton components.
Each button displays a different alert message when clicked.

This assignment was created for learning React component structure, props, children, and event handling.

---

## Objective

* Create reusable React components
* Pass data using props
* Use the children prop
* Handle events with onClick
* Display dynamic alert messages
* Organize components into multiple files

---

## Project Structure

src/

* App.jsx
* Toolbar.jsx
* AlertButton.jsx
* App.css
* index.css
* main.jsx

---

## Component Explanation

### AlertButton Component

This component receives two props:

* message → text to show in alert
* children → text inside the button

When the button is clicked, the alert() function runs and shows the message.

Example:

```jsx
function AlertButton({ message, children }) {
  return (
    <button onClick={() => alert(message)}>
      {children}
    </button>
  );
}
```

### Toolbar Component

The Toolbar component contains multiple AlertButton components.

Each button has a different message and text.

Example:

```jsx
function Toolbar() {
  return (
    <div className="toolbar">

      <AlertButton message="Playing music">
        Play
      </AlertButton>

      <AlertButton message="Uploading file">
        Upload
      </AlertButton>

      <AlertButton message="Deleting item">
        Delete
      </AlertButton>

    </div>
  );
}
```
### App Component

The App component displays the title and the Toolbar.

```jsx
import Toolbar from "./Toolbar";

function App() {
  return (
    <>
      <h1>Custom Alert Buttons</h1>
      <Toolbar />
    </>
  );
}
```
## How to Run the Project

1. Open terminal in project folder

2. Install dependencies

```
npm install
```

3. Start development server

```
npm run dev
```

4. Open browser

```
http://localhost:5173
```

5. Click each button to see alerts

---

## Test Cases

### Normal Test Cases

1. Click Play button
   Expected: alert shows "Playing music"

2. Click Upload button
   Expected: alert shows "Uploading file"

3. Click Delete button
   Expected: alert shows "Deleting item"

### Edge Test Cases

1. Button with empty message
   Expected: alert shows empty text

2. Button with long message
   Expected: alert still works

3. Button clicked multiple times
   Expected: alert shows every time
