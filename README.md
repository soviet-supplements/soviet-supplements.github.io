<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Page</title>
    <style>
        body {
            background-color: black;
            color: red;
            font-family: 'Courier New', Courier, monospace;
            text-align: center;
            padding-top: 20%;
        }

        input[type="password"] {
            font-family: 'Courier New', Courier, monospace;
            font-size: 20px;
            padding: 10px;
            background-color: black;
            color: red;
            border: 2px solid red;
            outline: none;
        }

        input[type="submit"] {
            background-color: red;
            color: black;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 18px;
            margin-top: 20px;
        }

        input[type="submit"]:hover {
            background-color: yellow;
        }

        h1 {
            font-size: 36px;
            letter-spacing: 2px;
        }

        .message {
            font-size: 16px;
            margin-top: 10px;
        }

        .error {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Access Restricted</h1>
    <p>Please enter the password to continue:</p>
    <form id="passwordForm">
        <input type="password" id="password" placeholder="Enter Code">
        <input type="submit" value="Submit">
    </form>
    <p class="message" id="message"></p>

    <script>
        document.getElementById('passwordForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const password = document.getElementById('password').value;
            const correctPassword = 'Medrol';  // Set the password you want

            if (password === correctPassword) {
                window.location.href = 'https://yourwebsite.com'; // Redirect to the main site
            } else {
                document.getElementById('message').innerHTML = "<span class='error'>Неправильный пароль. Попробуйте еще раз.</span>";
            }
        });
    </script>
</body>
</html>
