<p align="center" width="100%">
    <img width="50%" src="https://github.com/JonB/demo/blob/main/images/stock-market.jpg"> 
</p>

<h3 align="center">
  Backend de um Sistema de Gerenciamento de Usuários e Contas
</h3>

<p align="center">
  <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-%2304D361">
  <img alt="Language: Java" src="https://img.shields.io/badge/language-java-green">
  <img alt="Version: 1.0" src="https://img.shields.io/badge/version-1.0-yellowgreen">
</p>

## Sobre

Este projeto é um backend em Java 21 com Spring Boot, que permite gerenciar usuários e suas contas. Foi desenvolvido por **JonB** e utiliza MySQL como banco de dados.

---

## Rotas Disponíveis

### Usuários

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| POST   | `/v1/users` | Cria um novo usuário. Recebe `username`, `email` e `password`. |
| GET    | `/v1/users` | Lista todos os usuários cadastrados. |
| GET    | `/v1/users/{userId}` | Retorna os dados de um usuário específico. |
| PUT    | `/v1/users/{userId}` | Atualiza os dados de um usuário (`username` e/ou `password`). |
| DELETE | `/v1/users/{userId}` | Remove um usuário do sistema. |

### Contas

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| POST   | `/v1/users/{userId}/accounts` | Cria uma nova conta para um usuário. Recebe `description`, `street` e `number`. |
| GET    | `/v1/users/{userId}/accounts` | Lista todas as contas de um usuário. |

---

## Tecnologias Utilizadas

* Java 21
* Spring Boot
* Spring Data JPA
* MySQL
* Hibernate
* OpenFeign
* JUnit e Mockito para testes unitários

---

# Como Executar

### 1. Clone o repositório
git clone https://github.com/JonB/demo.git

### 2. Configure o banco de dados MySQL no application.properties
####   Exemplo:
####    spring.datasource.url=jdbc:mysql://localhost:3306/nome_do_banco
####    spring.datasource.username=seu_usuario
####    spring.datasource.password=sua_senha
####   spring.jpa.hibernate.ddl-auto=update

### 3. Execute a aplicação no IntelliJ ou via Maven
mvn spring-boot:run
