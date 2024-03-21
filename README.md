# Database Abstraction Layer (DAL)

A lightweight JavaScript package for abstracting database operations and providing a unified interface for interacting with different database systems.

## Installation

```bash
npm install database-abstraction-layer
```

## Features

- **Simple Interface**: Provides a simple and consistent API for common database operations such as CRUD (Create, Read, Update, Delete).
- **Support for Multiple Databases**: Supports various database systems including MySQL, PostgreSQL, MongoDB, SQLite, etc.
- **Security**: Built-in security features to prevent SQL injection and other common security vulnerabilities.
- **Customizable**: Easily extendable and customizable to suit specific project requirements.
- **Asynchronous Operations**: Supports asynchronous operations for handling large datasets and complex queries.

## Usage

```javascript
const DAL = require('database-abstraction-layer');

// Create a new DAL instance with database configuration
const db = new DAL({
  dialect: 'mysql', // Specify the database dialect (mysql, postgres, mongodb, sqlite, etc.)
  host: 'localhost',
  username: 'user',
  password: 'password',
  database: 'my_database'
});

// Example: Insert data into a table
db.insert('users', { name: 'John Doe', email: 'john@example.com' })
  .then(result => {
    console.log('Data inserted successfully:', result);
  })
  .catch(error => {
    console.error('Error inserting data:', error);
  });
```

## Documentation

For detailed usage instructions and API documentation, please refer to the [documentation].

## Contributing

Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
