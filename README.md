# React To-Do List

This is a simple to-do list application built as a first React project using Vite.  
It focuses on learning React hooks, component structure, and basic state management.

## Features

- Add new tasks using an input field and "Add" button
- Delete tasks individually
- Move tasks **up** or **down** in the list
- Mark tasks as **Done**, with completed tasks styled differently
- Automatically group completed tasks at the bottom of the list
- Basic responsive layout and custom button colors (Add, Delete, Up, Down, Done)

## Tech Stack

- React (functional components + `useState`)
- Vite (project scaffolding and dev server)
- CSS for custom styling (no CSS framework)

## How It Works

- `ToDoList.jsx`:
  - Stores all tasks in a `tasks` array state: each task = `{ text, completed }`.
  - `newTask` state tracks the current input value.
  - `handleInputChange` updates `newTask` from the text input.
  - `addTask` adds a new task if the input is not empty and clears the input.
  - `deleteTask(index)` removes a task by index.
  - `moveTaskUp(index)` and `moveTaskDown(index)` reorder tasks in the array.
  - `toggleComplete(index)` toggles the `completed` flag and reorders so completed tasks appear at the bottom.

- The component renders:
  - A title (`To-Do-List`)
  - Input + Add button
  - An ordered list of tasks with buttons: **Delete**, **Up**, **Down**, **Done**

## Styling

- `.to-do-list` centers the app and sets the main layout.
- Buttons have different background colors for each action (Add, Delete, Move, Done).
- `.text.completed` applies a line-through and grey color for completed tasks.
- Flex layout in `li` ensures the text uses available width and buttons stay aligned.
- Long task text is wrapped using `word-break` / `overflow-wrap` to avoid horizontal overflow.

