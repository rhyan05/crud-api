# API CRUD Simples

Esta é uma API simples que implementa todas as operações básicas do CRUD (Criar, Ler, Atualizar, Deletar) usando PHP e MySQL. 

## Pré-requisitos

1. **Banco de Dados**: Crie o banco de dados usando o arquivo `db_crud.sql`. Esse arquivo contém o modelo do banco de dados necessário para a API funcionar.

2. **Ferramenta para Testar APIs**: Você pode usar ferramentas como [Insomnia](https://insomnia.rest/), [Postman](https://www.postman.com/), ou [Paw](https://paw.cloud/) para testar a API.

## Estrutura do Projeto

### `index.php`

Este arquivo é responsável por gerenciar as requisições da API. Ele define qual operação será executada (`POST`, `GET`, `UPDATE`, `DELETE`) com base nos parâmetros da URL.

### `person.php`

Este arquivo contém a lógica de conexão com o banco de dados e as operações CRUD associadas ao modelo de `Person`.

## Endpoints da API

### Criar (POST)

Adiciona uma nova pessoa ao banco de dados.

**Exemplos:**
- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=create&name=João&age=30`
- Saida:
     {
     "status": "success",
     "message": "Pessoa criada com sucesso.",
     "id": 1,
     "name": João,
     "age": 30
   }
- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=create&name=Rhyan&age=19`
- Saida:
 {
  "status": "success",
  "message": "Pessoa criada com sucesso.",
  "id": 2
}

- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=create&name=Gisele&age=22`
- Saida:
  {
  "status": "success",
  "message": "Pessoa criada com sucesso.",
  "id": 3
}

### Ler (GET)

Recupera todas as pessoas ou uma pessoa específica com base no ID.

**Exemplos:**
- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=read`
- Saida:
  [
  {
    "id": 1,
    "name": "João",
    "age": 30
  },
  {
    "id": 2,
    "name": "Rhyan",
    "age": 19
  },
  {
    "id": 3,
    "name": "Gisele",
    "age": 22
  }
]

- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=read&id=1`
- Saida:
  {
  "id": 1,
  "name": "João",
  "age": 30
}

  
- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=read&id=2`
- Saida:
  {
  "id": 2,
  "name": "Rhyan",
  "age": 19
}


### Atualizar (UPDATE)

Atualiza as informações de uma pessoa existente com base no ID.

**Exemplos:**
- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=update&id=1&name=João Atualizado&age=35`
- Saida:
  {
    "status": "success",
    "message": "Pessoa atualizada com sucesso."
  }


- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=update&id=1&name=Gisele Atualizado&age=25`
- Saida:
{
  "status": "success",
  "message": "Pessoa atualizada com sucesso."
}


### Deletar (DELETE)

Remove uma pessoa do banco de dados com base no ID.

**Exemplos:**
- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=delete&id=1`
Saida:
{
    "status": "success",
    "message": "Pessoa removida com sucesso."
}

- `http://localhost/Projetos/API/apis-php/api-crud_simples/index.php?fn=read`
  [
  {
    "id": 2,
    "name": "Rhyan",
    "age": 19
  },
  {
    "id": 3,
    "name": "Gisele",
    "age": 22
  }
]


## Como Usar

1. **Configuração do Banco de Dados**: Execute o arquivo `db_crud.sql` no seu servidor MySQL para criar a tabela necessária.

2. **Configuração do Servidor PHP**: Certifique-se de que o servidor PHP está configurado e em execução.

3. **Testar a API**: Use a ferramenta de teste de APIs de sua escolha para fazer requisições para os endpoints listados.

## Contribuição

Se você encontrar problemas ou tiver sugestões para melhorias, sinta-se à vontade para abrir um "issue" ou fazer um "pull request".

