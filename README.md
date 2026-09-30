# Prova---P1---Computacao-em-Nuvem
Nome: Felipe Wodewotsky
RA: ecdc9dcb2d2eeef4fee4

## O que fiz
Executei uma página web em um contêiner Docker chamado Estoque.
Usei a imagem nginx:alpine e a porta 8085 do ambiente.

## Verificação do contêiner

root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                     NAMES
148377c3bae7   nginx:alpine   "/docker-entrypoint.…"   49 seconds ago   Up 49 seconds   0.0.0.0:8085->80/tcp, [::]:8085->80/tcp   estoque

## Teste da página

root@ubuntu:~$ curl http://localhost:8085
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Estoque</title>
</head>
<body>
<h1>Estoque disponivel</h1>
</body>
</html> 

## Explicação

O contêiner é utilizado para armazenar e executar uma instância da imagem nginx:alpine, que existe na rede e está sempre em execução. O mapeamento 8085 foi utilizado para definir uma porta ao processo, sendo executado com o comando curl, que apresentou o que estava registrado na porta 8085, este sendo o index.html criado.
