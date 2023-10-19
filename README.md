# Update Server and Deploy a Web Application

This is a bash script that performs a system update and deploys a web application using the Apache server.

## Prerequisites

Make sure you have a Linux system with root access or superuser permissions. Otherwise, you can run the commands by preceding them with `sudo`.

## How to Use

1. Clone the repository or create a new `deploy.sh` file on your server.

2. Open the terminal and execute the script with the following command:

    ```bash
    ./deploy.sh

## Steps Performed by the Script

1. Update the operating system:

    ```bash
    sudo apt update
    sudo apt upgrade -y

2. Install the Apache web server:

    ```bash
    sudo apt install apache2 -y

3. Install the `unzip` tool:

    ```bash
    sudo apt install unzip -y

3. Download and copy the application files:

    ```bash
    cd /tmp
    wget https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
    unzip main.zip
    cd linux-site-dio-main
    cp -R * /var/www/html/

Now, your server should be updated, and the web application will be available in `/var/www/html/`.

## License

This project is licensed under the **MIT License**.
