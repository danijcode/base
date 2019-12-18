# Template Base Laravel + Angular
Projeto base utilizando Laravel 5.6 + Angular 6.0 com autenticação JWT.

- Segue descritos os passos para configurar e subir os projetos front e backend local.

## Server
- Instale o [PHP] (http://fi2.php.net/downloads.php) e um dos seguintes bancos de dados: [MySQL] (https://www.mysql.com/downloads/), [PostgreSQL] (https : //www.postgresql.org/download/), [MS SQL Server] (https://www.microsoft.com/en-us/sql-server/sql-server-downloads) ou [SQL Lite] (https : //www.sqlite.org/download.html).
- Instale [Composer](https://getcomposer.org/) e [nodeJS](https://nodejs.org).
- Vá para a pasta `Server` e execute `composer install` para instalar as dependencias do projeto.
- Defina suas conexões de banco de dados em `.env`: DB_CONNECTION (mysql, pgsql, sqlsrv, sqlite), DB_DATABASE, DB_PORT, DB_USERNAME, DB_PASSWORD. 
- Após definir as configurações de banco de dados execute `php artisan migrate` para criar a tabela e inserir um usuario.
- Para envio de e-mail, certifique-se de ter no seu arquivo .env as seguintes chaves definidas: `MAIL_DRIVER`,` MAIL_HOST`, `MAIL_PORT`,` MAIL_USERNAME`, `MAIL_PASSWORD`,` MAIL_ENCRYPTION`.

## Client
- Instale [nodeJS](https://nodejs.org)
- instale globalmente o [Angular CLI](https://cli.angular.io/) com o comando `npm install -g @angular/cli@latest` (talvez precise rodar com sudo)
- vá para a pasta *Client* e execute `npm i` para instalar as dependencias do projeto (talvez a rxjs quebre, entao sera necessario instalar essa dependencia separadamente, recomendo a versão 6.0.0 `npm install rxjs@6.0.0 --save`)
- Altere o arquivo `/Client/src/environments/environment.ts` com a url do backend
- Execute `ng serve` para subir o frontend. Navegue `http://localhost:4200/`.
- Execute `ng build -prod` em `Client` para gerar os arquivos de procução que estarão na pasta `dist/`.

## Rodando Aplicação (Desenvolvimento)
- vá para a pasta raiz do projeto e execute `npm start`

## License: [MIT](https://opensource.org/licenses/MIT)