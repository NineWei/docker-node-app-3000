# 🐳 Node.js App - Dockerizado (Porta 3000)

Este projeto demonstra a conteinerização de uma aplicação Node.js simples usando **Docker**.

## Visão Geral

O objetivo é empacotar a aplicação Node.js em uma imagem Docker para que ela possa ser executada de forma **isolada e consistente** em qualquer ambiente, mapeando a porta interna do container para a porta **3000** da máquina local.

## Pré-requisitos

Certifique-se de que você tem as seguintes ferramentas instaladas na sua máquina:

* **Node.js e npm** (para testes e gerenciamento de dependências).
* **Docker** (para construir e rodar a imagem).

## Estrutura do Projeto

O projeto principal consiste em:

- App.mjs: O arquivo de entrada principal da aplicação Node.js.

- helpers.mjs: Módulo com funções auxiliares da aplicação.

- package.json: Lista de dependências e script de inicialização (npm start).

- Dockerfile: O arquivo que contém as instruções para construir a imagem.

---

## 📦 Como Rodar a Aplicação

Siga os passos abaixo para construir a imagem Docker e iniciar o container:

### 1. Construir a Imagem Docker

Você construiu a imagem sem dar um nome, o que resulta em uma imagem com nome e *tag* **`<none>`**:

```bash
docker build .
```

### 2. Encontrar o ID da Imagem

Para rodar o container, precisamos do ID da Imagem gerada. Use o comando docker images e procure a imagem <none> no topo da lista:

```bash
docker images
```

### 3. Rodar o Container (Usando o ID)

Use o ID da Imagem encontrado (ex: 5b3b3a3c1d2e) no comando docker run.

```bash
docker run -p 3000:3000 5b3b3a3c1d2e
```

### Aplicação em Funcionamento

- [local_host_3000](#local_host_3000)

### Parar o Container

Quando terminar de testar, pare o container:

```bash
docker ps  # Encontre o NAME
docker stop <NAME>
```
