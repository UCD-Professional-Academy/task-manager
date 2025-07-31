# Task Management Application with Drag & Drop

## Description

This is a simple Task Management Application that allows the users to add, move, and remove tasks between different stages (To Do, In Progress, and Done). Tasks are saved in **localStorage** to persist data when the page is reloaded. 

## Features

- Add tasks with input field.
- Drag & Drop tasks between lists.
- Persistent data using `localStorage`.
- Clean and responsive design.

## How to Run

1. Clone or download the repo.
2. Open `index.html` in a web browser.
3. Add, drag, and drop tasks to manage your tasks.

## Technologies Used

- HTML
- CSS
- JavaScript

## Code example
```js
fetch("https://api.adviceslip.com/advice")
    .then((response) => response.json())
    .then((data) => {
        // Append quoteDisplay below task management area
        document
        .querySelector(".container")
        .insertBefore(quoteDisplay, document.querySelector(".task-lists"));
        const quoteText = `${data.slip.advice}`;
        quoteDisplay.textContent = `"${quoteText}"`;
    })
```

```html
<div
    class="task-list"
    id="todo"
    ondrop="drop(event)"
    ondragover="allowDrop(event)"
>
    <h2>To Do</h2>
    <ul id="todo-list"></ul>
</div>

```