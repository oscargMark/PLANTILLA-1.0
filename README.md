# PLANTILLA-1.0
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario de Datos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 50px;
            background-color: #f4f4f4;
        }
        h1 {
            text-align: center;
        }
        form {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            max-width: 500px;
            margin: auto;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        label {
            display: block;
            margin-top: 15px;
        }
        input[type="text"], input[type="number"] {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        input[type="submit"] {
            margin-top: 20px;
            padding: 10px 15px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
        .success {
            color: green;
            text-align: center;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <h1>Formulario de Datos</h1>
    <form id="formulario">
        <label>Nombre:<input type="text" name="nombre" required></label>
        <label>Apellido 1:<input type="text" name="apellido1" required></label>
        <label>Apellido 2:<input type="text" name="apellido2"></label>
        <label>Tipo de vía:<input type="text" name="tipo_via"></label>
        <label>Nombre de vía:<input type="text" name="nombre_via"></label>
        <label>Número de vía:<input type="text" name="numero_via"></label>
        <label>Escalera:<input type="text" name="escalera"></label>
        <label>Portal:<input type="text" name="portal"></label>
        <label>Piso:<input type="text" name="piso"></label>
        <label>Código postal:<input type="text" name="codigo_postal"></label>
        <label>Localidad:<input type="text" name="localidad"></label>
        <label>Provincia:<input type="text" name="provincia"></label>
        <input type="submit" value="Enviar">
    </form>
    <div class="success" id="mensaje"></div>

    <script>
        const form = document.getElementById("formulario");
        const mensaje = document.getElementById("mensaje");

        form.addEventListener("submit", function(e) {
            e.preventDefault();
            // Aquí puedes añadir lógica para enviar los datos a Google Sheets o backend
            mensaje.textContent = "¡Formulario enviado correctamente!";
            form.reset();
        });
    </script>
</body>
</html>
