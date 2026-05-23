# FutureVet API 🐾

Sistema backend desenvolvido com Java e Spring Boot para auxiliar no gerenciamento veterinário, permitindo o cadastro e gerenciamento de usuários, pets, consultas e vacinas.

O projeto foi desenvolvido para a disciplina de Java Advanced da FIAP, seguindo os princípios de APIs RESTful, Programação Orientada a Objetos (POO), arquitetura em camadas e boas práticas de desenvolvimento.

---

# 📌 Objetivo do Projeto

A FutureVet API foi criada com o objetivo de facilitar o controle e gerenciamento de informações veterinárias, oferecendo:

* Cadastro de usuários
* Cadastro de pets
* Controle de consultas veterinárias
* Controle de vacinação
* Busca de informações
* Persistência em banco relacional
* Estrutura desacoplada e organizada

Além do CRUD tradicional, a aplicação também implementa:

* Paginação
* Ordenação
* Busca com parâmetros
* Tratamento de exceções
* Validação de dados
* DTOs
* Swagger
* Cache

---

# 🛠 Tecnologias Utilizadas

## Backend

* Java 17+
* Spring Boot
* Spring Data JPA
* Hibernate
* Maven
* Bean Validation
* Swagger / OpenAPI
* Cache Spring

## Banco de Dados

* H2 Database

---

# 📂 Estrutura do Projeto

```bash
src/main/java/com/futurevet/api
│
├── config
├── controller
├── dto
├── entity
├── exception
├── repository
├── service
└── enums
```

---

# 🧠 Arquitetura da Aplicação

O projeto utiliza arquitetura em camadas para garantir:

* Coesão
* Desacoplamento
* Facilidade de manutenção
* Reutilização de código
* Escalabilidade

## Camadas

### Controller

Responsável pelos endpoints REST.

### Service

Responsável pelas regras de negócio.

### Repository

Responsável pela comunicação com o banco de dados.

### DTO

Responsável pela transferência de dados.

### Entity

Representação das tabelas do banco.

### Exception

Tratamento global de erros e exceções.

---

# 📊 Entidades do Sistema

## 👤 Usuario

Representa os usuários do sistema.

### Principais atributos:

* id
* nome
* email
* senha

---

## 🐶 Pet

Representa os pets cadastrados.

### Principais atributos:

* id
* nome
* espécie
* idade
* tutor

Relacionamento:

* Um usuário pode possuir vários pets.

---

## 📅 Consulta

Representa as consultas veterinárias.

### Principais atributos:

* id
* data
* descrição
* pet

Relacionamento:

* Um pet pode possuir várias consultas.

---

## 💉 Vacina

Representa as vacinas aplicadas.

### Principais atributos:

* id
* nome
* dataAplicacao
* pet

Relacionamento:

* Um pet pode possuir várias vacinas.

---

# 🔗 Relacionamentos

```text
Usuário 1:N Pet
Pet 1:N Consulta
Pet 1:N Vacina
```

---

# ✅ Funcionalidades Implementadas

* CRUD completo
* Persistência de dados
* Relacionamentos com JPA
* Bean Validation
* Paginação
* Ordenação
* Busca por parâmetros
* Swagger
* DTOs
* Tratamento global de exceções
* Cache
* Estrutura RESTful

---

# 🔍 Paginação e Ordenação

A API suporta paginação e ordenação de resultados.

## Exemplo:

```http
GET /pets?page=0&size=10&sort=nome,asc
```

---

# 🧾 Validações

A aplicação utiliza Bean Validation para validação de campos.

Exemplos:

* Campos obrigatórios
* Validação de email
* Tamanho mínimo de senha
* Valores nulos

---

# ⚠️ Tratamento de Exceções

A aplicação possui tratamento global de erros utilizando:

* GlobalExceptionHandler
* BusinessException
* ResourceNotFoundException

---

# 📦 DTOs

Foram utilizados DTOs para:

* Melhor segurança
* Desacoplamento
* Controle de dados enviados/recebidos
* Melhor organização da API

---

# 📘 Swagger

A documentação da API pode ser acessada em:

```bash
http://localhost:8080/swagger-ui.html
```

ou

```bash
http://localhost:8080/swagger-ui/index.html
```

---

# 🚀 Como Executar o Projeto

## 1. Clonar o repositório

```bash
git clone LINK_DO_REPOSITORIO
```

---

## 2. Entrar na pasta do projeto

```bash
cd futurevet-api
```

---

## 3. Executar o projeto

### Maven

```bash
mvn spring-boot:run
```

---

# 🗄 Banco de Dados H2

## Console H2

```bash
http://localhost:8080/h2-console
```

## Configurações padrão

```text
JDBC URL: jdbc:h2:mem:testdb
User: sa
Password:
```

---

# 📮 Endpoints Principais

## 👤 Usuários

```http
POST /usuarios
GET /usuarios
GET /usuarios/{id}
PUT /usuarios/{id}
DELETE /usuarios/{id}
```

---

## 🐶 Pets

```http
POST /pets
GET /pets
GET /pets/{id}
PUT /pets/{id}
DELETE /pets/{id}
```

---

## 📅 Consultas

```http
POST /consultas
GET /consultas
GET /consultas/{id}
PUT /consultas/{id}
DELETE /consultas/{id}
```

---

## 💉 Vacinas

```http
POST /vacinas
GET /vacinas
GET /vacinas/{id}
PUT /vacinas/{id}
DELETE /vacinas/{id}
```

---

# 🧪 Testes da API

Os testes dos endpoints foram realizados utilizando:

* Postman
* Insomnia

A collection/exportação das requisições deve ser adicionada na pasta:

```bash
/documentos
```

---

# 📑 Documentação do Projeto

Sugestão de estrutura:

```bash
/documentos
├── arquitetura.png
├── der.png
├── diagrama-classes.png
├── cronograma.pdf
├── postman-collection.json
└── evidencias-testes
```

---

# 📅 Cronograma e Divisão de Tarefas

| Integrante   | Responsabilidade              |
| ------------ | ----------------------------- |
| Integrante 1 | Backend e entidades           |
| Integrante 2 | Endpoints e regras de negócio |
| Integrante 3 | Documentação e testes         |

---

# 🎯 Conceitos Aplicados

* Programação Orientada a Objetos
* APIs RESTful
* Spring Boot
* JPA/Hibernate
* DTO Pattern
* Repository Pattern
* Exception Handler
* Bean Validation
* Cache
* Paginação
* Arquitetura em camadas

---

# 👨‍💻 Integrantes

* João Caetano
* Adicionar integrantes da equipe

---

# 🔗 Repositório

```bash
Adicionar link do GitHub público
```

---

# 📚 Disciplina

Projeto desenvolvido para a disciplina de Java Advanced — FIAP.
