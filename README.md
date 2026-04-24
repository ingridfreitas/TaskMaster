# 📝 Sistema de Gerenciamento de Tarefas

Este projeto é uma aplicação web simples de gerenciamento de tarefas, desenvolvida com **JavaScript puro**, utilizando o **json-server (db.json)** como base de dados fake e hospedada na **Vercel**.
Para a segunda parte do projeto, asseguramos que teremos uma API real e um banco de dados completo.

## 🚀 Funcionalidades

A aplicação possui três principais áreas:

### 🔐 Tela de Login

* Autenticação via **e-mail e senha**
* Diferenciação de acesso entre **usuário comum** e **administrador**

---

### 👤 Área do Usuário

O usuário comum possui acesso restrito às suas próprias tarefas:

* 📋 Visualizar tarefas atribuídas a ele
* ➕ Criar novas tarefas (somente para si mesmo)
* 🔄 Atualizar o status das suas tarefas

---

### 🛠️ Área do Administrador

O Administrador possui controle total do sistema, com acesso a quatro abas principais:

#### 📌 Lista de Tarefas

* Visualização de todas as tarefas
* Identificação de qual usuário cada tarefa está atribuída

#### 👥 Usuários

* Visualização de todos os usuários cadastrados

#### ✅ Minhas Tarefas

* Acesso às tarefas atribuídas ao próprio administrador

#### 📶 Filtros

* Acesso aos filtros para verificar tarefas

---

## 🔒 Regras de Negócio

* Apenas o **administrador** pode:

  * Criar novos usuários
  * Atribuir tarefas para outros usuários

* O **usuário comum**:

  * Só pode criar tarefas para si mesmo
  * Só pode alterar o status das suas próprias tarefas

---

## 🧪 Tecnologias Utilizadas

### 🎨 Frontend
* HTML5
* CSS3
* JavaScript (Vanilla JS)

### ⚙️ Backend
* Node.js
* Express.js
* JSON Server
* FS (File System)
* Path

### ☁️ Deploy
* Vercel

---

## 🖥️ Backend

A aplicação possui um backend desenvolvido com **Node.js** e **Express.js**, responsável pelo processamento das requisições e gerenciamento dos dados.

O sistema utiliza os módulos nativos **fs** e **path** para manipulação de arquivos, adotando um arquivo `db.json` como banco de dados simples para persistência local, sem a necessidade de um banco externo.

### 📦 Modelagem de Dados

Foram criadas classes internas para organização das entidades do sistema:

* **Usuario**
* **Task**

Essas classes ajudam a estruturar e padronizar os dados manipulados pela aplicação.

### 🔗 API REST

O backend disponibiliza uma API REST com as seguintes funcionalidades:

* 🔐 Autenticação
  * Login
  * Recuperação de senha

* 👤 Usuários
  * Criar usuários (admin)
  * Listar usuários
  * Atualizar dados
  * Remover usuários

* 📋 Tarefas
  * Criar tarefas
  * Listar tarefas
  * Atualizar tarefas
  * Deletar tarefas

---

## ⚙️ Como Executar o Projeto Localmente

### 1. Clone o repositório

```bash
git clone https://github.com/ingridfreitas/TaskMaster.git
```

### 2. Instale os pacotes de dependências

```bash
npm install
```

### 3. Inicie o servidor

```bash
node server.js
```

### 4. Execute o projeto

Abra o link `http://localhost:3000` no navegador

---

## 🌐 Deploy

O projeto está configurado para deploy na **Vercel**.

Pode realizar os testes nesse link aqui:
[task-master.vercel.app/](https://task-master-six-rho.vercel.app/)

Lembrando que para o site funcionar, o `node server.js` deverá estar rodando localmente.

---

## 🔑 Credenciais para Teste

### 👤 Usuário Comum

* **E-mail:** [lara@unisagrado.com](mailto:lara@unisagrado.com)
* **Senha:** Lara@123

### 🛠️ Administrador

* **E-mail:** [iindyh@unisagrado.com](mailto:iindyh@unisagrado.com)
* **Senha:** Indy@123

---

## 📁 Estrutura do Projeto

```
📦 projeto
 ┣ 📂 administrador
 ┣ 📂 usuario
 ┣ 📂 tarefa
 ┣ 📄 index.html
 ┣ 📄 style.css
 ┣ 📄 login.css
 ┣ 📄 login.js
 ┣ 📄 server.js
 ┣ 📄 usuarioclass.js
 ┣ 📄 db.json
 ┗ 📄 README.md
```

---

## 💡 Observações

* Este projeto iniciou com uma API fake utilizando `json-server` e evoluiu para um backend próprio com Node.js e Express.
* Desenvolvido para fins de estudo e prototipação.

---

## 💻 Responsáveis pelo Projeto:

* ANDRÉ AZENHA NANNI
* GEOVANA MOREIRA DE OLIVEIRA
* INGRID HELOISE DOS SANTOS FREITAS
* KELVIN KLEYN SANTOS GRECIA
* LARA FERNANDA CRUZ DE LIMA
* LETICIA ISABELA DE OLIVEIRA
* RAFAEL CHUN LIN CHEN
* RIAN CAIO FUZINELLI
* SARA VILA REAL DA SILVA
* VITOR HUGO CASALE DE FREITAS
