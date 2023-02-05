# Persistindo objetos

No post anterior compartilhei um pouco sobre o que aprendi em relação aos arquivos pom.xml e persistence.xml, necessários para que possamos configurar e realizar a persistência de objetos utilizando o Hibernate com JPA.

Dando continuidade, hoje quero compartilhar o que aprendi sobre a criação de uma entidade e sobre como realizar as operações básicas de manipulação de um banco de dados.

# 🔰 Entidades 🔰

Começando com o que entendi sobre entidades, vi que basicamente são aquelas classes que servem como modelo as quais a JPA irá mapear, processar e criar uma tabela no banco de dados com aqueles atributos para que possamos armazenar os objetos persistidos.

Aprendi também algumas anotações que auxiliam o mapeamento, como:

@Entity: indica que aquela classe é uma entidade;
@Table: indica o nome da tabela que será usada para persistir os objetos;
@Id: indica que aquele atributo representa a chave primária;
@GeneratedValue: transfere a responsabilidade de gerar as chaves primárias para a própria aplicação e permite definir estratégias para que esse processo seja realizado;

# 🔰 Primeiras operações 🔰

Após aprender sobre o processo de mapeamento de uma entidade chegou a hora de finalmente aprender a persistir os objetos, realizar as primeiras operações. Em resumo, vi que para isso são necessários os seguintes passos:

1. Instanciar uma EntityManagerFactory (fábrica de gerenciadora de entidades);
2.  A partir dessa factory, instanciar uma EntityManager (gerenciadora de entidades);
3. Abrir uma Transaction;
4. Realizar a manipulação;
5. Fechar a Transaction;
6. Encerrar a EntityManager;
