# Animos Yuli 💖

Una hermosa página web de apoyo emocional con animaciones y diseño responsive.

## 🎨 Características

- **Fondo GIF a pantalla completa**: Un GIF animado cubre toda la pantalla
- **Imágenes flotantes animadas**: Imágenes que se agrandan y contraen flotando en cajas invisibles
- **Diseño responsive**:
  - 💻 **Desktop**: Imágenes en los laterales izquierdo y derecho
  - 📱 **Mobile**: Imágenes en la parte superior e inferior
- **Mensaje central**: "Animos Yuli <3" con efecto degradado arcoíris y pequeño GIF de fondo
- **Efectos visuales**: Glassmorphism, sombras, animaciones suaves

## 📁 Estructura del Proyecto

```
animos/
├── public/
│   └── assets/
│       ├── gifs/           # GIFs para fondo y centro
│       └── images/         # Imágenes flotantes
├── src/
│   ├── components/
│   │   ├── BackgroundGif.astro      # GIF de fondo
│   │   ├── CenterMessage.astro       # Mensaje central
│   │   └── FloatingImages.astro      # Imágenes animadas
│   ├── layouts/
│   │   └── MainLayout.astro          # Layout principal
│   └── pages/
│       └── index.astro               # Página principal
```

## 🚀 Cómo Usar

### 1. Agregar tus recursos

Coloca tus imágenes y GIFs en las carpetas correspondientes:

- **GIFs**: `public/assets/gifs/`
  - `background.gif` - GIF de fondo a pantalla completa
  - `center.gif` - Pequeño GIF detrás del mensaje central

- **Imágenes**: `public/assets/images/`
  - Agrega las imágenes que quieres que floten (estrellas, corazones, emojis, etc.)

### 2. Actualizar rutas en index.astro

Edita `src/pages/index.astro` y actualiza las rutas de los assets:

```astro
const backgroundGif = '/assets/gifs/tu-gif-fondo.gif';
const centerGif = '/assets/gifs/tu-gif-centro.gif';

const leftImages = [
  '/assets/images/tu-imagen-1.png',
  '/assets/images/tu-imagen-2.png',
  // ... más imágenes
];
```

### 3. Ejecutar el proyecto

```bash
# Instalar dependencias (si es necesario)
npm install

# Iniciar servidor de desarrollo
npm run dev
```

Visita `http://localhost:4321` para ver tu página.

## 🎨 Personalización

### Cambiar el mensaje

Edita la prop `message` en `index.astro`:

```astro
<CenterMessage message="Tu mensaje aquí <3" centerGifSrc={centerGif} />
```

### Ajustar animaciones

Los componentes tienen estilos CSS personalizables:

- **Velocidad de flotación**: Modifica `animation: float-and-scale 4s` en `FloatingImages.astro`
- **Colores del degradado**: Cambia los colores en `.message` en `CenterMessage.astro`
- **Tamaño de imágenes**: Ajusta `width` y `height` en `.floating-image img`

### Responsive breakpoints

El diseño cambia a móvil en `768px`. Para ajustar:

```css
@media (max-width: 768px) {
  /* Estilos mobile */
}
```

## 🧞 Comandos

| Comando                   | Acción                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Instala las dependencias                         |
| `npm run dev`             | Inicia servidor de desarrollo en `localhost:4321`|
| `npm run build`           | Construye el sitio para producción en `./dist/`  |
| `npm run preview`         | Previsualiza la build localmente                 |

## 🛠️ Tecnologías

- **Astro** - Framework web
- **TypeScript** - Tipado estático
- **CSS** - Animaciones y estilos personalizados

## 📝 Notas

- Los archivos de recursos son placeholders. Debes agregar tus propias imágenes y GIFs.
- Las imágenes flotantes se posicionan aleatoriamente cada vez que se carga la página.
- El diseño usa `overflow: hidden` para evitar scroll y mantener todo visible en pantalla.

## 💖 Creado con amor

Esta página fue diseñada para dar ánimos y apoyo emocional de la forma más bonita posible.

---

¡Disfruta dando porras a Yuli! 🎉
