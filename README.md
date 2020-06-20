<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Desafio 02: Conceitos do Node.js
</h3>

<blockquote align="center">“Não espere para plantar, apenas tenha paciência para colher”!</blockquote>

## Requisitos

[Node.js](https://nodejs.org/pt-br/)

# ⚙ Instalação

Instalar as dependencias:

```
yarn
```

ou

```
npm install
```

# 🚀 Executar

Nossa API Rest lista, cria, atualiza e deleta repositórios em um ambiente local.

Executar a aplicação na url http://localhost:3333:

```
yarn dev
```

ou

```
npm run dev
```

### Rotas e métodos:

- **GET**: /repositories

Essa rota retorna todos os repositórios criados na aplicação.

- **POST**: /repositories

Essa rota adiciona um novo repositório ao array local, para isso devemos passar os dados no corpo da requisição, seguindo o seguinte exemplo:

```json
{
  "title": "Conceitos NodeJS",
  "url": "http://github.com/mmouradev/conceitos-nodeJS",
  "techs": ["NodeJS", "Express"]
}
```

- **PUT**: /repositories/:id

Essa rota atualiza um repositório já cadastrado com novas informações, para isso devemos passar o **id** do repositório na URL da requisição e as informações que desejamos atualizar, conforme o exemplo:

```json
{
  "title": "Conceitos ReactJS",
  "url": "http://github.com/mmouradev/conceitos-reactJS",
  "techs": ["NodeJS", "Express"]
}
```

- **DELETE**: http://localhost:3333/repositories/:id

Essa rota deleta um repositório cadastrado, para isso devemos passar o **id** do repositório na URL da requisição.

- **POST**: http://localhost:3333/repositories/:id/like

Essa rota é utilizada para adicionar um like ao repositório selecionado pelo **id** na URL da requisição, além de retornar o repositório com o número de likes atualizado. Exemplo do retorno:

```json
{
  "id": "1a17d8ae-647d-446f-9a84-0561fb9cd28c",
  "title": "Conceitos ReactJS",
  "url": "http://github.com/mmouradev/conceitos-reactJS",
  "techs": ["NodeJS", "ReactJS"],
  "likes": 1
}
```

# 🛠 Executando os testes

A API contém testes automatizados para cada rota, para executar os testes:

```
yarn test
```

ou

```
npm run test
```
