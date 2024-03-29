<h1> Daesc </h1>

> Status: desenvolvimento ⚠️

## Objetivo
* Criar um site onde seja póssivel comunicar a empresa de água da cidade (Daesc), que em determinada região ficou sem água.

### Funcionalidades 
* Melhorar a comunicação com um órgão público da cidade.
* Fazer simulações para quitar dívidas.


### Tecnologias utilizadas 
<table> 
<tr>
<td>Node.JS </td>
<td> MySql </td>
<td>javaScript </td>
<td>Bootstrap</td>
</tr>
<tr>
<td>v18.15.0</td>
<td>v6.0</td>
<td>ECMAScript 2022</td>
<td>V5.3</td>
</tr>

</table>

### Módulos utilizados no node.js
<table> 
<tr>
<td>Express</td>
<td>Express-Handlebars</td>
<td>Express-session</td>
<td>Connect-flash</td>
<td>Body-Parser</td>
<td>MySql2</td>
<td>Swagger</td>
<td>Path</td>

</tr>
<tr>
<td>4.18.2</td>
<td>7.0.4</td>
<td>1.17.3</td>
<td>0.1.1</td>
<td>1.20.2</td>
<td>7.0.3</td>
<td>4.6.2</td>
<td>1.0.0</td>
</tr>

</table>


### Modelo em alta fidelidade
* <a href = "https://www.figma.com/file/Aeboe8zfAXq3nheiBtrRKn/StoryBoard%2F%2FKau%C3%A3?node-id=0%3A1" > Figma </a> 


 ### Estrutura de Dados

* Administrador
~~~~MySql
const Administrador = MySql.sequelize.define('administrador', {

    nome: {
        type: MySql.Sequelize.STRING(30)
    },

    sobrenome: {
        type: MySql.Sequelize.STRING(40)
    },

    email: {
        type: MySql.Sequelize.STRING(50)
    },

    senha: {
        type: MySql.Sequelize.STRING(30)
    }
} , { freezeTableName: true });
~~~~

* Formulário para notificar que ficou sem água
~~~~MySql
const Reclamacao = MySql.sequelize.define('reclamacao', {

    rua: {
        type: MySql.Sequelize.STRING(50)
    },
    
    bairro: {
        type: MySql.Sequelize.STRING(50)
    },
    
    descricao: {
        type: MySql.Sequelize.STRING(150)
   
} , { freezeTableName: true });
~~~~

* Simulação para quitar um talão
~~~~MySql
const Servico = MySql.sequelize.define('servico', {

    boleto: {
        type: MySql.Sequelize.INTEGER
    },
    
    entrada: {
        type: MySql.Sequelize.INTEGER
    },
    
    parcelamento: {
        type: MySql.Sequelize.INTEGER
    }
} , { freezeTableName: true });
~~~~
