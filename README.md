[![GitHub license](https://img.shields.io/badge/implemented%20by-Andy-blue)](https://www.linkedin.com/in/andy-kiaka-76a983110/)
# Plan_Api

App que consome dados de uma API e executa as operações CRUD internamente com Postgres

## Abordagem 🔩

A idea do sistema consiste em ter uma interface gráfica (Qt5) e um SGBD (postgres) onde inicialmente o sistema efetua a
operação Read recuperando os dados de uma API pública e os salva dentro do banco de dados. O sistema permite realizar a 
operação Create, podendo criar novos dados baseado nos dados recolhidos na operação anterior. E também pode ser efetuado 
as operações de Delete e Update que vão ser explicado no próximo tópico.

## Scenário 📖

O sistema recolhe dados públicos da Api https://jsonplaceholder.typicode.com/users representando pessoas e seus meios de contato,
o scenário criado aqui se trata de fictícios clientes de um banco que podem solicitar empréstimos.
- Create : representa a operação onde o cliente solicita um novo empréstimo e um formulário é preenchido.
- Read : representa as operações listar os clientes, listar as dívidas de um clientes ou o momento que o sistema solicita os dados da API
- Update: representa a operação de alteração do valor de um determinado empréstimo
- Delete: representa a operação de deletar uma dívida

### Pré-requisitos 📋

Para o bom funcionamento deste sistema, as seguintes bibliotecas são necessárias. 
No entanto nenhuma instalação manual é requerida, tudo é feito automaticamente com o docker.

Python 3.5 ou superior

Postgresql9 ou superior

Psycopg2

PyQt5

### Instalação e Execução 🔧

#### Após baixar , descompactar e acessar a pasta com os arquivos

N.B: Esta versão foi testada somente com ubuntu e a instalação leva uns 7 min devido ao tamanho das imagens e dos containers

- Em um terminal, execute o seguinte comando para construir as imagem e os containers   
- Antes da execução é necessário ter as portas 5432, 8088 e 8080 desocupadas no host para que postgres e adminer possam funcionar

```
docker-compose up
```         

## Dados gerados 📦

* Para tornar mais comodo a visualização das operações feitas no sistema, o serviço adminer é instalado junto ao sistema, que
permite acessar postgres pelo navegador web.
* Para logar no adminer, uma vez todos os serviços estiverem funcionando, abre seu navegador preferido e digite na barra de
endereço 'localhost:8088' , uma vez feito estará na página de login do adminer. Adminer consegue se conectar a diferentes tipos
de SGBD, portanto na opção sistema, escolha 'PostgreSQL'. No campo servidor, digite 'postgres_server'. No campo usuario, digite 'debug'.
No campo senha, digite '1234' e pode deixar o campo Base de dados em branco.

## Autor ✒️

* **Andy Kiaka** - *Job Completo* - [detona115](https://github.com/detona115)

---
⌨️ com ❤️ por [detona115](https://github.com/detona115) 😊
