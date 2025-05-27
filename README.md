
# Block Wars

**Block Wars** es un juego tipo arcade desarrollado en Python con Pygame. El jugador controla una nave que dispara hacia enemigos descendentes, recolecta ítems y trata de sobrevivir el mayor tiempo posible acumulando puntos.

---

##  Cómo jugar

- Mueve la nave con las teclas **A** (izquierda) y **D** (derecha).
- Dispara con la **barra espaciadora**.
- Pausa el juego con la tecla **P**.
- Recoge ítems para mejorar tu rendimiento.
- Evita que los enemigos colisionen contigo.
- El juego termina cuando pierdes todas las vidas.

---

##  Decisiones de diseño

- **Modularidad**: El código fue dividido en archivos por responsabilidad:
  - `main_code.py`: lógica principal del juego.
  - `personaje.py`: contiene la clase `Cubo` (la nave del jugador).
  - `enemigo.py`: contiene la clase `Enemigo`, que baja desde arriba.
  - `balas.py`: gestiona las balas que dispara el jugador.
  - `item.py`: gestiona los ítems con efectos (más balas, vidas, velocidad).

- **Colisiones**: Se manejan con `pygame.Rect` para detectar impactos entre balas, enemigos, ítems y el jugador.

- **Ítems especiales**:
  - **Item 1 (Ficha)**: aumenta la frecuencia de disparo.
  - **Item 2 (corazón)**: recupera una vida.
  - **Item 3 (Rayo)**: duplica la velocidad del jugador.

- **Audio**: Se agregaron efectos de sonido para disparos, daño, ítems y eventos como "game over" o pausas.

- **Menús interactivos**: Hay pantallas para el menú principal, pausa y game over, cada uno con botones visuales y sonidos.

- **Dificultad progresiva**: A medida que avanza el juego, los enemigos aparecen más rápido.

---

## Estructura del proyecto

```
BlockWars/
├── main_code.py
├── personaje.py
├── enemigo.py
├── balas.py
├── item.py
├── imagenes/
│   ├── ship.svg
│   ├── enemy.png
│   ├── bullet.png
│   ├── item.png
│   ├── corazon.png
│   ├── velocidad.png
│   ├── espacio.jpg
│   ├── espacio2.jpg
│   └── derrota.jpg
├── sonidos/
│   ├── laser.wav
│   ├── muerte.wav
│   ├── daño.mp3
│   ├── item_bala.mp3
│   ├── item_vida.mp3
│   ├── item_velocidad.mp3
│   ├── iniciar.mp3
│   ├── salir.mp3
│   ├── reiniciar.mp3
│   ├── pausa.mp3
│   ├── menu.mp3
│   ├── menu_fondo.mp3
│   ├── juego_fondo.mp3
│   ├── Suspenso.mp3
│   └── mario_bros.mp3
```

---

## Cómo ejecutar el juego

1. Asegúrate de tener Python 3 instalado.
2. Instala Pygame:

```bash
pip install pygame
```

3. Coloca todas las imágenes en una carpeta `imagenes/` y los sonidos en `sonidos/`.
4. Ejecuta el juego:

```bash
python main_code.py
```

---

## 🎨 Créditos

Desarrollado por [Oliver Toro Posada, Sebastían Ramírez Osorio].  
Hecho como proyecto para la materia de [Programación II].
