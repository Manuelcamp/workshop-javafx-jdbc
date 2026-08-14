# Sistema de Cadastro de Vendedores e Departamentos - JavaFX

Aplicação desktop desenvolvida em **Java** com **JavaFX**, criada como projeto final do curso, implementando um CRUD completo (Criar, Listar, Editar e Remover) para **Vendedores (Sellers)** e **Departamentos (Departments)**, com persistência de dados em **MySQL**.

## 📋 Funcionalidades

- Cadastro, edição e remoção de **Departamentos**
- Cadastro, edição e remoção de **Vendedores**, com associação a um Departamento
- Validação de campos obrigatórios nos formulários
- Alertas de confirmação e de erro (ex: violação de integridade ao remover um departamento com vendedores vinculados)
- Atualização automática das tabelas (TableView) após cada operação

## 🛠️ Tecnologias e Padrões Utilizados

- **Java** (JDK)
- **JavaFX** (interface gráfica via FXML)
- **MySQL** (banco de dados relacional)
- **JDBC** com `mysql-connector-j-9.5.0`
- Padrão **DAO** (Data Access Object) e **Service Layer**
- Padrão **Listener** (`DataChangeListener`) para atualização reativa das telas

## ✅ Pré-requisitos

Antes de rodar o projeto, certifique-se de ter instalado:

1. **JDK** (Java Development Kit) instalado na máquina
2. **Biblioteca JavaFX** adicionada ao projeto (via Build Path / módulo)
3. **Driver JDBC do MySQL**: `mysql-connector-j-9.5.0`
4. **Servidor MySQL** instalado e em execução

## 🗄️ Configuração do Banco de Dados

1. Execute o script SQL disponibilizado neste repositório para criar o banco de dados e as tabelas (`department` e `seller`) necessárias para o funcionamento do sistema.

2. Configure o arquivo **`db.properties`** (localizado na raiz do projeto) com os dados de acesso ao seu banco de dados MySQL:

```properties
user=SEU_USUARIO
password=SUA_SENHA
dburl=jdbc:mysql://ENDERECO_DO_BANCO:3306/NOME_DO_BANCO
useSSL=false
```

> ⚠️ Substitua `SEU_USUARIO`, `SUA_SENHA`, `ENDERECO_DO_BANCO` (ex: `localhost`) e `NOME_DO_BANCO` pelos dados reais do seu ambiente MySQL.

## ▶️ Como Executar

1. Clone este repositório
2. Importe o projeto em sua IDE de preferência (Eclipse, IntelliJ, etc.) com suporte a JavaFX configurado
3. Adicione a biblioteca `mysql-connector-j-9.5.0` ao Build Path do projeto
4. Execute o script SQL para criar o banco de dados
5. Configure o arquivo `db.properties` com os dados do seu banco (conforme instruções acima)
6. Execute a classe `Main.java` para iniciar a aplicação

## 📁 Estrutura do Projeto

```
src/
├── application/       # Classe principal (Main)
├── db/                # Classes de conexão e exceções de banco de dados
├── gui/               # Controllers das telas (FXML) e utilitários de interface
├── model/
│   ├── dao/           # Interfaces e implementações DAO (acesso a dados)
│   ├── entities/       # Entidades (Department, Seller)
│   ├── exceptions/     # Exceções de validação
│   └── services/       # Camada de serviço (regras de negócio)
```

## 📄 Licença

Projeto desenvolvido para fins educacionais, como parte do módulo final de um curso de Java com JavaFX.
