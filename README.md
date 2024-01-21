# DSLIST - Gerenciador de Lista de Jogos

## Descrição do Projeto

Desenvolvi o projeto DSLIST, um back-end robusto para gerenciar uma lista de jogos no GitHub. Utilizei tecnologias modernas como Spring, APIs RESTful e Docker Compose, destacando habilidades em ORM, consultas SQL personalizadas e implantação contínua. Essa experiência solidificou meu conhecimento em desenvolvimento back-end e integração eficiente de tecnologias para projetos web escaláveis.

### Tecnologias e Fundamentos Utilizados

- Sistemas Web e Recursos
- Padrão REST para API Web
- Estruturação de Projeto Spring REST
- Entidades e ORM
- Database Seeding
- Padrão de Camadas
- Padrão DTO
- Relacionamentos N-N
- Consultas SQL no Spring Data JPA
- Projections
- Ambiente Local com Docker Compose
- Processo de Homologação
- Processo de Deploy com CI/CD
- Configuração de CORS

### Estrutura do Projeto

```bash
.
├── .mvn
├── src
│   ├── main
│   │   └── java/com/devsuperior/dslist
│   │       ├── Controllers
│   │       │   ├── GameController.java
│   │       │   └── GameListController.java
│   │       ├── dto
│   │       │   ├── GameDTO.java
│   │       │   ├── GameListDTO.java
│   │       │   ├── GameMinDTO.java
│   │       │   └── ReplacementDTO.java
│   │       ├── entities
│   │       │   ├── Belonging.java
│   │       │   ├── BelongingPK.java
│   │       │   ├── Game.java
│   │       │   └── GameList.java
│   │       ├── projections
│   │       │   └── GameMinProjection.java
│   │       ├── repositories
│   │       │   ├── GameListRepository.java
│   │       │   └── GameRepository.java
│   │       └── services
│   │           ├── GameListService.java
│   │           └── GameService.java
│   └── resources
│       ├── application-dev.properties
│       ├── application-prod.properties
│       ├── application-test.properties
│       ├── application.properties
│       └── import.sql
├── test/java/com/devsuperior/dslist
│   └── DslistApplicationTests.java
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── system
```

### Instruções de Seed do Banco de Dados

```sql
INSERT INTO tb_game_list (name) VALUES ('Aventura e RPG');
INSERT INTO tb_game_list (name) VALUES ('Jogos de plataforma');

INSERT INTO tb_game (title, score, game_year, genre, platforms, img_url, short_description, long_description) VALUES ('Mass Effect Trilogy', 4.8, 2012, 'Role-playing (RPG), Shooter', 'XBox, Playstation, PC', 'https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/1.png', 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit esse officiis corrupti unde repellat non quibusdam! Id nihil itaque ipsum!', 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus dolorum illum placeat eligendi, quis maiores veniam. Incidunt dolorum, nisi deleniti dicta odit voluptatem nam provident temporibus reprehenderit blanditiis consectetur tenetur. Dignissimos blanditiis quod corporis iste, aliquid perspiciatis architecto quasi tempore ipsam voluptates ea ad distinctio, sapiente qui, amet quidem culpa.');
-- Adicione mais inserções conforme necessário

INSERT INTO tb_belonging (list_id, game_id, position) VALUES (1, 1, 0);
-- Adicione mais inserções conforme necessário
```
### Executando o Projeto Localmente
Certifique-se de ter o Docker Compose instalado. Clone o repositório e execute o seguinte comando na raiz do projeto:
```bash
docker-compose up -d
```
#### O projeto estará disponível em http://localhost:8080.

### Testes Automatizados
O projeto inclui testes automatizados para garantir a integridade e o funcionamento correto das funcionalidades. Execute os testes com o seguinte comando:
```bash
./mvnw test
```

### Contribuição
Sinta-se à vontade para contribuir para o projeto. Para isso, siga o processo padrão de fork, branch, commit e pull request.





















