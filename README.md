<h3 align="center">
  Desafio: Conceitos do Node.js
</h3>

## Sobre o desafio
Nesse desafio, foi criado uma aplicação Node.js que permite criar, listar, atualizar e remover dados dos repositórios, e além disso permite que os repositórios possam receber "likes".
 
**Observação**Este desafio está utilizando o gerenciador de pacotes **yarn**, sendo assim para instalar todas as dependências é necessário dar o comando `yarn` no terminal.

### Rotas da aplicação

Abaixo as rotas que foram criadas para atender o desafio.

- **`POST /repositories`**: A rota deve receber `title`, `url` e `techs` dentro do corpo da requisição. Ao cadastrar um novo projeto, ele deve retornar objeto no seguinte formato: `{ id: "uuid", title: 'Desafio Node.js', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }`;

- **`GET /repositories`**: Rota que lista todos os repositórios;

- **`PUT /repositories/:id`**: Rota que irá alterar o `title`, a `url` e as `techs` do repositório que possua o `id` igual ao `id` presente nos parâmetros da rota;

- **`DELETE /repositories/:id`**: Rota que irá deletar o repositório com o `id` presente nos parâmetros da rota;

- **`POST /repositories/:id/like`**: Rota que irá aumentar o número de likes do repositório específico escolhido através do `id` presente nos parâmetros da rota, a cada chamada dessa rota, o número de likes é aumentado em 1;