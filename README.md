Kaiburr Task 3 – React Frontend with Spring Boot Backend

This project is part of the Kaiburr assignment series.
In Task 1, a Java Spring Boot backend was created to manage task objects and run shell commands.
In this Task 3, a full web interface has been built using React (with TypeScript and Ant Design) that interacts with that backend through REST APIs.

Overview
The web UI allows users to:
Create new tasks
View all existing tasks from MongoDB
Search for tasks by name
Delete tasks
Run shell commands for a selected task and view their output directly in the browser
All data operations are handled through the backend REST API, which stores and retrieves information from a MongoDB database.

Technologies Used
Backend:
Java Spring Boot
MongoDB
Maven
Frontend:
React 19
TypeScript
Ant Design
Axios
Vite

How to Run the Application
1. Start the Backend
A.Open a terminal and navigate to:
  C:\Users\prabi\OneDrive\Desktop\PranavBijuNair\Kaiburr\Task3\task3
  
  
  B. Run the following command:
  mvn spring-boot:run
  
  
  C. Once started, the backend will be running on:
  http://localhost:8080

2. Start the Frontend
A.Open another terminal and navigate to:
C:\Users\prabi\OneDrive\Desktop\PranavBijuNair\Kaiburr\Task3\frontend

B.Run:
npm install
npm run dev

C.Open the link shown in the terminal (usually):
http://localhost:5173

Application Features
1. Create Task
A “+ Create Task” button opens a form where users can add a new task by specifying:
ID
Name
Owner
Command
After submission, the task is saved to MongoDB and appears in the table instantly.

2. View All Tasks
All existing tasks are displayed in a clean, paginated Ant Design table.
Each row shows ID, name, owner, and command.

3. Search Task
Users can search for any task by name using the search bar on top.
Matching results are displayed instantly.

4. Delete Task
Each task row includes a Delete button.
Clicking it removes the task from both the table and the database.

5. Run Command
Each task also includes a Run button.
When clicked, the backend executes the stored shell command.
The output is then displayed in a popup modal on the UI.

API Endpoints (Backend)
| Method | Endpoint                  | Description                           |
| ------ | ------------------------- | ------------------------------------- |
| GET    | /tasks                    | Get all tasks                         |
| GET    | /tasks?id={id}            | Get a single task by ID               |
| PUT    | /tasks                    | Create or update a task               |
| DELETE | /tasks/{id}               | Delete a task                         |
| GET    | /tasks/search?name={name} | Search tasks by name                  |
| PUT    | /tasks/{id}/execute       | Execute the stored command for a task |


Example Output (After Running a Command)
When running a task such as:
echo Hello Kaiburr

The UI displays:
Task Execution Output
Hello Kaiburr

Author
Pranav Biju Nair
Kaiburr Assignment – Task 3

