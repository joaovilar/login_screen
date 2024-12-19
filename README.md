# login_screen

![image](https://github.com/user-attachments/assets/95715f91-8d0a-4607-99f5-09722a95c2da)

![image](https://github.com/user-attachments/assets/309df00c-685f-4acc-8d52-355fc49333b7)

# Login Application

Este projeto é uma aplicação de login desenvolvida com Streamlit e conectada a um banco de dados Microsoft SQL Server. Ele inclui autenticação de usuário e uma interface personalizada com CSS customizado.

## Recursos

- **Autenticação de Usuário:** Os usuários podem fazer login usando credenciais armazenadas em um banco de dados SQL Server.
- **Interface Personalizada:** O design da interface foi melhorado com CSS customizado para criar uma experiência de usuário moderna.
- **Conexão ao Banco de Dados:** Conexão segura ao banco de dados para validação de usuários.
- **Saudação Personalizada:** Após o login bem-sucedido, o usuário é saudado pelo nome armazenado no banco de dados.

## Tecnologias Utilizadas

- **Streamlit:** Framework para criação de aplicações web interativas.
- **PyODBC:** Biblioteca para conexão ao banco de dados SQL Server.
- **Microsoft SQL Server:** Banco de dados relacional para armazenamento de credenciais de usuário.

## Configuração

### Pré-requisitos

1. **Python 3.8 ou superior** deve estar instalado.
2. Instale as dependências necessárias:

```bash
pip install streamlit pyodbc
```

3. Configure o banco de dados Microsoft SQL Server e certifique-se de que a tabela `tbusuario` existe com os seguintes campos:

| Campo   | Tipo         |
|---------|--------------|
| usuario | VARCHAR(50)  |
| senha   | VARCHAR(50)  |
| nome    | VARCHAR(100) |

4. Atualize as credenciais de banco de dados no código:

```python
server = 'azure-sql-dev-1.database.windows.net'
database = 'login'
db_username = 'seu_usuario'
db_password = 'sua_senha'
```

### Executando a Aplicação

1. No terminal, execute o seguinte comando para iniciar a aplicação Streamlit:

```bash
streamlit run app.py
```

2. Acesse a aplicação no navegador no endereço padrão: `http://localhost:8501`

## Personalização

### CSS Customizado

O design da aplicação foi melhorado com estilos CSS personalizados. Você pode editar o estilo diretamente no código, na seção de `st.markdown`.

### Mensagem de Boas-vindas

A mensagem exibida após o login pode ser personalizada na função `pagina_bem_vindo`:

```python
st.write(f"Olá, {st.session_state.nome}!")
```

## Funcionalidades Futuras

- Criação de novos usuários diretamente pela interface.
- Recuperação de senha.
- Logs de auditoria para registrar tentativas de login.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir um problema ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

