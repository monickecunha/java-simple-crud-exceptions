# 🚀 Projeto CRUD Simples de Usuários em Java

---

Este projeto é uma aplicação de console simples em Java que simula um sistema de **C**reate, **R**ead, **U**pdate e **D**elete (CRUD) para usuários. O principal objetivo deste projeto foi **demonstrar e aplicar diversos exemplos de tratamento de exceções** em um contexto prático de CRUD, além de explorar conceitos fundamentais de programação orientada a objetos e manipulação básica de dados em memória.

## ✨ Funcionalidades

O sistema permite as seguintes operações com usuários:

* **Cadastrar (Save):** Adiciona um novo usuário ao "armazenamento" em memória.
* **Atualizar (Update):** Modifica os dados de um usuário existente com base no seu ID.
* **Excluir (Delete):** Remove um usuário do armazenamento usando seu ID.
* **Buscar por Identificador (Find by ID):** Localiza e exibe os dados de um usuário específico.
* **Listar (Find All):** Exibe todos os usuários atualmente cadastrados.
* **Sair (Exit):** Encerra a aplicação.

## ⚠️ Foco Principal: Tratamento de Exceções

Um dos pilares deste projeto é a implementação robusta do tratamento de exceções. Diversas **exceções personalizadas** foram criadas para lidar com cenários de erro específicos, proporcionando um controle mais refinado sobre o fluxo do programa e a resposta a situações inesperadas. Isso inclui:

* **`CustomException`**: Uma exceção genérica para erros controlados.
* **`EmptyStorageException`**: Para quando as operações são tentadas em um armazenamento de dados vazio.
* **`UserNotFoundException`**: Para casos onde um usuário não é encontrado pelo seu identificador.
* **`ValidatorException`**: Para indicar falhas nas regras de validação de dados de entrada do usuário.

A forma como essas exceções são lançadas (`throw`) e capturadas (`try-catch`) em diferentes pontos do código demonstra como gerenciar erros de forma eficaz, evitando a interrupção abrupta do programa e fornecendo feedback útil ao usuário.

## 🛠️ Tecnologias Utilizadas

* **Java:** Linguagem de programação principal.
* **Estruturas de Dados Java:** `ArrayList` para armazenamento em memória.
* **Programação Orientada a Objetos (POO):** Utilização de classes, objetos, encapsulamento e métodos.
* **Enum:** Para representar as opções do menu.
* **`java.time` (LocalDate, DateTimeFormatter):** Para manipulação de datas.
* **Streams API:** Utilizado na `UserDAO` para operações de busca.

## 📁 Estrutura do Projeto

O projeto segue uma estrutura de pacotes organizada:

* **`Main.java`**: Ponto de entrada da aplicação, responsável pela interface com o usuário e pelo fluxo principal.
* **`dao`**: Contém a classe `UserDAO`, que simula a camada de acesso a dados, gerenciando os usuários em uma lista em memória.
* **`exception`**: Define exceções personalizadas para erros específicos do domínio da aplicação.
* **`model`**: Contém as classes que representam as entidades e opções do sistema (`UserModel` e `MenuOption`).
* **`validator`**: Contém a lógica de validação para os dados do usuário.

## ⚙️ Como Executar

Para executar este projeto, você precisará ter o **JDK (Java Development Kit)** instalado em sua máquina.

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/monickecunha/java-simple-crud-exceptions.git](https://github.com/monickecunha/java-simple-crud-exceptions.git)
    cd java-simple-crud-exceptions
    ```

2.  **Compile o Código:**
    Navegue até a pasta `src` e compile os arquivos `.java`. Se estiver usando uma IDE (como IntelliJ IDEA, Eclipse ou VS Code com extensões Java), ela fará isso automaticamente.

    Para compilar via terminal (a partir da raiz do projeto):
    ```bash
    javac -d out src/Main.java src/br/com/dio/dao/*.java src/br/com/dio/exception/*.java src/br/com/dio/model/*.java src/br/com/dio/validator/*.java
    ```
    *Obs: Você pode precisar ajustar o comando `javac` dependendo da versão do seu JDK e da sua estrutura de pacotes complexa para compilar tudo de uma vez. Usar uma IDE é mais fácil.*

3.  **Execute a Aplicação:**
    Após a compilação, você pode executar o `Main` a partir do diretório de saída:
    ```bash
    java -cp out Main
    ```
    Ou, se estiver em uma IDE, basta executar a classe `Main`.

A aplicação será iniciada no console, apresentando um menu de opções para interagir com o cadastro de usuários.

## 🤝 Contribuições

Sinta-se à vontade para explorar o código, sugerir melhorias ou relatar problemas.

---

## 👨‍💻 Autor

[monickecunha](https://github.com/monickecunha/) - Estudante de Análise e Desenvolvimento de Sistemas.
