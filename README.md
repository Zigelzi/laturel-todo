# Laturel ToDo
ToDo app for creating and sharing projects with customers

## How to deploy
1. Clone this repository to directory of your choosing
2. Clone the todo-spa and todo-api repositories to ./services/ folder of this repository
    * API: https://github.com/Zigelzi/laturel-todo-api
    * SPA: https://github.com/Zigelzi/laturel-todo-spa
3. Set environment variables
    * SECRET_KEY
    * TODO_POSTGRES_USER_*ENVIRONMENT*
    * TODO_POSTGRES_PASSWORD_*ENVIRONMENT*
    * TODO_DATABASE_NAME_*ENVIRONMENT*
    * TODO_DATABASE_URL_*ENVIRONMENT*
4. A: To build development environment execute docker-compose up -d --build in the root directory
    * Create the database with docker-compose exec todo-api python manage.py create_db
4. B: To build staging environment execte docker-compose -f docker-compose.stage.yml up -d --build
    * Create the database with docker-compose -f docker-compose.stage.yml exec todo-api python manage.py create_db
5. Go play! Dev environment can be found from localhost:1337 and staging from todo.laturel.fi
