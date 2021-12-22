# Project - Build a Task Manager

## Features
	- Multiple users can use the app 
	- Every user can add tasks 
	- After creating a task, user can assign it to different user 
	- Tasks
		- has a description
		- priority: enum<high/low/medium>
		- has a due date
		- has a state: pending / completed 
		- Notes
			- A task can have multiple notes inside it
			- Notes can be made by the owner or asignee 
	- The creator of the task can edit / delete the task 
	- The creator or asignee can mark the task as done 


## DB Schema Design

base_table
- id  - 			integer autoincrement primary key
- created_at - 	date
- updated_at -	date
	

users
- name - string(100)
- email - string(100) : validate(email)

tasks
- description - string
- priority - enum[high,medium,low]
- due_date - date
- status   - enum[pending,completed]
- creator_id  - fk(users.id)
- asignee_id	- fk(users.id)

notes 
- task_id		- fk(tasks.id)
- description - string 
- author_id	- fk(users.id)

## REST API








