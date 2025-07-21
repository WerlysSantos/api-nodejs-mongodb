
# 📦 API de Cadastro de Usuários

API RESTful desenvolvida com Node.js, Express e Prisma, conectada ao banco de dados MongoDB, com funcionalidades para **cadastrar, listar, atualizar e deletar usuários**.

---

## 🛠 Tecnologias Utilizadas

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)
- [Prisma ORM](https://www.prisma.io/)
- [MongoDB](https://www.mongodb.com/)
- [ESModules](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules)

---

## ⚙️ Configuração e Execução

### 1. Clone o repositório

```bash
git clone https://github.com/WerlysSantos/api-nodejs-mongodb
cd api-nodejs-mongodb
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure o acesso ao banco

Crie um arquivo `.env` com a string de conexão do MongoDB:

```
DATABASE_URL="mongodb+srv://usuario:senha@cluster.mongodb.net/banco"
```

### 4. Gere os arquivos do Prisma (caso ainda não existam)

```bash
npx prisma generate
```

### 5. Execute o servidor

```bash
node index.js
```

A aplicação estará disponível em:  
📍 `http://localhost:3000`

Caso a porta 3000 esteja em uso, altere para uma outra livre em seu computador

---

## 📌 Endpoints Disponíveis

### 🔹 POST `/users`

Cria um novo usuário.

**Body JSON:**

```json
{
  "name": "João",
  "age": "30",
  "email": "joao@email.com"
}
```

**Resposta:**

<img width="1322" height="371" alt="image" src="https://github.com/user-attachments/assets/5ef03f8c-3f9a-41fc-97c7-e8234b34f9c4" />

```json
{
  "name": "João",
  "age": "30",
  "email": "joao@email.com"
}
```

---

### 🔹 GET `/users`

Lista todos os usuários ou filtra por `name`, `email` ou `age`.

**Exemplos:**

- `GET /users` → lista todos  
- `GET /users?name=joão&age=30` → filtra por nome e idade

<img width="1321" height="384" alt="image" src="https://github.com/user-attachments/assets/1d45cd0f-1d5e-427f-80d8-e320498a5af2" />

---

### 🔹 PUT `/users/:id`

Atualiza os dados de um usuário pelo `id`.

**Body JSON:**

<img width="1321" height="435" alt="image" src="https://github.com/user-attachments/assets/d8e85605-7963-4585-b304-a01122e949fc" />

```json
{
  "name": "João da Silva",
  "age": 31,
  "email": "joaosilva@email.com"
}
```

---

### 🔹 DELETE `/users/:id`

Deleta um usuário pelo `id`.

**Resposta:**

<img width="1319" height="387" alt="image" src="https://github.com/user-attachments/assets/2f67fdb0-f2d9-451b-bad8-ba7a536dca87" />

```json
{
  "message": "Usuário deletado com sucesso!"
}
```

---

## 📌 Observações Técnicas

- O projeto usa `type: module`, permitindo o uso de `import/export`.
- O Prisma está configurado para acessar um client gerado em `./generated/prisma`.
- A API está preparada para funcionar com queries (filtros) no endpoint de listagem.

---

## ✍️ Autor

Werlys Santos  
🔗 [LinkedIn](www.linkedin.com/in/werlys-santos-175b0b361)  
🐙 [GitHub](https://github.com/WerlysSantos)
