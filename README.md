<p align="center">
  <img width="460" src="https://github.com/sethwololo/gofinances/blob/master/docs/img/logo.svg">
</p>

GoFinances é uma aplicação para gerenciamento de finanças que permite a importação e exibição de transações, assim como as entradas, saídas e um total  

## Instalação

+ Clone o repositório ou baixe-o como .zip

### Back-end
+ Rode o comando **yarn** para baixar as dependências
```bash
cd backend
yarn
```
+ Crie um banco de dados Postgres com o nome **gofinances** (e um **gofinances_tests** para rodar testes)
+ Altere as credenciais de acesso ao banco de dados no arquivo **ormconfig.json** caso seja necessário
```json
  "type": "postgres",
  "host": "localhost",
  "port": 5432,
  "username": "postgres",
  "password": "docker",
```
+ Para iniciar a aplicação, rode o comando **yarn dev:server**
```bash
yarn dev:server
```
+ A aplicação executará em **http://localhost:3333**
### Front-end
+ Rode o comando **yarn** para baixar as dependências
```bash
cd frontend
yarn
```
+ Para iniciar a aplicação, rode o comando **yarn dev:server**
```bash
yarn start
```
+ A aplicação executará em **http://localhost:3000** e abrirá automaticamente
![Logo](https://github.com/sethwololo/gofinances/blob/master/docs/img/GoFinances.png)
## Importando transações através de um arquivo *.csv*

+ Navegue até a aba **Importar**
+ Selecione o arquivo ou arraste-o até a área de importação
![Tela de Importação](https://github.com/sethwololo/gofinances/blob/master/docs/img/GoFinancesImport.png)

O arquivo a ser importado deve ter o seguinte formato:
```json
title, type, value, category
Lucros, income, 10000, Trabalho
Compras do mês, outcome, 60, Alimentação
```
