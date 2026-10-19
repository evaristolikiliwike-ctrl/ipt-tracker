\# IPT Tracker



\## Project Overview



IPT Tracker is a Spring Boot application developed as part of a project to support the management and tracking of Industrial Practical Training (IPT) activities.



\## Technologies Used



\- Java 21

\- Spring Boot

\- Maven

\- PostgreSQL

\- Spring Data JPA

\- Flyway Database Migrations

\- Bean Validation

\- Spring Boot Actuator



\## Prerequisites



Before running the application, install the following:



\- JDK 21

\- PostgreSQL or Docker

\- Git

\- A terminal such as PowerShell

\- Maven Wrapper, which is included in this repository



\## Getting Started



\### 1. Clone the Repository



```bash

git clone https://github.com/evaristolikiliwike-ctrl/ipt-tracker.git

cd ipt-tracker

```



\### 2. Configure the Database



The application uses PostgreSQL. Its default database URL is:



```text

jdbc:postgresql://localhost:5433/ipt\_tracker

```



Create a PostgreSQL database named `ipt\_tracker` and configure the connection details using these environment variables:



| Variable | Description |

|---|---|

| `DB\_URL` | PostgreSQL connection URL |

| `DB\_USERNAME` | PostgreSQL username |

| `DB\_PASSWORD` | PostgreSQL password |

| `JWT\_SECRET` | Secret used for JWT signing |

| `JWT\_EXPIRATION\_SECONDS` | JWT expiration time in seconds |



Use the values appropriate for your local environment. Never publish real database passwords or JWT secrets to GitHub.



\### 3. Run the Application



On Windows PowerShell:



```powershell

.\\mvnw.cmd spring-boot:run

```



On Linux or macOS:



```bash

./mvnw spring-boot:run

```



The default application port is `8081`.



\### 4. Run Tests



On Windows:



```powershell

.\\mvnw.cmd test

```



On Linux or macOS:



```bash

./mvnw test

```



\### 5. Check Application Health



If Spring Boot Actuator health is enabled and accessible, open:



`http://localhost:8081/actuator/health`



\## Database Migrations



Flyway manages database migrations stored in:



```text

src/main/resources/db/migration

```



Hibernate schema validation is enabled. The database schema must match the application's entity mappings and migration scripts.



\## Project Structure



```text

ipt-tracker/

├── src/

│   ├── main/

│   │   ├── java/

│   │   └── resources/

│   │       └── db/

│   │           └── migration/

│   └── test/

├── .gitignore

├── mvnw

├── mvnw.cmd

├── pom.xml

└── README.md

```



\## Contributing



1\. Create a branch for your changes.

2\. Make your changes.

3\. Run the tests.

4\. Commit your changes with a descriptive message.

5\. Push your changes to GitHub.



\## License



No license has been specified for this project yet.

