# waterdip_assignment

Given Problem Statement:

You will be building a server that can keep track of tasks. Your server must be able to do the following:

1. Create a new task with a title property and a boolean determining whether the task has been completed. A new unique id would be created for each new task

2. List all tasks created

3. Get a specific task

4. Delete a specified task

5. Edit the title or completion of a specific task

6. (Extra Credit) Bulk add multiple tasks in one request

7. (Extra Credit) Bulk delete multiple tasks in one request

Your application will accept JSON and/or URL parameters and will return JSON data. Your server would be ready to be automatically integrated in a web system

Sample Input 1: (Create A new Task)

Request1 [Method: POST] = http://localhost:5000/tasks

Body:

{
  "title": "Python Programming"
}

Output 1:

{
    "completed": false,
    "id": 1,
    "title": "Python Programming"
}

Sample Input 2: (Get all The Tasks)

Request2 [Method: GET] = http://localhost:5000/tasks

Output 2:

[
    {
        "completed": false,
        "id": 1,
        "title": "Python Programming"
    }
]

Sample Input 3: (Get Specific Task)

Request3 [Method: GET] : http://localhost:5000/tasks/1

Output 3:

{
    "completed": false,
    "id": 1,
    "title": "Python Programming"
}

Sample Input 4: (Delete Specific Task)

Request4 [Method: Delete] : http://localhost:5000/tasks/1

Output 4:

{
    "message": "Task deleted successfully"
}

Sample Input 5: (Modify Specific Task)

Request5 [Method: PUT] : http://localhost:5000/tasks/1

Body:

{
    "title":"C Programming"
}

Output 5:

{
    "completed": false,
    "id": 1,
    "title": "C Programming"
}

Sample Input 6 :(Add multiple Tasks)

Request6 [Method: POST] : http://localhost:5000/tasks/bulk

Body:

{
    "tasks":
    [
        {
            "title":"Java Programming"
        },
        {
            "title":"Python Programming"
        }
    ]
}

Output 6:

{
    "message": "Bulk tasks added successfully"
}

Sample Input 7: (Delete Multiple Tasks)

Request7 [Method: Delete]: http://localhost:5000/tasks/bulk

Body:

{
    "task_ids":[1,2]
}

Output 7:

{
    "message": "Bulk tasks deleted successfully"
}


