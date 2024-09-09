# Reloj Digital

Este proyecto es un reloj digital simple creado con HTML, CSS y JavaScript. Muestra la hora actual en formato de 24 horas y se actualiza automáticamente cada segundo.

## Estructura del Proyecto

El proyecto consta de tres archivos principales:

1. **`index.html`**: Contiene la estructura básica del reloj digital.
2. **`styles.css`**: Define el estilo y diseño del reloj digital y la página.
3. **`script.js`**: Actualiza la hora en el reloj cada segundo.

## Instalación y Uso

1. **Clona el Repositorio** (si aplicable):
    ```bash
    git clone https://github.com/tu-usuario/reloj-digital.git
    ```

2. **Navega al Directorio del Proyecto**:
    ```bash
    cd reloj-digital
    ```

3. **Abre `index.html` en un Navegador Web**:
    Simplemente abre el archivo `index.html` en tu navegador favorito para ver el reloj en acción.

## Archivos

### `index.html`
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reloj Digital</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="clock" id="clock">
        <!-- El reloj se actualizará aquí -->
    </div>
    <script src="script.js"></script>
</body>
</html>


body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #282c34;
    color: #61dafb;
    font-family: 'Arial', sans-serif;
}

.clock {
    font-size: 5rem;
    padding: 20px;
    border: 5px solid #61dafb;
    border-radius: 10px;
    background-color: #282c34;
    text-align: center;
}

function updateClock() {
    const now = new Date();
    const hours = String(now.getHours()).padStart(2, '0');
    const minutes = String(now.getMinutes()).padStart(2, '0');
    const seconds = String(now.getSeconds()).padStart(2, '0');
    const timeString = `${hours}:${minutes}:${seconds}`;

    document.getElementById('clock').textContent = timeString;
}

// Actualiza el reloj cada segundo
setInterval(updateClock, 1000);

// Llama a la función una vez para que el reloj se muestre inmediatamente
updateClock();

Contribuciones
Si deseas contribuir a este proyecto, por favor sigue estos pasos:

Realiza un fork del repositorio.
Crea una nueva rama (git checkout -b feature/nueva-funcionalidad).
Realiza tus cambios y haz commit (git commit -am 'Añadida nueva funcionalidad').
Envía un pull request.
Licencia
Este proyecto está licenciado bajo la Licencia MIT.
