Пример запроса данных по описанной схеме:

```graphql
query ($id: String!) {
  client: getClientsId(id: $id) {
    age
    name
  }
  documents: getClientsIdDocuments(id: $id) {
    type
    number
  }
  relatives: getClientsIdRelatives(id: $id) {
    name
    relationType
  }
}
```

Пример ответа:

```json
{
  "data": {
    "client": {
      "age": 30,
      "name": "Ivan Petrov"
    },
    "documents": [
      {
        "type": "passport",
        "number": "1111 223344"
      }
    ],
    "relatives": [
      {
        "name": "Irina Petrova",
        "relationType": "sister"
      }
    ]
  }
}
```
