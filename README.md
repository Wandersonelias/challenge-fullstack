# Challenge para desenvolvedor Full Stack Tributei

O objetivo deste desafio é avaliarmos o seu domínio em desenvolvimento fullstack, ou seja, sua organização, boas práticas com o código, criação e consumo de APIs Restfull, conhecimento dos frameworks e tecnologias utilizadas.

Um layout final bem elaborado e desenhado aponta para um diferencial seu, mas não é necessário se preocupar muito com o design. Afinal, não estamos buscando um designer para essa vaga! 

## Regras

1. Todo o seu código deve ser disponibilizado num repositório público ou privado em seu github ou bitbucket pessoal. Envie o link para (96) 992076582 no prazo de 3 dias a contar de 19/09/2021 para a entreaga deste desafio;
2. Desenvolver o projeto utilizando: 
    - Nodejs
    - Express
    - Mysql
    - Sequelize
    - Frontend: React, Vue ou um framework de sua escolha
    - HTML e CSS (ou algum pré-processador)
    - [Google Geocode API](https://developers.google.com/maps/documentation/geocoding/intro?hl=pt-br) (se precisar de uma API Key do Google, basta solicitar por e-mail)
    - [Leaflet](http://leafletjs.com/) para manipulação do mapa. O mapa a ser utilizado pode ser qualquer um (Google, Mapbox, OSM, etc).


## O Desafio

Este é o layout que deverá ser produzido:
![layout](challenge.png)

## Especificação das funcionalidades

Ao finalizar o desafio, o usuário deverá estar habilitado a cadastrar os clientes no formulário, e ao salvar, atualizar o mapa com o ponto (pin) daquele cadastro e a tabela com os dados do cliente. Na tabela deverá conter um botão para excluir o cliente, que deverá removê-lo do banco, mapa e tabela.
Obs. as informações enviadas via API tambem deveram aparecer atualizadas no frontend
#### POST /deliveries

Você deve fazer um cadastro de entregas, que terá os seguintes campos:
1. Nome do cliente
2. Peso em kg
3. Endereço
    - Logradouro
    - Número
    - Bairro
    - Complemento
    - Cidade
    - Estado
    - País
    - Geolocalização
        - Latitude
        - Longitude

Estes dados devem ser salvos numa tabelas deliveries no banco Mysql.
Note que no formulário há apenas um campo para colocar o endereço. Isso se deve ao fato de que o usuário deverá preencher apenas uma linha de endereço. Ao clicar em **Buscar**, os dados deste campo devem ser enviados à API do Google para buscar as informações de localização e incorporados ao objeto da delivery. Neste ponto, os campos de latitude e longitude devem ser preenchidos, mas devem ficar como _disabled_. Ao clicar em **Salvar**, salva os dados no banco, limpa o formulário e atualiza o mapa e a tabela. O botão **Resetar Cadastro** deve limpar a base de deliveries, tabela e pontos do mapa.

#### GET /deliveries

A requisição GET para /deliveries deve trazer um json com as informações das deliveries que existem no banco e exibí-las no mapa e na tabela.

#### DELETE /deliveries

Há um botão na tabela para excluir a delivery. Ele deverá remover todos os clientes tanto do banco quanto do mapa/tabela.


### Algumas dicas e observações
> Obs 1.: Fique a vontade para utilizar qualquer 3rd party ou fonte de dados de terceiros;

> Obs 2.: Considere que todos os campos são de preenchimento obrigatório no formulário.

> Obs 3.: Considere validar os campos também na API e em caso de inconsistência retornar erro num JSON estruturado com código HTTP 400

> Obs 4. : Todo o sistema deverá tambem funcionar por meio de uma API restfull, para que os dados possam ser inseridos via requisições de api

## Dúvidas
Envie suas dúvidas diretamente para (96) 992076582 Wanderson.
