Livros Vai na Web FullStack
Este é um projeto full-stack para gerenciamento e doação de livros, composto por dois componentes principais: um front-end em React.js e uma API back-end em Flask.

Estrutura do Projeto
O projeto está organizado como um monorepo usando submódulos Git:

Livros_Vai_na_Web: Frontend desenvolvido em React.js
VaiNaAPI: Backend desenvolvido em Flask
Frontend - Livros Vai na Web
Descrição
Interface de usuário para navegação, visualização de livros doados e registro de novas doações.

Tecnologias Utilizadas
React.js: Framework JavaScript para a criação de interfaces de usuário
React Router: Biblioteca para navegação entre páginas
SCSS: Para estilização avançada com modularidade
Axios: Para comunicação com a API
Vite: Como bundler e ferramenta de desenvolvimento
Componentes Principais
Header: Navegação e barra de busca
Footer: Informações de contato e redes sociais
Páginas:
Início: Apresentação e motivação do projeto
Livros Doados: Exibição dos livros já doados
Quero Doar: Formulário para cadastrar novas doações
Backend - VaiNaAPI
Descrição
API REST para cadastro e consulta de livros, desenvolvida com Flask e SQLite.

Tecnologias Utilizadas
Flask: Framework web para Python
SQLite: Banco de dados leve e embarcado
Flask-CORS: Para permitir requisições cross-origin
Poetry/pip: Para gerenciamento de dependências
Endpoints Principais
/: Página inicial com documentação
/doar: Endpoint para cadastro de livros (POST)
/livros: Endpoint para listagem de livros (GET)
Configuração do Ambiente de Desenvolvimento
Pré-requisitos
Node.js (v22 ou superior)
Python (v3.9 ou superior)
Git (para gerenciar submódulos)

## Clonando o Repositório

```bash
# Clone o repositório principal com submódulos
git clone --recurse-submodules https://github.com/seu-usuario/Livros_Vai_na_Web_FullStack.git
cd Livros_Vai_na_Web_FullStack

# Se você já clonou sem submódulos, execute:
git submodule update --init --recursive
```

## Configurando o Frontend

```bash
# Entre no diretório do frontend
cd Livros_Vai_na_Web

# Instale as dependências
npm install
# ou
yarn install

# Inicie o servidor de desenvolvimento
npm run dev
# ou
yarn dev
```

## Configurando o Backend

```bash
# Entre no diretório do backend
cd VaiNaAPI

# Opção 1: Usando pip
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
pip install -r requirements.txt

# Opção 2: Usando Poetry
poetry install

# Execute o servidor de desenvolvimento
python src/app.py
```

Integração Frontend-Backend
O frontend se comunica com o backend através de requisições HTTP. A conexão está configurada nos seguintes arquivos:

QueroDoar.jsx: Para envio de novos livros
LivrosDoados.jsx: Para obtenção da lista de livros
URL da API em produção: https://vainaapi.onrender.com

## Compilação para Produção

### Frontend

```bash
cd Livros_Vai_na_Web
npm run build
# ou
yarn build
```

### Backend

```bash
cd VaiNaAPI
gunicorn -w 4 src.app:app
```

Estrutura do Banco de Dados
O backend utiliza SQLite com a seguinte tabela:


Contribuição
Faça um fork do projeto
Crie sua feature branch: git checkout -b feature/nova-funcionalidade
Commit suas mudanças: git commit -m 'Adiciona nova funcionalidade'
Push para a branch: git push origin feature/nova-funcionalidade
Envie um Pull Request