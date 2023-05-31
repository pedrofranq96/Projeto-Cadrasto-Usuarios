# Documentação do Cadastro de Usuários

## Descrição
O Cadastro de Usuários é uma aplicação web que permite o registro e visualização de usuários. A aplicação é dividida em duas partes: o backend, responsável por fornecer uma API RESTful utilizando o JSON Server e o arquivo `db.json`, e o frontend, desenvolvido com React, que consome essa API utilizando o Axios para realizar as requisições.

A aplicação foi desenvolvida utilizando as seguintes tecnologias:

Bootstrap: um framework CSS que oferece uma série de componentes e estilos prontos para serem utilizados, facilitando o desenvolvimento da interface do usuário.
React Router: uma biblioteca que permite a criação de rotas na aplicação, facilitando a navegação entre diferentes telas.
Axios: uma biblioteca para fazer requisições HTTP, utilizada para se comunicar com o servidor.
Font Awesome: uma biblioteca de ícones vetoriais que podem ser utilizados na aplicação.
JSON Server: um pacote Node.js que cria um servidor REST a partir de um arquivo JSON, utilizado para simular uma API para armazenar os dados dos usuários.
React Router DOM: uma extensão do React Router que oferece alguns componentes adicionais para trabalhar com o React e o navegador.

### Backend
O backend da aplicação é implementado utilizando o JSON Server, que fornece uma API RESTful simulada com base em um arquivo JSON. O arquivo `db.json` contém os dados dos usuários. A API RESTful oferece as seguintes rotas:

- GET `/users`: Retorna a lista de usuários cadastrados.
- POST `/users`: Adiciona um novo usuário.
- GET `/users/:id`: Retorna um usuário específico com base no ID.
- PUT `/users/:id`: Atualiza os dados de um usuário específico.
- DELETE `/users/:id`: Remove um usuário específico.

A estrutura do backend é organizada da seguinte forma:

```
Cadastro-de-usuarios/
├── backend/
  ├── db.json
  ├── package.json
  ├── package-lock.json
```
### Frontend
O frontend da aplicação é desenvolvido utilizando o React, juntamente com outras bibliotecas e tecnologias como Bootstrap, React Router, Axios e Font Awesome. O Axios é utilizado para fazer as requisições HTTP para o backend e consumir a API RESTful fornecida pelo JSON Server.

A estrutura do frontend é organizada da seguinte forma:

```
Cadastro-de-usuarios/
├── frontend/
  ├── public/
  │   ├── index.html
  ├── src/
  │   ├── components/
  │   │   ├── home/
  |   |   |  ├── Home.jsx
  │   │   ├── template/
  |   |   |  ├── Header.jsx
  |   |   |  ├── Header.css
  |   |   |  ├── Logo.jsx
  |   |   |  ├── Logo.css
  |   |   |  ├── Main.jsx
  |   |   |  ├── Main.css
  |   |   |  ├── Nav.jsx
  |   |   |  ├── Nav.css
  |   |   |  ├── Footer.jsx
  |   |   |  ├── Footer.css
  │   │   ├── template/
  |   │   │   ├── UserCrud.jsx
  │   ├── main/
  │   │   ├── App.css
  │   │   ├── App.jsx
  │   │   ├── Routes.jsx
  │   ├── index.css
  │   ├── index.js
  │   └── ...
  ├── package.json
  ├── package-lock.json
  └── ...
```

- A pasta `public/` contém o arquivo HTML principal (`index.html`) e outros arquivos estáticos necessários para a aplicação.
- A pasta `src/` contém o código-fonte da aplicação.
- A pasta `components/` contém os componentes reutilizáveis da aplicação separados por subpastas(`home`,`template` e `user`), como o cabeçalho (`Header.js`) e o formulário de usuário (`UserCrud.jsx`), entre outros.
- A pasta `main/` contém as rotas e o componente principal da aplicação, onde são definidas as rotas e o conteúdo das páginas.
- A pasta `services/` contém o arquivo `api.js`, responsável por encapsular as chamadas HTTP utilizando o Axios para se comunicar com a API RESTful fornecida pelo backend.
- O arquivo `App.js` é o componente principal da aplicação, onde são definidas as rotas e o conteúdo das páginas.
- O arquivo `index.js` é o ponto de entrada da aplicação, onde o React é inicializado e o componente `App` é renderizado.
- O arquivo `package.json` contém as informações sobre as dependências e scripts do projeto.
- O arquivo `db.json` localizado na pasta backend, local onde é armazenado o banco de dados da aplicacão.
## Instalação e Configuração

### Pré-requisitos
- Node.js e npm instalados na máquina.

###

 Backend
1. Clone o repositório do projeto do Cadastro de Usuários para o seu computador.
2. Abra o terminal e navegue até o diretório raiz do projeto.
3. Execute o seguinte comando para instalar as dependências do projeto:
   ```
   npm install
   ```
4. Execute o seguinte comando para iniciar o servidor do JSON Server e disponibilizar a API RESTful:
   ```
   cd backend
   npm start
   ```

### Frontend
1. Abra um novo terminal e navegue até o diretório raiz do projeto.
2. Execute o seguinte comando para instalar as dependências do projeto:
   ```
   npm install
   ```
3. Após a instalação das dependências, execute o seguinte comando para iniciar a aplicação:
   ```
   cd frontend
   npm start
   ```
4. A aplicação será iniciada e estará acessível no seu navegador no endereço http://localhost:3000.

## Uso da Aplicação

Ao acessar a aplicação, você será direcionado para a tela inicial (`Home`), onde poderá visualizar a mensagem de bem vindo. A partir dessa tela, é possível navegar para a tela de usuários (`Users`) para adicionar novos usuários e visualizar a lista de usuários cadastrados.

### Tela Inicial (`Home`)

- Exibe a Notaa de bem vindo.

### Tela de Usuários (`Users`)

- Exibe um formulário para adicionar um novo usuário.
- Preencha os campos obrigatórios (nome e email).
- Clique no botão "Salvar" para adicionar o usuário.
- Após adicionar o usuário com sucesso, o novo usuário será exibido na lista.

## Considerações Finais

O Cadastro de Usuários é uma aplicação web que utiliza o JSON Server como backend para fornecer uma API RESTful simulada e o React como frontend para consumir essa API através do Axios. Esperamos que essa documentação possa te auxiliar na compreensão e utilização da aplicação. Em caso de dúvidas ou problemas, não hesite em entrar em contato com a equipe responsável pelo desenvolvimento da aplicação.
