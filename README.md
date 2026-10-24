# SIDESP Backend

Backend do projeto SIDESP desenvolvido em Java 17 com Spring Boot, responsável pela API, autenticação e acesso ao banco de dados.

## Tecnologias

- Java 17
- Spring Boot
- Maven
- MySQL / MariaDB
- Flyway
- Spring Security e JWT
- Testes automatizados com JUnit

## Pré-requisitos

- JDK 17
- MySQL ou MariaDB

## Configuração local

1. Crie um banco de dados vazio chamado `sidesp`.
2. Execute o script `scripts/configurar-local.ps1` no PowerShell para gerar a configuração local.
3. Informe a URL JDBC, o usuário e a senha do banco local.
4. Preserve as chaves criptográficas existentes se já possuir uma configuração válida.

O arquivo `config/local.properties` contém dados locais e não deve ser enviado ao GitHub. Use `config.example.properties` apenas como referência.

## Executar

Para iniciar a aplicação:

```powershell
.\mvnw.cmd spring-boot:run
```

Para executar os testes:

```powershell
.\mvnw.cmd test
```

Para gerar o pacote:

```powershell
.\mvnw.cmd clean package
```

## Estrutura

- `src/main/java`: código-fonte Java.
- `src/main/resources`: configurações e migrations do Flyway.
- `src/test`: testes automatizados.
- `scripts`: scripts de configuração local.
- `banco`: scripts auxiliares do banco de dados.
- `pom.xml`: dependências e configuração Maven.

## Segurança

Não publique senhas, tokens, chaves criptográficas ou arquivos de configuração locais.

## Status

Projeto acadêmico em desenvolvimento. Consulte o código-fonte e os testes para verificar o estado atual das funcionalidades.
