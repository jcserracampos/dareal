# Da Real

Este é um projeto que visa criar uma plataforma de compartilhamento e discussão de notícias da internet.


## Instalação inicial

* Clone este projeto

* Instale a versão 2.7.0 (Recomendo usar um gerenciador de versão como o RBENV)

* Instale o Node.js
    ```sh
    Fedora: sudo yum install nodejs
    Ubuntu: sudo apt-get install nodejs
    OSX: brew install nodejs
    ```

* Execute o bundler para instalar as dependências:

    ```sh
    $ bundle
    ```
* Crie um banco MySQL com username e password e preencha as variáveis em
`config/database.yml`.  Você também precisará de um banco de testes.

    ```yaml
    development:
      adapter: mysql2
      encoding: utf8mb4
      reconnect: false
      database: lobsters_dev
      socket: /tmp/mysql.sock
      username: *dev_username*
      password: *dev_password*

    test:
      adapter: mysql2
      encoding: utf8mb4
      reconnect: false
      database: lobsters_test
      socket: /tmp/mysql.sock
      username: *test_username*
      password: *test_password*
    ```

* Carregue o esquema do banco de dados.

    ```sh
    $ rails db:schema:load
    ```

* Coloque o seu CSS em `app/assets/stylesheets/local`.

* Popule o banco de dados com algumas seeds:

    ```sh
    $ rails db:seed
    ```

* Para desenvolvimento, use o comando fake_data para gerar dados falsos. Depois suba o servidor.
  Você poderá logar em `http://localhost:3000` com seu usuário `test`:

    ```sh
    $ rails fake_data
    $ rails server
    ```
## Como contribuir

Faça um fork deste projeto e submeta um PR.