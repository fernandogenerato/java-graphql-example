

# Spring GraphQL Example

This is a demo project that illustrates how to use Spring with GraphQL to create a book and author query API using the guide available in spring https://spring.io/guides/gs/graphql-server
## Prerequisites

Before you begin, ensure you have the following requirements:

- JDK 21 or higher installed
- Maven installed
- Java IDE (such as IntelliJ IDEA, Eclipse, or similar)

## How to Use

1. Clone this repository on your local machine:

```bash
git clone https://github.com/fernandogenerato/java-graphql-example.git
```

2. Open the project in your Java IDE.

3. Navigate to the `BookController` class located in `src/main/java/com/graphql/demo`.

4. Run the Spring Boot application. This will start a local server on the default port (usually 8080).

5. Now, you can send GraphQL queries to the `/graphql` endpoint like this:

```graphql
query {
  bookById(id: "book-1") {
    id
    name
    pageCount
    author {
      id
      firstName
      lastName
    }
  }
}

query {
  bookByAuthorID(id: "author-3") {
    id
    name
    pageCount
    author {
      id
      firstName
      lastName
    }
  }
}
```
## Included Unit Tests
This project includes unit tests to ensure code coverage and maintain quality. You can find the unit tests in the src/test directory. Run the tests using your preferred IDE or using Maven:

![image](https://github.com/fernandogenerato/java-graphql-example/assets/22321412/a2f76e89-e656-4669-b59a-5971a222a093)

## Accessing GraphiQL Client

To facilitate testing and exploration of the GraphQL API, you can access the GraphiQL client by visiting [http://localhost:8080/graphiql](http://localhost:8080/graphiql). 

GraphiQL provides an interactive graphical interface for building and sending GraphQL queries.

See more in Official docs: https://github.com/graphql/graphiql

![image](https://github.com/fernandogenerato/java-graphql-example/assets/22321412/810b2390-a312-4881-b7aa-6f7abe3879fd)


## Project Structure

- `BookController`: Spring controller responsible for handling GraphQL queries related to books and authors.

- `Book`: Model class representing a book with methods to retrieve books by ID and author.

- `Author`: Model class representing an author with methods to retrieve authors by ID.
