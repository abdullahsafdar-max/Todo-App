# Todo App (Task Management System)
#### A simple, browser-based Todo application built using HTML, CSS, and JavaScript. This project demonstrates core front-end development concepts such as DOM manipulation, event handling, and state management using arrays.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Data Structure](#data-structure)
- [Application Workflow](#application-workflow)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)
- [Author](#author)

## Project Overview

This project is a simple **Todo List** application that allows users to add, complete, and delete tasks.

The application was developed as a learning exercise to strengthen fundamental JavaScript concepts and front-end development skills. Throughout this project, the following concepts were practiced:

- DOM manipulation
- Event listeners
- Arrays and objects
- Functions
- Rendering dynamic content based on the application state

## Features

| Feature | Description |
|---------|-------------|
| **Add Task** | Users can enter a task and click **Add** to add it to the list. |
| **Input Validation** | Prevents empty tasks from being added and displays an alert message if the input is empty. |
| **Mark as Complete** | Users can mark a task as complete by selecting the checkbox. Completed tasks are displayed with a strikethrough. |
| **Delete Task** | Removes a task permanently from the list |
| **Dynamic Rendering** | The task list is automatically updated whenever a task is added, deleted, or completed. |
| **Empty State Message** | Displays **"No tasks yet. Add one above!"** when there are no tasks in the list. |

## Technologies Used

| Technology | Purpose |
|------------|---------|
| **HTML5** | Creates the structure of the webpage, including the input box, button, and task list. |
| **CSS3** | Styles the webpage and makes it clean, organized, and responsive. |
| **JavaScript** | Adds functionality, manages tasks, and updates the page based on user actions. |

## Project Structure

```text
todo-app/
│
├── index.html        # Creates the layout of the Todo App
├── style.css         # Adds colors, spacing, and responsive design
└── newscript.js      # Adds functionality like adding, completing, and deleting tasks
```
## Data Structure

The Todo App stores all tasks in a JavaScript array. Each task is saved as an object that contains information about the task, such as its unique ID, the task text, and whether it has been completed.

### Task Object

Each task follows this structure:

| Property | Type | Description |
|----------|------|-------------|
| **id** | Number | A unique ID for each task. |
| **text** | String | The task entered by the user. |
| **completed** | Boolean | Shows whether the task is completed (`true`) or not (`false`). |

```javascript
{
  id: Number,
  text: String,
  completed: Boolean
}
```

### Example

```javascript
let tasks = [
  { id: 1, text: "Learn JavaScript", completed: false },
  { id: 2, text: "Build Todo App", completed: true },
  { id: 3, text: "Read a Book", completed: false }
];
```
## Application Workflow

The application works by taking the user's input, updating the task list, and then refreshing the page content to show the latest changes.

### Workflow

```text
Page Loads
    │
    ▼
tasks = [] (empty array)
    │
    ▼
renderTasks() runs and shows "No tasks yet" message
    │
    ▼
User enters a task and clicks "Add"
    │
    ▼
Input is checked to make sure it is not empty
    │
    ▼
A new task object is created
    │
    ▼
The task is added to the tasks array
    │
    ▼
renderTasks() runs again and updates the task list
    │
    ├──► User checks the checkbox
    │         ▼
    │   Task is marked as completed
    │         ▼
    │   renderTasks() updates the list
    │
    └──► User clicks Delete
              ▼
        Task is removed from the array
              ▼
        renderTasks() updates the list
```

### Step-by-Step Process

| Step | What Happens |
|------|--------------|
| **1** | The page loads and an empty `tasks` array is created. |
| **2** | `renderTasks()` runs and displays **"No tasks yet. Add one above!"** because there are no tasks. |
| **3** | The user enters a task in the input box. |
| **4** | When the **Add** button is clicked, the app checks that the input is not empty. |
| **5** | A new task object is created with an `id`, `text`, and `completed` value. |
| **6** | The new task is added to the `tasks` array. |
| **7** | `renderTasks()` runs again and displays the updated task list. |
| **8** | If the user checks the checkbox, the task is marked as completed and the list is updated. |
| **9** | If the user clicks **Delete**, the task is removed from the array and the list is updated. |

### Key Idea

The `tasks` array stores all the task data. Whenever a task is added, completed, or deleted, the array is updated first. After that, `renderTasks()` refreshes the task list so the page always shows the latest data.
### Why This Structure?

- An **array** is used to store all tasks in one place.
- An **object** is used to keep the information for each task together.
- A unique **id** helps identify each task when it needs to be completed or deleted.
- The **completed** property keeps track of whether a task is finished.

## How to Run

Follow these steps to run the application on your local machine:

1. Download the project files or clone the repository.

2. Make sure the following files are in the same folder:
   - `index.html`
   - `style.css`
   - `newscript.js`

   The HTML file links to the CSS and JavaScript files by their filenames, so they must be in the same folder for the application to work correctly.

3. Open the `index.html` file in your file explorer.
   - Double-click it, or
   - Right-click → **Open with** → your preferred browser (Chrome, Edge, Firefox, etc.).

---

### Using the Application

- Enter a task in the input field.
- Click the **Add** button to add the task to the list.
- Click the checkbox to mark a task as completed.
- Click the **Delete** button to remove a task from the list.

> **Note:** This is a client-side application built with HTML, CSS, and JavaScript. No installation, server setup, or internet connection is required.

## Future Improvements

Some features that can be added in future versions of this project are:

- Save tasks using **Local Storage** so they remain after refreshing the page.
- Add an **Edit Task** feature to update existing tasks.
- Add filters to view **All**, **Active**, or **Completed** tasks.
- Display the number of remaining tasks.
- Improve keyboard navigation and accessibility.
- Enhance the design with animations or a dark mode.

## Author

**Abdullah Safdar**

- 🎓 Business Analytics Student
- 💻 Technologies: HTML, CSS, JavaScript
- 🌐 GitHub: https://github.com/your-abdullahsafdar-max
