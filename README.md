# Projeto de Estudo e Piloto BackEnd em Node.Js

Este projeto consiste em criar um backend, para uma empresa de barbearia, utilizando todas as tecnologias requeridas do mercado, como redis, queue, mongoDB, postgreSQL. Esse projeto é baseado no curso Gostack do site [Rockeseat](https://rocketseat.com.br/).

# **Bibliotecas Utilizadas**

> **[Express](http://expressjs.com/)** - *yarn add express*

> **[Express-async-errors](https://github.com/davidbanham/express-async-errors#readme)** - *yarn add express-async-errors*

> **[Express-handlebars](https://github.com/ericf/express-handlebars)** - *yarn add express-handlebars*

> **[Json Web Toke](https://github.com/auth0/node-jsonwebtoken#readme)** - *yarn add jsonwebtoken*

> **[Mongoose](https://mongoosejs.com/)** - *yarn add mongoose*

> **[Multer](https://github.com/expressjs/multer#readme)** - *yarn add multer*

> **[Node Mailer](https://nodemailer.com/)** - *yarn add nodemailer*

> **[Node Mailer Express Handlebars](https://github.com/yads/nodemailer-express-handlebars)** - *yarn add nodemailer-express-handlebars*

> **[Pg](http://github.com/brianc/node-postgres)** - *yarn add pg*

> **[Pg hstore](https://github.com/scarney81/pg-hstore)** - *yarn add pg-hstore*

> **[Sequelize](https://sequelize.org/)** - *yarn add sequelize*

> **[Youch](https://github.com/poppinss/youch#readme)** - *yarn add youch*

> **[Yup](https://github.com/jquense/yup)** - *yarn add yup*

> **[Dot Env](https://github.com/motdotla/dotenv#readme)** - *yarn add dotenv*

> **[Date Fns](https://github.com/date-fns/date-fns#readme)** - *yarn add date-fns*

> **[Bee queue](https://github.com/bee-queue/bee-queue)** - *yarn add bee-queue*

> **[Bcryptjs](https://github.com/dcodeIO/bcrypt.js#readme)** - *yarn add bcryptjs*

> **[Sentry Node](https://github.com/getsentry/sentry-javascript/tree/master/packages/node)** - *yarn add @sentry/node*

# **Dependências de Desenvolvimento**

> **[Eslint Plugin](https://github.com/typescript-eslint/typescript-eslint#readme)** - *yarn add @typescript-eslint/eslint-plugin -D*

> **[Parser](https://github.com/typescript-eslint/typescript-eslint#readme)** - *yarn dev @typescript-eslint/parser - D*

> **[Eslint](https://eslint.org/)** - *yarn dev eslint -D*

> **[Nodemon](http://nodemon.io/)** - *yarn add nodemon -D*

> **[Prettier](https://prettier.io/)** - *yarn add prettier -D*

> **[Sequelize Cli](https://github.com/sequelize/cli)** - *yarn add sequelize-cli -D*

> **[Sucrase](https://github.com/alangpierce/sucrase#readme)** - *yarn add sucrase -D*

# **Inicializando o Projeto**
Para inicializar o projeto, basta utilizar o comando

> yarn install

ou

> npm install

Após instalado as dependências, para iniciar o projeto, basta digitar no terminal o seguinte comando

> yarn dev

ou

> npm dev


# **Consumindo as rotas de Api**

- **Criação de Usuário** - http://localhost:3333/users - **POST**

	    {
    		"name": "Nome do usuario",
    		"email": "emailusuario@hotmail.com",
    		"password": "password"
    	}

 - **Criar Sessão do Usuário** - http://localhost:3333/sessions - **POST**

		{
	    	"email": "emailusuario@hotmail.com"",
	    	"password": "password"
	    }

- **Atualizar o usuário**  - http://localhost:3333/users - **PUT** - Barear Token (Criado na rota sessão do usuário)

		{
    		"name": "Nome do usuario",
    		"email": "emailusuario@hotmail.com",
    		"password": "123456"
    	}

- **Enviar Arquivo de Midia** - http://localhost:3333/files - **POST** - Barear Token (Criado na rota sessão do usuário)

		Enviar como parâmetro um Multipart com cabeçalho file e o arquivo selecionado.

- **Listagem de Providers** - http://localhost:3333/providers - **GET** - Barear Token (Criado na rota sessão do usuário)

- **Deletar um Providers** - http://localhost:3333/providers/:id - **DELETE** - Barear Token (Criado na rota sessão do usuário)

- **Criar um novo Appointments** - http://localhost:3333/appointments - **POST** - Barear Token (Criado na rota sessão do usuário)

	    {
			"provider_id": 6,
			"date": "2020-01-08T20:47:00-03:00"
		}

- **Listar todos os Appointments** - http://localhost:3333/appointments - **GET** - Barear Token (Criado na rota sessão do usuário)

 - **Listar todos os Schedules** - http://localhost:3333/schedule - **GET** - Barear Token -(Criado na rota sessão do usuário)

	   Enviar no cabeçalho da requisição parâmetro date com a data no formato 2019-07-01T00:00:00-03:00

 - **Criar nova notificação** - http://localhost:3333/notifications/:idnotification - **PUT** - Barear Token -(Criado na rota sessão do usuário)

 - **Pegar todas as notificação** - http://localhost:3333/notifications/ - **GET** - Barear Token -(Criado na rota sessão do usuário)

 - **Listar Horários Vago de Providers** - http://localhost:3333/providers/:id/available - **GET** - Barear Token -(Criado na rota sessão do usuário)

       Enviar no cabeçalho da requisição parâmetro date com a data no formato 1578525622634 milissegundos



