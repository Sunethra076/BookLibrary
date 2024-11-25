# BookLibrary
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Library</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: auto;
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1, h2 {
            text-align: center;
        }

        form {
            display: flex;
            flex-direction: column;
        }

        input {
            margin: 10px 0;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            padding: 10px;
            background: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background: #218838;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            background: #f8f9fa;
            margin: 5px 0;
            padding: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Book Library</h1>
        <form id="book-form">
            <input type="text" id="title" placeholder="Book Title" required>
            <input type="text" id="author" placeholder="Author" required>
            <input type="text" id="genre" placeholder="Genre" required>
            <button type="submit">Add Book</button>
        </form>
        <h2>Book List</h2>
        <ul id="book-list"></ul>
    </div>
    <script>
        document.getElementById('book-form').addEventListener('submit', function(e) {
            e.preventDefault();

            // Get input values
            const title = document.getElementById('title').value;
            const author = document.getElementById('author').value;
            const genre = document.getElementById('genre').value;

            // Create a new list item
            const li = document.createElement('li');
            li.textContent = `${title} by ${author} - Genre: ${genre}`;

            // Add the new list item to the book list
            document.getElementById('book-list').appendChild(li);

            // Clear the input fields
            document.getElementById('book-form').reset();
        });
    </script>
</body>
</html>
