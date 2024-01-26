Part 1: write and test the server-side code powered by Django and Django Channels.
Objectives
By the end of Part 1, you will be able to:

1. Create simple GET requests with Django REST Framework.
2. Implement token-based authentication with JSON Web Tokens (JWT).
3. Use Django Channels to create and update data on the server.
4. Send messages to the UI from the server via WebSockets.
5. Test asyncio coroutines with pytest.

Create simple GET requests with Django REST Framework.
Setting Up the server:
        <!-- Commands: -->
        $ mkdir taxi-app && cd taxi-app
        $ mkdir server && cd server
        $ python3.7 -m venv env
        $ source env/bin/activate
        $ django-admin.py startproject taxi
        $ cd taxi
        $ python manage.py startapp trips

        <!-- Download Postgres and Redis -->
        $ brew install postgresql
        $ brew services start postgresql
        $ brew install redis
        $ brew services start redis

        <!-- Connect to Postgres using the psql client. -->
        $ psql -U postgres
        sudo -u postgres createuser <username>
        sudo -u postgres createdb <dbname>
        alter user <username> with encrypted password '<password>';
        psql=# grant all privileges on database <dbname> to <username> ;
        setting environment variable to :
        export PGDATABASE=taxi
        export PGUSER=taxi
        export PGPASSWORD=taxi

