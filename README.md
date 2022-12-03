# MASTERCLASS PHP

## Criar o projeto
``composer create-project laravel/laravel projeto8``

### Requisitando a dependencia 
``composer require laravel/breeze``

### Instalando a dependencia 
``php artisan breeze:install``

### Instalando e rodando
``npm install``
``npm run dev``

### Mostrando os bancos de dados
``show databases;``

### Criando o banco de dados
``create database niveis;``

### Alterar o create user table e adicionar os niveis de acesso

## Configurar o .env

### Inserindo os registros
``php artisan migrate``

### Rodar o servidor do PHP
``php artisan serve``

### Adicionar o nivel de usuario na criação dele
### Adicionar niveis no Models\User
### Mostra as tabelas do banco
``SHOW TABLES``

### Mostra os dados do usuario logado
``{{ Auth::user()->CAMPO }}``

## Instalação do gerador de Crud
``composer require ibex/crud-generator --dev``
``php artisan vendor:publish --tag=crud``

## Cria a migration do produtos
``php artisan make:migration produto_table``
``php artisan migrate``

## Cria o crud do Produto
``php artisan make:crud produtos``

## Adiciona a route do produtos em web.php
``Route::resource('produtos', 'App\Http\Controllers\ProdutoController')->middleware(['auth']);``

### Modificar o Layout app adicionando conteudo com @yield

### Adiciona o link do bootstrap

### Pega o conteúdp do dashboard para formatar o layouts.app

## Criando a Policy do produto
``php artisan make:policy ProdutoPolicy --model=Produto``

### Adicionar o AuthServiceProvider da ProdutoPolicy

## Criar a regra do update do ProdutoPolicy
``$user->niveis == 1``

## Verificar a regra no ProdutoController no edit / update
``$this->authorize('update', $produto);``

### Adicionar as regras de niveis nos botões
``Auth::user()->niveis == 1``
