# To-do-List
My goal was to create a simple todo list using React that was interactive, easy to use, and had a cohesive design.
To start I broke down the UI into a component hierarchy considering each class, css, and design layers. 
1. App.jsx contains the entire app.
2. NewToDoForm.jsx contains the user input
3. TodoList.jsx displays the todo list
4. TodoItem.jsx displays and deletes each todo list item

To start I broke down the UI into a component hierarchy considering each class, css, and design layers. 1. App.jsx contains the entire app. 2. NewToDoForm.jsx contains the user input 3. TodoList.jsx manages the todo list 4. TodoItem.jsx displays and deletes each todo list item
<br />

The App.jsx component is the parent component that renders a form for adding new todo items (NewTodoForm) and a list of existing todo items (TodoList). These components work together to manage the state of todos and provide functionality for adding, toggling, and deleting todo items.
<br />

In order to make the list items interactive, I created a NewToDoForm.jsx. The overall purpose of this component is to provide a form for adding new items. It receives a prop onSubmit with the value of the addTodo function. The addTodo function is a callback used to handle the submission of new todo items. When the form is submitted, it triggers the handleSubmit function, which in turn calls the onSubmit function with the lowercased value of the entered item. After submission, the input field is cleared by setting the newItem state to an empty string. I incorperated useState to take in an event object and setNewItem to event target value get the input value and set it as the new item value. With the onChange, it allows the new item to get set as the value of the input. I did this by changing the state variable. The value is controlled by the newItem state, and the onChange event updates the newItem state with the entered value.
<br />

The TodoItem component provides a visual representation of an individual todo item with a checkbox for marking completion status and a delete button for removing the todo. The interaction with the checkbox and delete button triggers the corresponding callback functions passed as props (toggleTodo and deleteTodo). 
<br />

The ToDoList.jsx  component is responsible for rendering the list of todo items. It receives three props: todos, toggleTodo, and deleteTodo. These props are functions and data related to managing todo items. The todos prop is an array of todo items, while toggleTodo and deleteTodo are functions to handle toggling and deleting todos. The map() function maps over the todos array, creating a TodoItem component for each todo in the list. Each TodoItem is passed the properties of the individual todo (...todo), a unique key based on the id of the todo, and the toggleTodo and deleteTodo callback functions. The conditional rendering ensures that if the list is empty, a message indicating "No Todos" is displayed.

reference tutorial from : https://youtu.be/Rh3tobg7hEo?feature=shared 

