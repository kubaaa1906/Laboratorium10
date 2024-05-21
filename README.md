# Laboratorium10

Użyte polecenia:
1. Stworzenie sieci: docker network create --driver=bridge --subnet=10.0.0.0/24 lab10net
2. Uruchomienie kontenera 1: docker run -d --name web1 --network lab10net -p 8081:80 --mount type=bind,source=C:\Users\Kuba\Lab10,target=/usr/share/nginx/html,readonly --mount type=bind,source=C:\Users\Kuba\Lab10\web1,target=/var/log/nginx nginx:latest

  Uruchomienie kontenera 2: docker run -d --name web2 --network lab10net -p 8082:80 --mount type=bind,source=C:\Users\Kuba\Lab10,target=/usr/share/nginx/html,readonly --mount type=bind,source=C:\Users\Kuba\Lab10\web2,target=/var/log/nginx nginx:latest

  Uruchomienie kontenera 3: docker run -d --name web3 --network lab10net -p 8083:80 --mount type=bind,source=C:\Users\Kuba\Lab10,target=/usr/share/nginx/html,readonly --mount type=bind,source=C:\Users\Kuba\Lab10\web3,target=/var/log/nginx nginx:latest
