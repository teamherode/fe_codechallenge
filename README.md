# Teamhero Code-Challenge (Frontend)

## Situation:

A user is looking for fitting jobs on the Teamhero platform. He is presented with a list of jobs that he can apply to. 

The application process is simple: The user selects all jobs he wants to apply to in a form and clicks submit.

The user can have skills assigned to his profile. If a job requires a skill, the user needs to have this skill in order to apply to the job.

## Requirements:

Please create a simple frontend application that allows the user to select jobs and submit applications to them.

There are 4 endpoints available:

- `GET /me` - Returns data about the current user
- `GET /project_shifts` - Returns a list of available jobs
- `GET /project_shifts?id=1` - Returns a single job with the given id
- `GET /project_shift_applications` - Returns a list of applications that have been submitted
- `GET /project_shift_applications?id=1` - Returns a single application with the given id
- `POST /project_shift_applications` - Creates a new application
- `GET /skills` - Returns a list of all skills
- `GET /skills?id=1` - Returns a single skill with the given id

## Task:

- Every job has a `start` and `end` date and an `area`, where the job is located. Please display the jobs grouped by area and sorted by start date (ascending).
- if a user has already applied to a job, he should not be able to apply again
- **Bonus**: If a job has `skills` assigned, the user needs to have this skill in order to apply to the job (`/me` endpoint). Please add a validation to the form that checks if the user has all the skills required for the jobs he wants to apply to and show some kind of validation message, if he doesn't.

## Mock data

To start the mock data server, you can run: 

```bash
npx json-server ./mock/db.json --port 3004
```

This will start the server on [localhost:3004](http://localhost:3004).

You will need to send a `POST` request for every chosen job to `/project_shift_applications` to create an application with the following body example:

```json
{
  "contact": "121",
  "shift": "101",
  "note": "this sounds super good!"
}
```

## Our expectations:

We would like to see, how you would approach solving this technical task. We are specially interested, how you structure your code. Please put emphasis on clean code, reusable components and seperation of concerns.

You are encouraged to use any libraries you like. We are using React in our frontend, so if you are familiar with that, feel free to use it. If you feel more comfortable with another framework, that's fine too. Also feel free to utilise any other tools you like. 

## Submission:

Please send us a link to a GitHub repository with your solution. If you have any questions, feel free to contact us at any time. If you don't have time to finish the task, please prepare a MVP and explain how you would continue to work on it.

## Hints:

- if you need more inside on how `json-server` works, you can find the documentation here: [https://github.com/typicode/json-server](https://github.com/typicode/json-server)

## Happy coding! 🚀
