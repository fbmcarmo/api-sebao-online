# 📚 Sebão Online API

API REST desenvolvida em **Node.js** para o **Sebão Online**, um marketplace voltado para compra, venda e troca de livros usados.

A API é responsável por fornecer todos os serviços necessários para o funcionamento da plataforma, incluindo autenticação de usuários, gerenciamento de usuários e gerenciamento de livros. A comunicação com o frontend é realizada por meio de endpoints REST, garantindo uma integração simples, segura e eficiente.

O projeto foi desenvolvido utilizando a arquitetura **MVC (Model-View-Controller)**, promovendo organização do código, separação de responsabilidades e facilidade de manutenção.

🔗 **Repositório:** https://github.com/fbmcarmo/api-sebao-online

---

## 🚀 Funcionalidades

* 👤 Cadastro de usuários
* 🔐 Autenticação utilizando JWT
* 🔒 Proteção de rotas autenticadas
* 📚 Cadastro de livros
* 📖 Consulta de livros
* ✏️ Atualização de livros
* ❌ Exclusão de livros
* 🗄️ Persistência de dados em PostgreSQL
* 🌐 API REST para integração com aplicações frontend

---

## 🛠️ Tecnologias Utilizadas

* Node.js
* JavaScript (ES6+)
* Express.js
* PostgreSQL
* Sequelize
* JSON Web Token (JWT)
* Bcrypt
* Dotenv
* CORS

---

## 📂 Estrutura do Projeto

```text
.
├── src
│   ├── config
│   │   └── database.js
│   │
│   ├── controllers
│   │   ├── auth.js
│   │   ├── livros.js
│   │   └── users.js
│   │
│   ├── middlewares
│   │   ├── auth.js
│   │   ├── livros.js
│   │   └── users.js
│   │
│   ├── models
│   │   ├── index.js
│   │   ├── livros.js
│   │   └── users.js
│   │
│   └── routes
│       ├── auth.js
│       ├── livros.js
│       └── users.js
│
├── .env
├── package.json
├── package-lock.json
└── index.js
```

---

## 🏛️ Arquitetura

A aplicação segue o padrão arquitetural **MVC (Model-View-Controller)**.

### Models

Representam as entidades da aplicação e realizam a comunicação com o banco de dados através do Sequelize.

### Controllers

Concentram a lógica de negócio da aplicação, processando as requisições recebidas e retornando as respostas adequadas.

### Routes

Definem os endpoints da API e direcionam as requisições para seus respectivos controllers.

### Middlewares

Executam validações, autenticação e demais regras antes da execução dos controllers.

### Config

Centraliza as configurações da aplicação, incluindo a conexão com o banco de dados.

Essa estrutura favorece a organização do código, facilita a manutenção e permite que novas funcionalidades sejam adicionadas com maior facilidade.

---

## ⚙️ Pré-requisitos

Antes de executar o projeto, certifique-se de possuir instalado:

* Node.js (versão 18 ou superior)
* PostgreSQL
* Git

---

## 📥 Instalação

Clone o repositório:

```bash
git clone https://github.com/fbmcarmo/api-sebao-online.git
```

Entre na pasta do projeto:

```bash
cd api-sebao-online
```

Instale as dependências:

```bash
npm install
```

---

## 🔑 Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto.

Exemplo:

```env
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_NAME=sebao_online
DATABASE_USER=seu_usuario
DATABASE_PASSWORD=sua_senha

JWT_SECRET=sua_chave_secreta

PORT=3000
```

---

## ▶️ Executando a Aplicação

Modo de desenvolvimento:

```bash
npm run dev
```

Modo de produção:

```bash
npm start
```

A API estará disponível em:

```text
http://localhost:3000
```

---

## 🔐 Autenticação

A autenticação é realizada utilizando **JSON Web Token (JWT)**.

Após realizar o login, o token retornado deve ser enviado nas requisições protegidas através do cabeçalho:

```http
Authorization: Bearer SEU_TOKEN
```

---

## 📡 Endpoints da API

### 🔐 Autenticação

| Método   | Endpoint | Descrição                                    |
| -------- | -------- | -------------------------------------------- |
| **POST** | `/login` | Autentica um usuário e retorna um token JWT. |

---

### 👤 Usuários

| Método     | Endpoint     | Descrição                      |
| ---------- | ------------ | ------------------------------ |
| **POST**   | `/users`     | Cadastra um novo usuário.      |
| **GET**    | `/users`     | Lista todos os usuários.       |
| **GET**    | `/users/:id` | Retorna um usuário pelo ID.    |
| **PUT**    | `/users/:id` | Atualiza um usuário existente. |
| **DELETE** | `/users/:id` | Remove um usuário.             |

---

### 📚 Livros

| Método     | Endpoint      | Descrição                            |
| ---------- | ------------- | ------------------------------------ |
| **GET**    | `/livros`     | Lista todos os livros cadastrados.   |
| **GET**    | `/livros/:id` | Retorna um livro pelo ID.            |
| **POST**   | `/livros`     | Cadastra um novo livro.              |
| **PUT**    | `/livros/:id` | Atualiza as informações de um livro. |
| **DELETE** | `/livros/:id` | Remove um livro do sistema.          |

---

## 🔄 Fluxo da Aplicação

```text
Cliente (Frontend)

        │
        ▼

 API REST (Express.js)

        │
        ▼

 Controllers (MVC)

        │
        ▼

 Models (Sequelize)

        │
        ▼

 PostgreSQL
```

---

## 🗄️ Banco de Dados

A aplicação utiliza o **PostgreSQL** como banco de dados relacional e o **Sequelize** como ORM para realizar a comunicação entre a aplicação e o banco de dados.

---

## ✅ Boas Práticas Aplicadas

* Arquitetura MVC
* Arquitetura REST
* Separação de responsabilidades
* Organização em camadas
* Uso de variáveis de ambiente
* Autenticação baseada em JWT
* Criptografia de senhas com Bcrypt
* Utilização de middlewares para autenticação
* Padronização das respostas da API
* Código limpo, organizado e reutilizável

---

## 🚀 Melhorias Futuras

* Implementação de testes automatizados
* Paginação nas consultas
* Filtros avançados para pesquisa de livros
* Upload de imagens para livros
* Docker
* Logs estruturados
* Pipeline de CI/CD
* Cache com Redis

---

## 👨‍💻 Desenvolvedor

**Bruno Moreira**

Full Stack Software Engineer

* GitHub: https://github.com/fbmcarmo
* LinkedIn: https://www.linkedin.com/in/fbmcarmo

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos e de demonstração de conhecimentos em desenvolvimento Full Stack.
