# 📺 Panel Institucional Interactivo - Televisores-Establecimiento

Panel dinámico de información institucional diseñado para pantallas públicas (TVs) en establecimientos educacionales. Muestra en tiempo real: clima, horarios escolares, pronóstico del tiempo y carrusel de imágenes.

**[Visualizar Proyecto](https://github.com/Pedro-Fernandez-M/Televisores-Establecimiento)**

---

## 🎯 Características Principales

✨ **Información en Tiempo Real**
- Clima actual y pronóstico de 5 días
- Hora y fecha actualizados en vivo (zona horaria Chile)
- Estado actual de la escuela (en clases, recreo, almuerzo, desayuno)

📊 **Interfaz Responsiva**
- Diseño adaptable a cualquier tamaño de pantalla
- Optimizado para pantallas grandes (TVs, monitores)
- Escalado automático para diferentes resoluciones (1920px, 2560px+)

🎨 **Experiencia Visual Mejorada**
- Carrusel automático de imágenes
- Gradientes modernos y diseño limpio
- Animaciones suaves y transiciones
- Modos de accesibilidad (alto contraste, texto grande)

⚙️ **Sistema de Horarios Escolares**
- Detección automática de actividades escolares
- Diferenciación de fin de semana y horarios fuera de clase
- Indicadores visuales con colores por actividad

📱 **Sin Interacción de Usuario**
- Interfaz optimizada para modo autoejecución en TVs
- Eliminación de cursores y elementos de control
- Caché de datos para mejor rendimiento

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Tecnología |
|-----------|-----------|
| **Frontend** | HTML5, CSS3, JavaScript (Vanilla) |
| **APIs Externas** | OpenWeatherMap API |
| **Diseño** | CSS Grid, Flexbox, Media Queries |
| **Optimización** | Lazy Loading, Responsive Design |
| **Control de Versiones** | Git, GitHub, Git LFS (para archivos grandes) |

---

## 📋 Requisitos Previos

- Navegador web moderno (Chrome, Firefox, Edge, Safari)
- Conexión a Internet (para obtener datos de clima)
- Clave API de OpenWeatherMap (gratuita)

---

## 🚀 Instalación y Uso

### 1. **Clonar el Repositorio**
```bash
git clone https://github.com/Pedro-Fernandez-M/Televisores-Establecimiento.git
cd Televisores-Establecimiento
```

### 2. **Abrir en el Navegador**
```bash
# Opción 1: Abrir directamente el archivo
open index.html

# Opción 2: Usar un servidor local (recomendado)
python -m http.server 8000
# Luego acceder a: http://localhost:8000
```

### 3. **Configurar API del Clima** (Opcional pero recomendado)
1. Crear cuenta en [OpenWeatherMap](https://openweathermap.org/api)
2. Obtener clave API gratuita
3. Editar `index.html` y reemplazar la URL de la API con tu clave:
```javascript
const WEATHER_API_URL = 'https://api.openweathermap.org/data/2.5/weather?lat=...&lon=...&appid=TU_CLAVE_AQUI';
```

---

## 📁 Estructura del Proyecto

```
Televisores-Establecimiento/
├── index.html                 # Archivo principal (HTML + CSS + JS)
├── imagenes/                  # Carpeta con imágenes para carrusel
│   ├── 1.jpg
│   ├── 2.jpg
│   ├── imagen 6.png
│   ├── imagen 7.png
│   └── ...
├── videos/                    # Carpeta con videos (opcional)
│   ├── caida 1.mp4
│   ├── caida 2.mp4
│   └── ...
├── LOGO1.png                  # Logo institución 1
├── LOGO2.png                  # Logo institución 2
├── LOGO3.png                  # Logo institución 3
├── .gitattributes             # Configuración Git LFS
└── README.md                  # Este archivo

```

---

## 🎛️ Personalización

### Cambiar Información de la Escuela
Edita la línea en `index.html`:
```html
<h1>🎓 Liceo Bicentenario Industrial Ingeniero Ricardo Fenner Ruedi 🎓</h1>
```

### Modificar Horarios Escolares
Localiza el objeto `SCHED` en el script y actualiza los tiempos:
```javascript
const SCHED = {
    weekdays: {
        '07:00-08:18': { activity: 'Desayuno', icon: '🍞', cls: 'desayuno' },
        '08:19-09:49': { activity: 'En Clases', icon: '📚', cls: 'clases' },
        // ... más horarios
    }
}
```

### Agregar Imágenes al Carrusel
1. Coloca las imágenes en la carpeta `/imagenes/`
2. El sistema las detecta automáticamente
3. Se rotarán cada 5 segundos

---

## 🔐 Configuración de Seguridad

- Incluye validación de imágenes (fallback si no cargan)
- Manejo de errores para solicitudes de API
- Sin almacenamiento sensible en cliente

---

## 📊 Datos de Ejemplo

- **Ubicación:** La Unión, Los Ríos, Chile
- **Zona Horaria:** UTC-4 (Chile, región sur)
- **Horario Escolar:** 7:00 AM - 5:20 PM (lunes a viernes)
- **Pronóstico:** 5 días adelante con niveles UV

---

## 🎓 Detalles Técnicos

### Rendimiento
- Carga inicial < 2 segundos
- Actualización de clima: cada 30 minutos
- Carrusel de imágenes: cada 5 segundos
- Hora actualizada: cada segundo

### Compatibilidad
- ✅ Chrome/Chromium 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### Accesibilidad
- Soporta modo de alto contraste
- Texto escalable para lectores de pantalla
- Etiquetas semánticas HTML5

---

## 🚀 Despliegue

### GitHub Pages
1. Este proyecto es perfectamente compatible con GitHub Pages
2. El sitio puede verse en vivo desde el repositorio
3. Perfecto para desplegar en una TV/monitor con conexión a Internet

### Servidor Local
Para usar en una red local sin Internet público:
```bash
python -m http.server 8000
# Acceder desde otras máquinas: http://IP_LOCAL:8000
```

---

## 📝 Licencia

Este proyecto es de código abierto y está disponible para uso libre en establecimientos educacionales.

---

## 👨‍💻 Autor

**Pedro Fernández M.**
- 📧 Email: [tu-email@ejemplo.com]
- 🔗 GitHub: [Pedro-Fernandez-M](https://github.com/Pedro-Fernandez-M)
- 💼 LinkedIn: [Tu perfil LinkedIn]

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si encuentras un bug o tienes ideas de mejora:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/MejoraMi`)
3. Commit tus cambios (`git commit -am 'Agrega MejoraMi'`)
4. Push a la rama (`git push origin feature/MejoraMi`)
5. Abre un Pull Request

---

## 📌 Versión Actual

**v1.0.0** - Release inicial
- Panel funcional con clima en tiempo real
- Carrusel de imágenes
- Sistema de horarios escolares
- Optimización para pantallas grandes

---

## 🔄 Próximas Mejoras Planeadas

- [ ] Base de datos para configurar múltiples establecimientos
- [ ] Dashboard de administración
- [ ] Soporte para múltiples idiomas
- [ ] Integración con calendario escolar
- [ ] Sistema de notificaciones
- [ ] Analytics y estadísticas

---

## ⚠️ Troubleshooting

### El clima no se carga
- Verifica conexión a Internet
- Comprueba que la API key sea válida
- Revisa la consola del navegador (F12) para errores

### Las imágenes no aparecen
- Asegúrate que estén en la carpeta `/imagenes/`
- Verifica los nombres de archivo (sensibles a mayúsculas)
- El sistema carga automáticamente .jpg, .png, .gif, .webp

### Los horarios no coinciden
- Verifica que estés en la zona horaria correcta
- Comprueba que los tiempos en `SCHED` sean válidos (HH:MM)

---

## 📚 Recursos Útiles

- [OpenWeatherMap API Docs](https://openweathermap.org/api)
- [MDN Web Docs - CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Git LFS Documentation](https://git-lfs.github.com/)

---

**⭐ Si este proyecto te fue útil, considera darle una estrella en GitHub!**

