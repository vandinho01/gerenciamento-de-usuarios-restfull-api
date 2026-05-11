# Client-Server

Aplicação Node.js com Express que consome uma API RESTful de usuários.

## Tecnologias

- **Node.js**
- **Express** — framework web
- **EJS** — template engine para renderização das views
- **Morgan** — logger de requisições HTTP
- **Cookie Parser** — manipulação de cookies
- **Restify Clients** — cliente HTTP para consumo da API

## Estrutura do Projeto

```
client-server/
├── bin/
│   └── www             # Ponto de entrada, sobe o servidor
├── public/             # Arquivos estáticos (CSS, JS, imagens)
├── routes/
│   ├── index.js        # Rota principal
│   └── users.js        # Rotas de usuários
├── views/              # Templates EJS
├── app.js              # Configuração do Express
└── package.json
```

## Instalação

```bash
npm install
```

## Executando

```bash
npm start
```

O servidor sobe na porta definida em `bin/www` (padrão: **3000**).

## Rotas

| Método | Rota      | Descrição                  |
|--------|-----------|----------------------------|
| GET    | `/`       | Página inicial             |
| GET    | `/users`  | Lista todos os usuários    |

## Tratamento de Erros

- Requisições para rotas inexistentes retornam **404**
- Erros internos retornam **500**
- Em ambiente de desenvolvimento, o stack trace é exibido na página de erro
