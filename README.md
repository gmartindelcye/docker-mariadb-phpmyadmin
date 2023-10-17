# docker-mariadb-phpmyadmin
Docker container for MariaDB and PhpMyAdmin

## Instructions

1. Create permanent volumes routes:

    ```bash
    sudo mkdir -p ./mariadb/data
    ```

2. Run docker compose:

    ```bash
    docker compose up -d
    ```

### Connection to DB

*Connect*: mongo container    (suggestion, could be anything)

*database*: None (you create the database and collections)

*user*: root

*password*: root

## Notes
This configuration will run MariaDB on port 40000 and PhpMyAdmin on port 40001 in your localhost only. For loading phpmyadmin locally you need to open an SSH tunnel like this:

    ```bash
    ssh USERNAME@YOURDOMAIN.COM -L40001:127.0.0.1:40001
    ```

you can now load http://localhost:40001 and will be prompted with phpmyadmin where you can log in with the password you set in the docker-compose.yml file above.

### Connection

root password : root
mysql user:  dbuser 
mysql password: dbuser