# MVC
Atividade sobre Arquitetura MVC

# Instalação do Node.js e Express

## 1. Instalando o Node.js no Projeto

Se você já tem o Node.js instalado no seu sistema, pode inicializar um projeto diretamente pelo terminal.

### Passo 1: Criar um diretório do projeto

No terminal, crie e acesse o diretório do projeto:

```sh
mkdir meu-servidor
cd meu-servidor
```

### Passo 2: Inicializar um projeto Node.js

Dentro do diretório, execute:

```sh
npm init -y
```

Isso criará um arquivo `package.json` com as configurações do projeto.

### Passo 3: Instalar o Express

Para instalar o Express no projeto, execute:

```sh
npm install express
```

Isso adicionará o Express como dependência do projeto.

---

## 2. Criando um Servidor com Express

### Passo 1: Criar o servidor

Crie um arquivo `server.js` e adicione o seguinte código:

```js
const express = require('express');
const app = express();
const PORT = 3000;

app.get('/', (req, res) => {
    res.send('Olá, mundo! Seu servidor Express está rodando!');
});

app.listen(PORT, () => {
    console.log(`Servidor rodando em http://localhost:${PORT}`);
});
```

### Passo 2: Executar o servidor

No terminal, execute:

```sh
node server.js
```

Agora, acesse `http://localhost:3000` no navegador para ver a resposta do servidor.

---

## 3. Executando com Nodemon (Opcional)
Para reiniciar automaticamente o servidor ao fazer alterações, instale o Nodemon como dependência de desenvolvimento:

```sh
npm install --save-dev nodemon
```

Em seguida, adicione um script no `package.json` para facilitar a execução:

```json
"scripts": {
  "start": "node server.js",
  "dev": "nodemon server.js"
}
```

Agora, para rodar o servidor com Nodemon, execute:

```sh
npm run dev
```

Sempre que você salvar alterações no código, o servidor será reiniciado automaticamente!

---

