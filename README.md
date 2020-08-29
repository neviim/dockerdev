# Install Docker-compose
```bash
# Install docker-compose
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/\
docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

$ sudo chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
$ docker ps
```


# Executando o dockerfile

```bash
# cria o build da aplicação webserver criada em golang
docker built -t neviim/golangJads-docker .

# executa a alicação utilizando o docker com a golang
docker run -p 8080:8080 neviim/golangjads-docker:latest

# sobe esta imagem para o repositorio docker hub
docker push neviim/golangjads-docker:latest
```


# usando docker-compose
```bash
#  monta os micro serviçoes em container com opção de rebuild
docker-compose up -d --build
docker-compose up -d
docker-compose build

# Nginx webserver pagina index.html
http://192.168.0.44:8080

# Golang webserver
http://192.168.0.44:8081

# lista os container ativos
docker-compose ps

# para matar todos os serviçoes
docker-compose down
```


### Docker comandos uteis
```bash
# remove um container em execução
docker rm -f 47696d8a4d6a 

# remove a imagem
docker rmi -f 17da892442fa



```
