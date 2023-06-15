# SecurePanHandler
Panhandler over TLS

Install Panhandler on the host

```curl -s -k -L https://raw.githubusercontent.com/PaloAltoNetworks/panhandler/master/ph | bash```

To use SecurePanHandler, get the files on a directory and create a TLS keypair in the ./conf.d/ directory named `server.key` and `server.crt`.

```openssl req -x509 -newkey rsa:2048 -nodes -keyout conf.d/server.key -out conf.d/server.crt -days 365```

Enter `docker-compose up -d` or `docker compose up -d` or  and access panhandler on the Docker host via https://yourhost:8080/

Login with the username and password specified in the docker-compose.yml file.
