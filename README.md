# Teste de Estagiários da talentos

Neste teste, exploramos a implementação de operações CRUD (Create, Read, Update, Delete) utilizando TypeScript e Express para uma estrutura de dados de Posts. Cada Post é composto por um nome, uma descrição e uma categoria.

Toda a informação será guardada em memória sem a necessidade do uso de banco de dados

## Tecnologias utilizadas
- TypeScript: Uma linguagem de programação que adiciona recursos de tipagem estática ao JavaScript.
- Express: Um framework minimalista para criação de aplicativos web em Node.js.

## Estrutura de Dados
A estrutura de dados utilizada neste teste é composta pelos seguintes campos:

- `id` (string): Identificador único do post.
- `nome` (string): Nome do post.
- `descricao` (string): Descrição do post.
- `categoria` (string): Categoria do post.

## Rotas e Funcionalidades

O servidor Express é configurado com as seguintes rotas e funcionalidades:

1. **GET /posts**: Retorna todos os posts existentes.
2. **GET /posts/:id**: Retorna um post específico com base no seu ID.
3. **POST /posts**: Cria um novo post.
4. **PUT /posts/:id**: Atualiza um post existente com base no seu ID.
5. **DELETE /posts/:id**: Exclui um post existente com base no seu ID.

As informações necessárias para cada rota são enviadas através do corpo da requisição, no formato JSON.

## Exemplo de Uso

A seguir, apresentamos um exemplo de como utilizar as rotas para realizar operações CRUD nos posts:

### GET /posts

**Descrição**: Retorna todos os posts existentes.

**Exemplo de requisição**: 

```http
GET /posts
```

**Exemplo de resposta**:

```json
[
  {
    "id": "1",
    "nome": "Post 1",
    "descricao": "Descrição do Post 1",
    "categoria": "Categoria 1"
  },
  {
    "id": "2",
    "nome": "Post 2",
    "descricao": "Descrição do Post 2",
    "categoria": "Categoria 2"
  }
]
```

### POST /posts

**Descrição**: Cria um novo post.

**Exemplo de requisição**:

```http
POST /posts
Content-Type: application/json

{
  "nome": "Novo Post",
  "descricao": "Descrição do Novo Post",
  "categoria": "Nova Categoria"
}
```

**Exemplo de resposta**:

```json
{
  "id": "3",
  "nome": "Novo Post",
  "descricao": "Descrição do Novo Post",
  "categoria": "Nova Categoria"
}
```

### PUT /posts/:id

**Descrição**: Atualiza um post existente com base no seu ID.

**Exemplo de requisição**:

```http
PUT /posts/1
Content-Type: application/json

{
  "nome": "Post Atualizado",
  "descricao": "Descrição Atualizada",
  "categoria": "Categoria Atualizada"
}
```

**Exemplo de resposta**:

```json
{
  "id": "1",
  "nome": "Post Atualizado",
  "descricao": "Descrição Atualizada",
  "categoria": "Categoria Atualizada"
}
```

### DELETE /posts/:id

**Descrição**: Exclui um post existente com base no seu ID.

**Exemplo de requisição
