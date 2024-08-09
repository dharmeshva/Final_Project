# [Group 10] - SENG8070 - Final Assignment

# Project Overview:-
Welcome to the project for the Online Bookstore System! In order to sell physical books, e-books, and audiobooks online, this project entails creating a robust database system.Customers can explore the catalogue, make purchases, and give reviews using the system. The technology also integrates publishers and authors.

# Group Members and Responsibilities

1. Muzammil Shaikh - 8969614: Unit tests, Integration tests and migration scripts
2. Dharmesh Vanani - 8952848 : CRUD functions, Database design and implementation 
3. Dhrumilbhai Dhameliya - 8970119 : Entity Relations diagram and documentation

# Database Design Tables and Attributes
Explanation:
    The online bookstore's various entities are represented by the multiple tables that make up the database structure. Every table records pertinent details about the object it represents.
In addition to supporting effective queries and transactions, this design guarantees data integrity.

### Authors
| Attribute   | Type          |
|-------------|---------------|
| author_id   | INT PRIMARY KEY |
| name        | VARCHAR(255)  |
| bio         | TEXT          |
| total_books | INT           |

### Publishers
| Attribute     | Type          |
|---------------|---------------|
| publisher_id  | INT PRIMARY KEY |
| name          | VARCHAR(255)  |
| contactInfo   | VARCHAR(255)  |
| Book_id       | INT           |

### Books
| Attribute       | Type            |
|-----------------|-----------------|
| book_id         | INT PRIMARY KEY |
| title           | VARCHAR(255)    |
| genre           | INT             |
| price           | DECIMAL(10,2)   |
| format          | VARCHAR(20)     |
| author_id       | INT             |
| publisher_id    | INT             |
| reviews_id      | INT             |
| publicationYear | INT             |

### Customers
| Attribute      | Type            |
|----------------|-----------------|
| customer_id    | INT PRIMARY KEY |
| name           | VARCHAR(255)    |
| email          | VARCHAR(255)    |
| total_spent    | DECIMAL(10,2)   |
| join_date      | DATE            |
| publisher_id   | INT             |
| reviews_id     | INT             |
| order  _id     | INT             |


### Orders
| Attribute     | Type            |
|---------------|-----------------|
| order_id      | INT PRIMARY KEY |
| customer_id   | INT             |
| order_date    | DATE            |
| status        | VARCHAR(20)     |
| total_amount  | DECIMAL(10,2)   |

### Purchase
| Attribute    | Type            |
|--------------|-----------------|
| purchase_id      | INT PRIMARY KEY |
| customer_id      | INT             |
| book_id          | INT             |
| quantity         | INT             |
| total_price      | DECIMAL(10,2)   |
| purchaseDate     |DATE             |

### Reviews
| Attribute     | Type            |
|---------------|-----------------|
| review_id     | INT PRIMARY KEY |
| book_id       | INT             |
| customer_id   | INT             |
| rating        | INT             |
| comment       | TEXT            |
| review_date   | DATE            |


## Prerequisites

Before starting the project, ensure you have the following installed:

1. **Docker** (to run PostgreSQL)
2. **Node.js** (at least version 12)
3. **TypeScript** (globally installed)
4. **pg (node-postgres)** library for PostgreSQL interaction

You can install these prerequisites using the following commands:

```bash
# Install Docker
# For Ubuntu
sudo apt update
sudo apt install docker.io
```
### Download Node.js:
    Navigate to the [Download Page of Nodejs](https://nodejs.org/en/download/),
    Download the package that corresponds to your system.
    
    ```bash
    node -v
    ```

### Clone the Repository:
```bash
git clone (https://github.com/dharmeshva/Final_Project.git)
cd Final_Project
```
### Install the required Dependencies:
```bash
npm install axios@^1.6.2 cors@^2.8.5 express@^4.18.1 pg@^8.7.3 reflect-metadata@^0.1.13 typeorm@^0.3.6
```
### Install the required Dev Dependencies:
```bash
npm install --save-dev @types/cors@^2.8.12 @types/express@^4.17.13 @types/node@^18.0.0
npm install --save-dev @typescript-eslint/eslint-plugin@^5.29.0 @typescript-eslint/parser@^5.29.0 eslint@^8.18.0
npm install --save-dev eslint-plugin-import@^2.26.0 eslint-plugin-jest@^26.5.3 jest@^28.1.1
npm install --save-dev nodemon@^3.0.1 ts-jest@^28.0.5 ts-node@^10.2.1 typescript@^4.7.4
```

### Run the Project:
```bash
npm start
```

### Run Unit Tests:
```bash
npm run test
```
### Run Integration Tests :
Run integration tests to verify the interaction between different tables and data consistency
```bash
npm run test:integration
```










