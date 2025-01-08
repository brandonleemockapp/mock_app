
# Catalog Web App

This is a Django web application that allows users to search a catalog of products by description, filter by category, and apply multiple tags.

## Prerequisites

Before you start, ensure you have the following installed:

- Python 3.x
- Django
- Git

## Setup Instructions

### 1. Clone the Repository

First, clone the repository to your local machine using the following command:

```bash
git clone https://github.com/brandonleemockapp/mock_app.git
cd mock_app/catalog_app
```

### 2. Install Dependencies

Make sure to install the required dependencies listed in `requirements.txt`. You can do this using `pip`:

```bash
pip install -r requirements.txt
```

### 3. Make Migrations

Generate the necessary migration files based on the models in your Django app:

```bash
python manage.py makemigrations
```

### 4. Apply Migrations

Apply the migrations to the database:

```bash
python manage.py migrate
```

### 5. Populate the Database

If you need to populate the database with sample data, you can run the following script:

```bash
python manage.py shell < scripts/populate_db.py
```

This will populate the database with 20 sample products.

### 6. Run the Development Server

To start the development server, run:

```bash
python manage.py runserver
```

The server will start, and you can access the web app by visiting [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

## How to Use the Web App
### 1. Search Products
On the main page, you’ll see a search bar that allows you to search products by their descriptions.

Type a keyword (e.g., "phone", "gamer") in the search bar and hit "Search".
The page will refresh and display products that match the description.

### 2. Filter by Category
You can filter products by category using the dropdown menu. The available categories are fetched from the database.

Select a category from the dropdown (e.g., Electronics, Clothing, etc.).
The page will display only the products within the selected category.

### 3. Filter by Tags
You can filter products by tags by selecting one or more checkboxes for tags (e.g., New, Sale, Popular).

Check one or more tags, and the page will display products that match the selected tags.
The web app will display products that match all selected tags.

### Use example
Search for a description: "gamer"
Filter by category: "Electronics"
Filter by tags: Select "New" and "Sale"
In this case, the web app will display only the products that:

Have the word "gamer" in their description
Belong to the "Electronics" category
Have both "New" and "Sale" tags.

### 4. Reset Filters
If you want to reset the filters, you can either:

Clear the search bar and deselect all checkboxes.
Refresh the page to reset the filters.
