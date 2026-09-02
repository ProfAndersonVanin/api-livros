# 📚 Sistema de Biblioteca

> **Projeto desenvolvido na disciplina de SW-II · Sistemas Web II**  
> ETEC Professora Maria Cristina Medeiros

---

## 🎯 Sobre o projeto

Este projeto tem como objetivo desenvolver, de forma incremental, uma **aplicação web para gerenciamento de livros**, utilizando uma arquitetura baseada em **API REST + Banco de Dados + Front End**.

Ao longo das etapas, serão trabalhados conceitos de desenvolvimento de APIs, persistência de dados, operações CRUD e integração entre Back End e Front End.

### 🏗️ Tecnologias utilizadas

| Camada | Tecnologia |
|---|---|
| ⚙️ Back End | **FastAPI** |
| 🐍 Linguagem | **Python** |
| 🗄️ Banco de Dados | **MySQL** |
| 🌐 Front End | **HTML5 + CSS3 + JavaScript** |
| 🔌 Comunicação | **API REST / HTTP** |
| 📦 Gerenciamento | **Git e GitHub** |

---

## 🧩 Arquitetura do projeto

A aplicação será construída seguindo uma estrutura simples de três camadas:

```text
┌──────────────────────────────┐
│          FRONT END           │
│      HTML + CSS + JS         │
└──────────────┬───────────────┘
               │
               │ HTTP / JSON
               ▼
┌──────────────────────────────┐
│           API REST           │
│           FastAPI            │
└──────────────┬───────────────┘
               │
               │ SQL / ORM
               ▼
┌──────────────────────────────┐
│          DATABASE            │
│            MySQL             │
│       biblioteca_db          │
└──────────────────────────────┘
```

---

# 🚀 Etapas do projeto

O desenvolvimento será realizado em **4 etapas**, permitindo que o sistema seja construído gradualmente.

---

## 🟢 Etapa 1 · Fundação

### 🔧 Preparação do ambiente

Nesta etapa será preparada toda a estrutura inicial necessária para o desenvolvimento da aplicação.

### Conteúdos

- 🐍 Configuração do ambiente Python
- 📦 Instalação das dependências
- 📁 Organização inicial do projeto
- 🗄️ Criação do banco de dados `biblioteca_db`
- 🔌 Configuração da conexão com o MySQL
- ⚙️ Configuração inicial do FastAPI
- ❤️ Criação de uma rota de saúde da API

### Endpoint inicial

```http
GET /health
```

Resposta esperada:

```json
{
    "status": "ok"
}
```

### 🎯 Objetivo

Ao final desta etapa, teremos uma **API FastAPI funcionando e conectada ao banco de dados MySQL**.

---

## 🔵 Etapa 2 · Modelo e consultas

Nesta etapa será iniciada a implementação das funcionalidades relacionadas aos livros.

### 📚 Conteúdos

- 🧱 Criação do modelo `Livro`
- 🗄️ Configuração da tabela no banco de dados
- 📋 Criação dos schemas
- 🔌 Configuração da sessão do banco
- ➕ Implementação da rota `POST`
- 📖 Implementação da rota `GET`

### Principais endpoints

| Método | Endpoint | Função |
|---|---|---|
| `POST` | `/livros` | ➕ Cadastrar livro |
| `GET` | `/livros` | 📚 Listar livros |

### 🎯 Objetivo

Permitir que a API seja capaz de **cadastrar e consultar livros armazenados no MySQL**.

---

## 🟠 Etapa 3 · CRUD completo

Nesta etapa a API será ampliada para permitir todas as operações fundamentais de um sistema CRUD.

### 🔄 Operações

- ➕ **Create** · Criar
- 🔎 **Read** · Consultar
- ✏️ **Update** · Atualizar
- 🗑️ **Delete** · Excluir

### Principais endpoints

| Método | Endpoint | Função |
|---|---|---|
| `POST` | `/livros` | ➕ Cadastrar livro |
| `GET` | `/livros` | 📚 Listar livros |
| `GET` | `/livros/{id}` | 🔎 Consultar livro |
| `PUT` | `/livros/{id}` | ✏️ Atualizar livro |
| `DELETE` | `/livros/{id}` | 🗑️ Excluir livro |

### 🛡️ Tratamento de erros

Também serão implementados mecanismos para tratar situações como:

- ⚠️ Livro não encontrado
- ⚠️ Dados inválidos
- ⚠️ ID inexistente
- ⚠️ Erros de comunicação com o banco
- ⚠️ Dados obrigatórios não informados

### 🧪 Testes

Serão realizados testes das principais operações do CRUD para verificar o funcionamento da API.

### 🎯 Objetivo

Ao final desta etapa teremos uma **API REST completa para gerenciamento de livros**.

---

## 🟣 Etapa 4 · Front End

Na última etapa será desenvolvida uma interface web para consumir a API criada nas etapas anteriores.

### 🎨 Tecnologias

- 🌐 HTML5
- 🎨 CSS3
- ⚡ JavaScript
- 🔌 Fetch API
- 📡 API REST

### Funcionalidades

#### ➕ Cadastro

Formulário para inserir novos livros no sistema.

#### 📚 Listagem

Exibição dos livros cadastrados no banco de dados.

#### ✏️ Edição

Possibilidade de alterar os dados de um livro existente.

#### 🗑️ Exclusão

Possibilidade de remover um livro do sistema.

### 🎯 Objetivo

Integrar o **Front End desenvolvido em HTML, CSS e JavaScript** com a **API FastAPI**, criando uma aplicação web funcional.

---

# 📂 Estrutura esperada

Ao longo do desenvolvimento, o projeto deverá assumir uma estrutura semelhante a:

```text
sistema-biblioteca/
│
├── 📁 backend/
│   │
│   ├── 📄 main.py
│   ├── 📄 database.py
│   ├── 📄 models.py
│   ├── 📄 schemas.py
│   │
│   └── 📁 routers/
│       └── 📄 livros.py
│
├── 📁 frontend/
│   │
│   ├── 📄 index.html
│   ├── 📄 style.css
│   └── 📄 script.js
│
├── 📄 requirements.txt
├── 📄 .gitignore
└── 📄 README.md
```

> A estrutura poderá ser modificada durante o desenvolvimento conforme as necessidades do projeto.

---

# 🗃️ Banco de dados

O projeto utilizará o **MySQL** como sistema gerenciador de banco de dados.

### Banco utilizado

```text
biblioteca_db
```

### Entidade principal

```text
Livro
```

A estrutura definitiva da tabela será definida durante a **Etapa 2**.

---

# 🔌 API REST

A API será responsável pela comunicação entre o Front End e o banco de dados.

```text
Frontend
   │
   │ HTTP
   ▼
FastAPI
   │
   │ SQL
   ▼
MySQL
```

Os dados serão enviados e recebidos utilizando o formato **JSON**.

Exemplo:

```json
{
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano": 1899
}
```

---

# 🛠️ Instalação

## 1️⃣ Clonar o repositório

```bash
git clone URL_DO_REPOSITORIO
```

## 2️⃣ Entrar no diretório

```bash
cd sistema-biblioteca
```

## 3️⃣ Criar ambiente virtual

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

## 4️⃣ Instalar as dependências

```bash
pip install -r requirements.txt
```

---

# ▶️ Executando a API

A partir da pasta do Back End:

```bash
uvicorn main:app --reload
```

A API estará disponível em:

```text
http://localhost:8000
```

### 📖 Documentação automática

O FastAPI disponibiliza automaticamente uma interface para testar os endpoints.

**Swagger UI:**

```text
http://localhost:8000/docs
```

**ReDoc:**

```text
http://localhost:8000/redoc
```

---

# 🧪 Testando a aplicação

Durante o desenvolvimento poderão ser utilizadas ferramentas como:

- 🔵 Swagger UI
- 📮 Postman
- 🌐 Navegador
- 💻 Front End da aplicação

Os testes serão realizados progressivamente a cada etapa.

---

# 📈 Evolução do projeto

| Etapa | Status | Resultado |
|---|---|---|
| 🟢 Etapa 1 | ⬜ | Fundação da aplicação |
| 🔵 Etapa 2 | ⬜ | Modelo e consultas |
| 🟠 Etapa 3 | ⬜ | CRUD completo |
| 🟣 Etapa 4 | ⬜ | Front End |

---

# 🎓 Objetivos educacionais

Ao desenvolver este projeto, os estudantes terão contato prático com:

- 🐍 Desenvolvimento de aplicações Web com Python
- ⚡ Construção de APIs REST com FastAPI
- 🗄️ Persistência de dados utilizando MySQL
- 🔄 Operações CRUD
- 📦 Organização de projetos
- 🔌 Comunicação entre Front End e Back End
- 📡 Requisições HTTP
- 📋 Manipulação de dados JSON
- 🧪 Testes de APIs
- 🌐 Desenvolvimento de interfaces Web
- 🔀 Versionamento utilizando Git e GitHub

---

# 👨‍💻 Disciplina

**SW-II · Sistemas Web II**

**ETEC Professora Maria Cristina Medeiros**

Projeto desenvolvido com finalidade **didática e educacional**, acompanhando de forma incremental as principais etapas de construção de uma aplicação Web.

---

## ⭐ Proposta do projeto

> **Do banco de dados à interface Web: construindo uma aplicação completa passo a passo.**

Cada etapa acrescenta uma nova camada ao sistema, permitindo compreender não apenas **como programar**, mas também **como as diferentes tecnologias de uma aplicação Web se comunicam**.

---

## 📌 Status

🚧 **Projeto em desenvolvimento**

```text
Etapa 1  ███████░░░  Fundação
Etapa 2  ░░░░░░░░░░  Modelo e consultas
Etapa 3  ░░░░░░░░░░  CRUD completo
Etapa 4  ░░░░░░░░░░  Front End
```
