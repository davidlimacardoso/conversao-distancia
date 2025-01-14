
# Conversão de Distância

Este projeto é uma aplicação web simples que permite a conversão de distâncias entre diferentes unidades (por exemplo, milhas para quilômetros). A aplicação é construída com Python e utiliza o Gunicorn como servidor WSGI.

### Link da imagem no Docker Hub [aqui](https://hub.docker.com/repository/docker/davidlimacd/conversao-distancia/general) 🖼️ 🔗

## Estrutura do Projeto

```bash
    .
    ├── app.py # Código principal da aplicação
    ├── Dockerfile # Dockerfile para construção da imagem
    ├── README.md # Documentação do projeto
    ├── requirements.txt # Dependências do projeto
    └── templates
    └── index.html # Template HTML da aplicação
```

## Pré-requisitos

- Docker instalado na sua máquina.

## Instalação

1. Clone este repositório:
```bash
   git clone https://github.com/davidlimacardoso/conversao-distancia
   cd conversao-distancia
```
2. Construindo a imagem Docker:
```bash
docker build -t conversao-distancia -f Dockerfile .
```

3. Listar as imagens para verificar se a imagem foi criada:
```bash
docker images
```

4. Executando o container:
```bash
docker run -d -p 8181:5000 conversao-distancia
```
5. Verificando se o container está em execução:
```bash
docker ps
```

## Publicação no Docker Hub
### Para publicar a imagem no Docker Hub, é necessário seguir os seguintes passos:

1. Construindo a imagem com uma tag específica:
```bash
docker build -t davidlimacd/conversao-distancia:v1 -f Dockerfile .
```

2. Fazendo o push da imagem para o Docker Hub:
```bash
docker push davidlimacd/conversao-distancia:v1
```

3. Adicione a tag latest:
```bash
docker tag davidlimacd/conversao-distancia:v1 davidlimacd/conversao-distancia:latest
```

4. Fazendo o push da imagem:
```bash
docker push davidlimacd/conversao-distancia:latest
```

5. Acesse a imagem no Docker Hub:

**Link**: https://hub.docker.com/repository/docker/davidlimacd/conversao-distancia/general

## Acessando a Aplicação
Após executar o container, acesse a aplicação em seu navegador através do seguinte URL:

```
http://localhost:8181
```

Contribuições
Contribuições são bem-vindas! 
