## How to Connect to and Use PostgreSQL with Laravel

Laravel comes with mysql connections, by default. Some projects might have need for different database to be used. One popular database is PostgreSQL.

Below are the steps to achieve this:

- Download PostgreSQL from [the official website](https://www.postgresql.org/download/).
- Install it on your machine
- Create a fresh laravel project via composer create-project laravel/laravel your-project-name
- You will be prompted to set up your postgresql connection password. Do that and take note of the password. You may create a new user as well.
- Create a table in PgAdmin. I am going to be using a table called laravel-with-postgresql.
- Update your .env file with the following details:

    1. DB_CONNECTION=pgsql
    2. DB_HOST=127.0.0.1
    3. DB_PORT=5432
    4. DB_DATABASE=your-database-name
    5. DB_USERNAME=database-owner-name
    6. DB_PASSWORD=database-owner-password

- Now you can go ahead to run your migrations from the command line via php artisan migrate
- You should get the output below, showing the status of each migration
- Open your PgAdmin and confirm that the table in question has the tables migrated
- Voila, you have successdully linked laravel with PostgreSQL
- At this point, you can go ahead to use the database via laravel's Eloquent ORM, just like you would use MySQL with it.

### Good Luck!

