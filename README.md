Explorando Padrões de Projetos na Prática com Java
Repositório com as implementações dos padrões de projeto explorados no Lab "Explorando Padrões de Projetos na Prática com Java". Especificamente, este projeto explorou a aplicação desses padrões utilizando o ecossistema Spring Framework para criar uma API robusta e escalável.

🧠 Padrões de Projeto Explorados
Durante o desenvolvimento, foram implementados e observados os seguintes padrões:

Singleton: O Spring utiliza este padrão por padrão para gerenciar o ciclo de vida e o escopo dos Beans.

Strategy/Repository: Implementado para facilitar a persistência de dados e a troca de estratégias de acesso ao banco através do Spring Data JPA.

Facade: Utilizado para abstrair a complexidade da integração com a API externa do ViaCEP e a persistência no banco de dados local, oferecendo uma interface simples para o cliente.

🛠️ Desenvolvimento e Fluxo de Trabalho
Para a conclusão deste desafio, segui as boas práticas de versionamento e colaboração:

Fork: Realizei o fork do repositório original da DIO para minha conta pessoal do GitHub.

Clone: Baixei o projeto para desenvolvimento local utilizando o VS Code.

Implementação: Realizei as alterações no código para consolidar o aprendizado, integrando o OpenFeign para o consumo de serviços externos.

🚀 Tecnologias e Configuração
Java 17 (Utilizando o JDK da Eclipse Adoptium).

Spring Boot 2.5.4.

Spring OpenFeign: Para consumo simplificado da API do ViaCEP.

H2 Database: Banco de dados em memória para agilidade nos testes.

📖 Como Executar e Testar
Execução via Terminal
Para rodar a aplicação no Windows, utilize o Maven Wrapper (certifique-se de estar na pasta raiz):

PowerShell
.\mvnw.cmd spring-boot:run
(Nota: Se houver erro de porta 8080 em uso, certifique-se de encerrar processos Java ativos antes de reiniciar).

Testes via Swagger (OpenAPI)
Após iniciar a aplicação, você pode testar todos os verbos HTTP (GET, POST, PUT, DELETE) através da documentação interativa: 🔗 URL: http://localhost:8080/swagger-ui.html

Exemplo de JSON para o POST: Ao cadastrar um novo cliente, o sistema utiliza o padrão Facade para buscar o endereço completo automaticamente através do CEP informado:

JSON
{
  "nome": "Paulo Barros",
  "endereco": {
    "cep": "51030000"
  }
}
Desenvolvido por: [Seu Nome/GitHub] Estudante de Análise e Desenvolvimento de Sistemas (4º Período).
