# Project 05 --- Inventory Management System

A beginner-friendly, menu-driven Inventory Management System built with
Python. The project uses JSON for persistent storage, allowing product
records to remain available when the program is closed and reopened.

## Features

-   **Add products** --- store a product ID, name, price, and quantity.
-   **Update products** --- update the price and quantity of an existing
    product.
-   **Delete products** --- remove a product using its ID.
-   **Search products** --- find a product by ID or name.
-   **Inventory report** --- display the number of products, total
    quantity in stock, total inventory value, and low-stock items.
-   **JSON data storage** --- load records from and save records to
    `inventory.json`.
-   **Menu-driven interface** --- choose an operation from the main
    menu.

## Technologies Used

-   Python
-   JSON (`json` module)
-   Jupyter Notebook / Python environment

## How It Works

1.  When the program starts, it attempts to load records from
    `inventory.json`.
2.  If the file does not exist yet, the program starts with an empty
    inventory.
3.  The `save_records()` function writes the current inventory to the
    JSON file.
4.  Add, update, and delete operations call `save_records()` so changes
    are persisted.
5.  The main menu lets the user choose which operation to perform.

## Product Record Structure

Each product is stored as a dictionary with the following fields:

``` python
{
    "id": "1001",
    "name": "Soya Milk",
    "price": 35.0,
    "quantity": 200
}
```

The records are stored as a list of dictionaries and saved in JSON
format.

## Running the Project

1.  Make sure Python or Jupyter Notebook is installed.
2.  Open the notebook or Python file containing the project code.
3.  Run the setup cells first so the JSON data is loaded and the
    functions are defined.
4.  Run the main menu:

``` python
main_menu()
```

5.  Select an option from the menu and follow the prompts.

> Keep `inventory.json` in the same working directory as the program.
> The file stores inventory data; Python function definitions still need
> to be run when starting a fresh notebook kernel.

## Inventory Report

The report calculates:

-   Total number of products
-   Total quantity across all products
-   Total inventory value, calculated as `price × quantity` for each
    product
-   Products with fewer than 10 units in stock

The low-stock threshold is currently set to fewer than 10 units and can
be adjusted in the code.

## Project Structure

``` text
Inventory-Management-System/
├── inventory_management.ipynb   # Notebook containing the Python code
├── inventory.json               # Saved inventory records (created at runtime)
└── README.md                    # Project documentation
```

Rename the notebook in this example to match your actual filename.

## Current Limitations

-   The current version expects valid numeric input for price and
    quantity; input validation can be added as an enhancement.
-   Data is stored locally in a JSON file rather than a database.
-   The application runs in a console/notebook rather than a graphical
    interface.

## Possible Future Improvements

-   Add input validation for price and quantity.
-   Add a confirmation prompt before deleting a product.
-   Allow partial-name searches.
-   Add sorting and filtering by price or stock quantity.
-   Export inventory reports to CSV or Excel.
-   Use SQLite or MySQL for database-backed storage.
-   Add a graphical user interface.

## Learning Outcomes

Through this project, I practised:

-   Python functions and loops
-   Lists and dictionaries
-   Conditional statements
-   Reading and writing JSON files
-   Searching and updating records
-   Organising a program into reusable functions
-   Building a menu-driven application

Shriya Verma | Data Analytics with Generative AI 
August Batch 2026

------------------------------------------------------------------------

**Project:** Project 05 --- Inventory Management System\
**Language:** Python\
**Storage:** JSON
