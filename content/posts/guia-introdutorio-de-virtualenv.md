+++ 
draft = false
date = 2021-12-08T11:17:25-03:00
title = "Guia Introdutório de Virtualenv"
description = "INtrodução ao ambiente virtual do Python."
slug = ""
authors = ["Kaio Gerhardt"]
tags = []
categories = []
externalLink = ""
series = []
+++

Quando estamos desenvolvendo uma aplicação de modo geral, é muito comum utilizarmos diversas bibliotecas para facilitar e até agilizar o processo. Com a linguagem Python isso não seria diferente.

Durante o desenvolvimento de um projeto, podemos utilizar diversas bibliotecas, algumas vezes repetidas, em versões diferentes. Como por exemplo, poderíamos desenvolver dois projetos, para melhor entendimento vamos chamar de "projeto X" e "projeto Y". No projeto Y utilizamos a biblioteca mysqlclient na versão 1.0, e no projeto X utilizamos a mesma biblioteca na versão 1.5.

Isso acaba sendo algo complexo para o Sistema Operacional gerenciar e geralmente acaba causando incompatibilidade com alguma das versões. Sendo uma das soluções para este problema a utilização de diferentes ambientes virtuais.

## O que é a Virtualenv?
A Virtualenv nada mais é do que um ambiente virtual de desenvolvimento. Onde este ambiente virtual empacota todas as dependências que um projeto utiliza e armazena em um diretório especifico. Fazendo com que assim, nenhum pacote seja instalado no Sistema Operacional, não gerando incompatibilidade.

Com isso, cada projeto pode ter o seu ambiente virtual com suas dependências e suas bibliotecas em versões especificas. Facilitando também a implementação e utilização do projeto em outra máquina, pois assim o projeto vai com todas as suas necessidades sem precisar instalar nada em outra maquina.

## Mas como funciona a Virtualenv?
De maneira simples, o ambiente virtual realiza uma cópia de tudo o que um programa na linguagem Python precisa para executar.

Esta cópia inclui:
1. O código fonte do seu projeto, escrito por você;
2. PIP (que é o gerenciado de pacotes do python);
3. Bibliotecas padrão do Python;
4. Versão utilizada do Python;
5. E as bibliotecas instaladas com o Python.

## Como instalar a virtualenv?
A instalação se dá pelo gerenciador de pacotes do Python, o PIP, de maneira bem simples. Para instalar é necessário apenas que utilize o comando abaixo no seu terminal.

``
pip install virtualenv
``

Com isso, a Virtualenv será instalada e vai estar pronta pra ser utilizada.

## Como criar uma nova virtualenv?
Para a criação de um novo ambiente virutal é bastante simples, é necessário utilizar apenas o comando demonstrado abaixo no terminal do seu Sistema Operacional. Lembrando que é necessário estar dentro do diretório no qual quer que o ambiente seja criado.

``
virtualenv nome_da_virtualenv
``

Como por exemplo: 
``
virtualenv venv1    
``

Com isso, criamos o ambiente virtual do projeto chamado "venv1". É ela que vai comportar todos os pacotes necessários para a execução.

## Como ativar a virtualenv?

Depois de criar o ambiente é necessário ativa-lo, a "ativação" do ambiente nada mais é do que entrar no terminal do ambiente. Para a ativação, utilizamos o seguinte comando:

``
nome_da_virtualenv/Scripts/Activate 
``

No nosso exemplo seria: 
``
venv1/Scripts/Activate
``

Ou também, é possível ativar o ambiente navegando pelos diretórios no CMD até chegar no .exe no activate. Sendo o caminha o seguinte:

``
venv\Scripts
``

E depois rodar o comando "activate" no terminal para ativar o ambiente. Após ativar, irá notar que na linha de comando vai aparecer um "(venv)", indicando que o ambiente está ativado e que tudo digitando após será aplicado dentro do ambiente.

``
(venv) C:\Users\Kaio\Desktop\projetox\venv1\Scripts>
``

## Como desativar o ambiente virtual?
Para desativar o ambiente é bem mais simples do que ativá-lo. Estando dentro do ambiente com a tag "(venv)" na frente da linha de comando, é necessário apenas rodar o comando "deactivate" e pronto, ambiente desativado.

## Instalando pacotes!
A instalação de pacotes por meio gerenciador de pacotes, o PIP, é feito da maneira convencional. Só lembrando que é necessário esta com o ambiente ativado e com a tag "(venv)" na linha de comando. Para exemplificar, segue abaixo o comando para instalar o pacote pyinstaller no ambiente virtual.

``
(venv) C:\Users\Kaio\Desktop\projetox\venv1\Scripts> pip install pyinstaller
``

## Considerações Finais.

Com este pequeno guia podemos notar o quão fácil é utilizar o virtualenv, e o quanto ele pode facilitar no nosso dia e quanta dor de cabeça pode evitar. Eliminando não apenas a incompatibilidade de projetos, mas também facilitando a utilização do mesmo em outras máquinas.