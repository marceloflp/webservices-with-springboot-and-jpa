# API DE GERENCIAMENTO DE PEDIDOS

Uma API REST desenvolvida em **Java utilizando Spring Boot** para gerenciamento de pedidos, produtos e usuários.

O objetivo deste projeto é simular o funcionamento básico de um sistema de pedidos, semelhante ao núcleo de um e-commerce. A aplicação permite cadastrar usuários, listar produtos, consultar pedidos e visualizar os itens associados a cada pedido.

Este projeto foi desenvolvido com foco em praticar conceitos fundamentais do ecossistema Spring, especialmente a criação de APIs REST e o mapeamento de entidades com JPA.

---

## Tecnologias utilizadas

- Java  
- Spring Boot  
- Spring Web  
- Spring Data JPA  
- Hibernate  
- Maven  
- Banco de dados H2  

---

## Sobre o projeto

A aplicação implementa um modelo de domínio simples envolvendo usuários, produtos, categorias e pedidos.

A ideia principal foi exercitar:

- construção de **APIs REST**
- modelagem de entidades com JPA
- relacionamentos entre entidades
- organização da aplicação em camadas
- utilização do **Spring Data JPA** para acesso a dados

O projeto segue uma estrutura comum em aplicações Spring Boot, separando responsabilidades entre controllers, services e repositories.

---

## Modelo de domínio

As principais entidades do sistema são:

- **User** – representa os usuários da aplicação  
- **Order** – representa os pedidos realizados pelos usuários  
- **Product** – produtos disponíveis no sistema  
- **Category** – categorias dos produtos  
- **OrderItem** – itens que compõem um pedido  
- **Payment** – pagamento associado ao pedido  

Alguns relacionamentos importantes:

- Um usuário pode ter vários pedidos
- Um pedido possui vários itens
- Cada item referencia um produto
- Produtos podem pertencer a mais de uma categoria

---

## Estrutura do projeto
O projeto está organizado em camadas seguindo um padrão bastante utilizado em aplicações Spring:
```
src/main/java/com/educandoweb/course

config
entities
repositories
services
resources
exceptions
```

### Entities

Contém as entidades JPA que representam o modelo de domínio da aplicação.

### Repositories

Interfaces responsáveis pelo acesso ao banco de dados utilizando Spring Data JPA.

### Services

Camada responsável pelas regras de negócio da aplicação.

### Resources (Controllers)

Responsável por expor os endpoints REST da API.

### Config

Contém classes de configuração e inicialização de dados de teste.

---

## Endpoints principais

### Users
- GET /users
- GET /users/{id}
- POST /users
- PUT /users/{id}
- DELETE /users/{id}

## Products
- GET /products
- GET /products/{id}

## Categories
- GET /categories
- GET /categories/{id}

## Orders
- GET /orders
- GET /orders/{id}


---

## Como executar o projeto

### Clonar o repositório

```bash
git clone https://github.com/marceloflp/webservices-with-springboot-and-jpa.git
```

### Entrar na pasta do projeto
```bash
cd webservices-with-springboot-and-jpa
```

### Executar a aplicação
```bash
./mvnw spring-boot:run
```
---

### Objetivos do projeto
Este projeto foi desenvolvido como parte dos estudos sobre desenvolvimento de aplicações backend com Spring Boot.

A implementação busca consolidar conhecimentos sobre:

- APIs REST
- JPA e Hibernate
- Relacionamento entre entidades
- Arquitetura em camadas
- Organização de projetos Spring
