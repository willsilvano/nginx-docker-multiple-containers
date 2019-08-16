## Setup

Follow the next steps:

1. Edit the `/etc/hosts` file and put the websites url:

    - 127.0.1.1	site1.com
    - 127.0.1.1	site2.com
    - 127.0.1.1	site3.com

2. Execute net command to create a new Docker network:

    ```
    bash nginx/create-net.sh
    ```

3. Start the nginx container:

    ```
    docker-compose -f "nginx/docker-compose.yml" up -d
    ```

4. Start the websites containers:

    ```
    docker-compose -f "site1/docker-compose.yml" up -d
    
    docker-compose -f "site2/docker-compose.yml" up -d
    
    docker-compose -f "site3/docker-compose.yml" up -d
    ```

5. Access the website containers:
    - http://site1.com
    - http://site2.com
    - http://site3.com


These configurations are based on `nginx-proxy` Docker image. 

More info https://github.com/jwilder/nginx-proxy