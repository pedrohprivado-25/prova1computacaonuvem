# Prova 1 de Computação em Nuvem
Nome: Pedro Henrique privado Alves 
RA: B75D38C11AFDDFB397A2

## O que Fiz

Executei uma Página WEB em um contêiner Docker Chamado estoque.
Usei a imagem nginx:aplpine e a porta 8085 do ambiente.

## Verificação do Contêiner 

root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS              PORTS                                     NAMES
e19505de88b7   nginx:alpine   "/docker-entrypoint.…"   About a minute ago   Up About a minute   0.0.0.0:8085->80/tcp, [::]:8085->80/tcp   estoque

## Teste da Página

root@ubuntu:~$ curl http://localhost:8085
!DOCTYPE html
html lang="pt-BR"
head
meta charsert="UTF-8"
title ESTOQUE /title
head
body
h1 Estoque disponivel /h1
/body
/html

## Explicação 

A imagem nginx:alpine é a base usada para criar o contêiner. Já o contêiner estoque é essa imagem funcionando na prática, onde coloquei meu arquivo index.html.

O 8085:80 serve para ligar a porta 8085 do Ubuntu com a porta 80 do contêiner. Assim, quando acesso localhost:8085, a solicitação é enviada para o Nginx dentro do contêiner, que mostra a página de estoque.
