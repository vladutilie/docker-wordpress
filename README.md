# WordPress on Docker
This repository provides the necessary files to set up WordPress using Docker. It allows you to quickly deploy a WordPress instance with a MySQL database and phpMyAdmin for easy database management.

## Prerequisites
Before you get started, make sure you have the following tools installed on your system:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started
To set up WordPress on Docker, follow these steps:

1. Clone this repository to your local machine:

```
git clone https://github.com/vladutilie/docker-wordpress.git wp-with-docker
```

2. Navigate to the cloned repository:

```
cd wp-with-docker
```

3. Create a copy of the .env.example file and name it .env:

```
cp .env.example .env
```

4. Open the `.env` file in a text editor and configure the following environment variables:

- **`MYSQL_DATABASE`**: The name of the MySQL database for WordPress.
- **`MYSQL_ROOT_PASSWORD`**: The root password for the MySQL database.
- **`MYSQL_USER`**: The MySQL user for WordPress.
- **`MYSQL_PASSWORD`**: The password for the MySQL user.
- **`NAME`**: A name for your WordPress Docker containers (e.g., my-wordpress-website).
  
5. In the `docker-compose.yml` file, you can customize the following options:

- **`container_name`**: The container name if needed.
- Ports, volumes, and environment variables as per your requirements.

6. Start the containers:

```
docker-compose up -d
```

7. Access your WordPress site in a web browser by navigating to `http://localhost:8000` (or replace localhost with your server's IP address).

8. You can also access phpMyAdmin at `http://localhost:8080` to manage your database using the credentials you set in the `.env` file.

## Customizing PHP Settings
You can customize PHP settings by editing the `uploads.ini` file in this repository. It currently sets file upload limits and memory limits to generous values. Make sure to adjust these settings according to your needs.

## Contributing
If you'd like to contribute to this project, please open an issue or submit a pull request with your suggested changes.

## License
This project is free of any personal or commercial use. Use it as you want. 😌

Enjoy your WordPress development with Docker! 🚀
