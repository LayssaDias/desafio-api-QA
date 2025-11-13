# 🧪 Desafio de Avaliação Prática: Testes Automatizados de API (ServeRest)

Este projeto contém a solução para o desafio de testes automatizados de API utilizando a plataforma pública de testes [ServeRest](https://serverest.dev/).

## 🎯 Objetivo

O objetivo deste projeto é avaliar a capacidade de configurar, desenvolver e executar testes automatizados para endpoints de uma API REST, cobrindo cenários de sucesso, falha e validação para os principais recursos.

## ⚙️ Tecnologias Utilizadas

* **Framework:** Cypress
* **Linguagem:** TypeScript
* **Plataforma de Teste:** ServeRest (https://serverest.dev/)

---

## 🚀 Configuração e Instalação

Siga os passos abaixo para configurar o ambiente e executar os testes:

### Pré-requisitos

Você precisa ter o **Node.js** e o **npm** (ou Yarn) instalados em sua máquina.

### 1. Clonar o Repositório

```bash
git clone [https://www.youtube.com/watch?v=JkO7GvqS6Xw](https://www.youtube.com/watch?v=JkO7GvqS6Xw)
cd desafio-api-qa
2. Instalar DependênciasInstale todas as dependências do projeto listadas no package.json:Bashnpm install
# ou
yarn install
📝 Estrutura do ProjetoA estrutura do projeto segue as convenções do Cypress, com arquivos de teste separados por recurso (e2e), dados de teste em fixtures e funções de requisição centralizadas em um API Helper.Pasta/ArquivoFunçãocypress/support/apiHelper.tsCentraliza todas as requisições HTTP (POST, GET, DELETE) para a ServeRest.cypress/fixtures/users.jsonContém a massa de dados estática (ex: credenciais do administrador).cypress/e2e/usuarios.cy.tsTestes para o endpoint de Cadastro e Busca de Usuários.cypress/e2e/login.cy.tsTestes para o endpoint de Autenticação e Login.cypress/e2e/produtos.cy.tsTestes para o endpoint de Cadastro e Listagem de Produtos.cypress/e2e/carrinhos.cy.tsTestes para o endpoint de Criação e Finalização de Carrinhos.▶️ Como Executar os TestesVocê pode executar os testes em modo interativo ou em modo headless (terminal).1. Modo Interativo (Cypress UI)Para abrir a interface gráfica do Cypress e selecionar a suíte de testes que deseja executar:
Bash
npx cypress open
2. Modo Headless (Terminal)Para rodar todos os testes no terminal e gerar um relatório de execução:Bashnpx cypress run
✅ Cenários de DestaqueOs testes cobrem os seguintes cenários importantes, focando na robustez e unicidade dos dados:Unicidade de Dados: O cadastro de usuários utiliza dados dinâmicos (Date.now()) para evitar colisões e garantir que o teste de sucesso seja executado corretamente, mesmo com execuções repetidas.Setup e Teardown: Os testes de produtos.cy.ts e carrinhos.cy.ts garantem a criação e autenticação de um usuário administrador no hook before antes de tentar criar recursos protegidos.Validação de Erros: Cenários de falha (ex: login inválido, e-mail duplicado) validam tanto o Status Code (400, 401) quanto as mensagens de erro específicas da API.
