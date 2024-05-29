# TC_Embrapa

TC_Embrapa é uma API que coleta dados do site da Embrapa e permite que os usuários visualizem esses dados em diversos tipos de gráficos.

## Descrição

TC_Embrapa é uma API desenvolvida com FastAPI que oferece endpoints para autenticação de usuários, registro e visualização de dados obtidos do site da Embrapa. Os dados podem ser visualizados em diferentes formatos de gráficos, facilitando a análise e interpretação das informações.

## Contribuidores

- Jorge Kayodê Lima Trindade
- Octávio Ruiz Thomas

## Instalação

### Pré-requisitos

- Python 3.7 ou superior
- SQLite

### Passos para instalação

1. Clone o repositório:
    ```bash
    git clone https://github.com/RedCanister/TC_Embrapa.git
    cd tc_embrapa
    ```

2. Crie um ambiente virtual:
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows use `venv\Scripts\activate`
    ```

3. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

4. Configure o banco de dados:
    ```bash
    python -c "from utils.make import engine; from sqlalchemy import MetaData; metadata = MetaData(bind=engine); metadata.create_all()"
    ```

5. Inicie a aplicação:
    ```bash
    uvicorn main:app --reload
    ```

## Uso

## Endpoints principais

- `GET /`: Redireciona para a página de login.
- `GET /page`: Retorna a página de login.
- `GET /cadastro`: Retorna a página de cadastro.
- `POST /register`: Registra um novo usuário.
- `POST /login`: Realiza login de usuário.
- `GET /producao`: Visualiza dados de produção.
- `GET /processamento`: Visualiza dados de processamento.
- `GET /comercializacao`: Visualiza dados de comercialização.
- `GET /importacao`: Visualiza dados de importação.
- `GET /exportacao`: Visualiza dados de exportação.

## Funcionalidades

- Autenticação de usuário com JWT.
- Registro de novos usuários.
- Login de usuários registrados.
- Visualização de dados extraídos do site da Embrapa em diferentes formatos de gráficos.

## Licença

Este projeto está licenciado sob a Licença MIT.
