
## Como Testar os Endpoints

Abra o terminal na raiz do projeto e execute o comando `mvn clean install`.
Após a compilação bem-sucedida, execute a aplicação.
A seguir, você pode escolher um dos caminhos:

**Swagger**

1. Com a aplicação em execução, abra um navegador web e acesse a URL http://localhost:8080/swagger-ui/index.html#.
2. Para testar um endpoint, clique nele, preencha os parâmetros ou corpo da requisição necessários e clique em "Try it out!".

**Postman**

1. Abra o Postman.
2. Clique em "New" e depois em "Request".
3. Digite a URL do endpoint que você deseja testar no campo de texto URL.
4. Selecione o método HTTP apropriado (GET, POST, PUT, DELETE, etc.).
5. Se necessário, adicione parâmetros, corpo da requisição e cabeçalhos.
6. Clique em "Send" para enviar a requisição.

### **Criar Tarefa (POST)**

- Endpoint: `http://localhost:8080/tasks/create`
- Corpo da Requisição (JSON):

    ```json
      {
        "title": "Tarefa",
        "description": "Essa é a descrição da tarefa",
        "completed": false,
        "dateOfConclusion": "2024-03-22"
      }
     ```

### **Listar Todas as Tarefas (GET)**

- Endpoint: `http://localhost:8080/tasks/list`

### **Atualizar Tarefa Existente (PUT)**

- Endpoint: `http://localhost:8080/tasks/update`
- Corpo da Requisição (JSON):

     ```json
      {
        "id": "1",
        "title": "Tarefa",
        "description": "Essa é a descrição da tarefa",
        "completed": false,
        "dateOfConclusion": "2024-03-22"
      }
     ```

### **Deletar Tarefa por ID (DELETE)**

- Endpoint: `http://localhost:8080/tasks/delete/{id}`
- Substitua `{id}` pelo ID da tarefa que deseja deletar.
  
Certifique-se de substituir `http://localhost:8080` pela URL correta da sua aplicação, se necessário.
