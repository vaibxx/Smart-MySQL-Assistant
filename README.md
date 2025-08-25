# Smart-MySQL-Assistant
An interactive Streamlit-based web assistant for MySQL databases. It allows you to connect to your database, manage schemas, load metadata from JSON, and chat with an AI-powered SQL assistant for query generation and execution.


# Features

🔐 Login & Connections
-Connect to MySQL with username, password, host, and database name.
-Optionally load schema from JSON files instead of live DB.

📂 Schema Management
-Auto-detect primary keys, foreign keys, and constraints
-Download a template JSON to define schema manually.

🤖 AI SQL Assistant
-Chat interface for natural language queries.
-Generates SQL queries using LLMs.
-Executes queries and returns results interactively.

📝 Interactive Inserts
-Automatically fetch related foreign key values for dropdown selection.
-Simplifies inserting records across linked tables.

📊 Streamlit UI
-Clean, responsive layout (wide mode).
-Sidebar for login/config.
-Chat panel for conversation per connection.


# JSON Schema Example

🛠️ Here’s how a schema file looks:
{
  "tables": {
    "users": {
      "columns": {
        "id": {"type": "INT", "primary_key": true, "auto_increment": true},
        "name": {"type": "VARCHAR(255)", "nullable": false},
        "email": {"type": "VARCHAR(255)", "unique": true}
      }
    },
    "orders": {
      "columns": {
        "id": {"type": "INT", "primary_key": true, "auto_increment": true},
        "user_id": {"type": "INT", "foreign_key": "users.id"},
        "amount": {"type": "DECIMAL(10,2)"}
      }
    }
  }
}



# Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss.
