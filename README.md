# scattegories-web-app

# pre-requisites to run

Docker Desktop - To allow us to build containers that host our node js http server. these containers are a

# Workflow examples

0. hit **ctrl** + **shift** + **`**
   _open Terminal OR POWERSHELL in VSCode_


## Creating web app 


1. `docker-compose build`
   _build the docker image from the docker compose file and cache locally_

2. `docker-compose run`
   _run the cached image and get up local container_

3. Navigate to http://localhost:8080/
   _local address hosting our server_


## Creating a new branch

When you want to start working on a new feature or fix:

1. `git checkout master`  
   _Switch to the master branch to base your work on the latest stable code._

2. `git pull`  
   _Fetch and integrate the latest changes from the remote master branch._

3. `git checkout -b your-branch-name`  
   _Create and switch to a new local branch for your work._

---

## Adding changes and pushing to remote

After making edits or adding new files:

1. `git status`  
   _Check which files have been modified or added._
   _Can also be seen in Visual studio_

2. `git add filename`  
   _Stage specific files for commit. Use `git add .` to stage everything._

3. `git commit -m "your message"`  
   _Save your changes locally with a descriptive message._

4. `git push origin your-branch-name`  
   _Push your branch and commits to the remote repository._

---

## Merging someone else's changes into your branch

To stay up-to-date with changes from others (e.g., merged into master):

1. `git checkout your-branch-name`  
   _Make sure you're on your working branch._

2. `git fetch`  
   _Get the latest updates from the remote repository._

3. `git merge origin/master`  
   _Merge the latest master changes into your branch._

> If there are conflicts, Git will prompt you to resolve them manually.

---

## Deleting a branch

Once your work is merged and no longer needed:

1. `git checkout master`  
   _Switch to master or another branch before deleting._

2. `git branch -d your-branch-name`  
   _Delete the local branch (safe if already merged)._

3. `git branch -D your-branch-name`  
   _Delete the local branch (unsafe)._

optional- can also do on web ui

4. `git push origin --delete your-branch-name`  
   _Delete the branch from the remote repository._


# folder structure

scattegories-web-app/
├── node_modules/           # Installed dependencies
├── public/                 # Static assets served directly
│   ├── css/                # Stylesheets
│   ├── js/                 # Frontend JavaScript files
│   └── img/                # Images and icons
├── src/                    # Application source code
│   ├── routes/             # API and page route definitions
│   ├── views/              # Templates for rendering HTML (e.g., EJS, Pug)
│   └── server.js           # Express app setup
├── .env                    # Environment variables
├── .gitignore              # Git ignore rules
├── Dockerfile              # Docker container setup
├── docker-compose.yml      # Multi-container orchestration
├── package.json            # Project metadata and scripts
└── README.md               # Project documentation

# libraries used

nodemon -> watches all paths for cahnges to .js, .mjs and .json files and reloads server if files change

express -> most standard http server for dynamic web development 

ejs -> library for express, used to 