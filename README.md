# Yml-expressjs
npm install express
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Olá, mundo!');
});

app.listen(port, () => {
  console.log(`Servidor rodando na porta ${port}`);
});
npm install ejs
<!-- views/index.ejs -->
<!DOCTYPE html>
<html>
<head>
  <title>Minha Página</title>
</head>
<body>
  <h1>Minha Página</h1>
  <p>Essa é uma página web dinâmica!</p>
  <p>Nome: <%= nome %></p>
</body>
</html>
const express = require('express');
const app = express();
const port = 3000;

app.set('view engine', 'ejs');

app.get('/', (req, res) => {
  res.render('index', { nome: 'João' });
});

app.listen(port, () => {
  console.log(`Servidor rodando na porta ${port}`);
});
