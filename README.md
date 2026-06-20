# HGW Landing Page - GitHub Pages

Landing page moderna y responsive diseñada para HGW (Bienestar que Transforma tu Vida), optimizada para convertir visitantes en prospectos y generar confianza.

## 🚀 Características

- **Diseño Moderno**: Interfaz elegante con la paleta de colores HGW
- **Responsive**: Se adapta perfectamente a todos los dispositivos (móvil, tablet, desktop)
- **TailwindCSS**: Estilizado con TailwindCSS vía CDN para fácil mantenimiento
- **Interactivo**: Menú móvil, scroll suave, animaciones al scroll
- **SEO Friendly**: Meta tags optimizados para motores de búsqueda
- **Rápido**: Sin dependencias de build, carga instantánea
- **Botón WhatsApp**: Botón flotante para contacto directo
- **Animaciones**: Efectos fade-in al hacer scroll

## 📋 Secciones

1. **Hero**: "BIENESTAR QUE TRANSFORMA TU VIDA" con CTAs
2. **¿Qué es HGW?**: Tres pilares (Bienestar, Ahorro, Oportunidad)
3. **Productos Destacados**: Grid con productos HGW (Berry Coffee, Choco Gano, Tourmaline Toothpaste, etc.)
4. **¿Por qué HGW?**: Beneficios y razones para elegir HGW
5. **Historias de Transformación**: Testimonios de usuarios
6. **El Ecosistema HGW**: Flujo visual del modelo de negocio
7. **Sobre Edgar**: Presentación personal
8. **CTA Final**: Llamada a la acción con WhatsApp

## 🎨 Paleta de Colores HGW

- **Verde Principal**: #1E7D3A
- **Verde Secundario**: #6DBE45
- **Naranja Acción**: #F47C20
- **Amarillo**: #F5B400
- **Blanco**: #FFFFFF

## � Tipografías

- **Montserrat**: Bold para títulos, SemiBold para subtítulos
- **Lato**: Para texto corporativo

## 📦 Despliegue en GitHub Pages

### Opción 1: Desde la rama principal (main)

1. **Crea un nuevo repositorio en GitHub**
   - Ve a github.com y crea un nuevo repositorio
   - Puedes llamarlo `landing-page` o el nombre que prefieras

2. **Sube los archivos a GitHub**
   
   Si ya tienes Git instalado:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/TU_REPOSITORIO.git
   git push -u origin main
   ```

3. **Activa GitHub Pages**
   - Ve a la pestaña "Settings" de tu repositorio
   - En el menú lateral, haz clic en "Pages"
   - En "Build and deployment" > "Source", selecciona "Deploy from a branch"
   - En "Branch", selecciona "main" y la carpeta "/ (root)"
   - Haz clic en "Save"

4. **Espera unos minutos**
   - GitHub desplegará tu sitio
   - Verás el enlace en la sección de Pages (ej: `https://TU_USUARIO.github.io/TU_REPOSITORIO/`)

### Opción 2: Usando GitHub Actions (Automático)

Este repositorio incluye un workflow de GitHub Actions para despliegue automático. Solo necesitas:

1. Subir los archivos a GitHub (como en el paso 2 anterior)
2. El workflow se activará automáticamente con cada push a la rama main
3. Tu sitio se desplegará automáticamente

## 🎨 Personalización

### Cambiar número de WhatsApp

El número de WhatsApp aparece en 3 lugares. Actualmente configurado: `+573181972223`

Para cambiarlo, busca y reemplaza `573181972223` con tu número:

1. **Botón flotante** (línea ~671):
   ```html
   <a href="https://wa.me/TU_NUMERO?text=Hola,%20me%20interesa%20conocer%20más%20sobre%20HGW"
   ```

2. **CTA Final** (línea ~619):
   ```html
   <a href="https://wa.me/TU_NUMERO?text=Hola,%20me%20interesa%20conocer%20más%20sobre%20HGW"
   ```

3. **Footer** (línea ~646):
   ```html
   <a href="https://wa.me/TU_NUMERO"
   ```

### Cambiar colores HGW

Los colores están definidos en CSS variables (líneas 13-18):
```css
:root {
    --hgw-green-primary: #1E7D3A;
    --hgw-green-secondary: #6DBE45;
    --hgw-orange: #F47C20;
    --hgw-yellow: #F5B400;
    --hgw-white: #FFFFFF;
}
```

### Cambiar contenido

Edita directamente el texto en `index.html`:
- **Hero**: Título y subtítulo principal
- **Productos**: Nombres, descripciones y beneficios
- **Testimonios**: Nombres y textos de usuarios
- **Sobre Edgar**: Tu información personal
- **Redes sociales**: Enlaces en el footer

### Agregar imágenes de productos reales

Para usar las imágenes reales de los productos:
1. Crea una carpeta `images` en el proyecto
2. Agrega tus imágenes de productos
3. Reemplaza los emojis en las cards de productos por:
   ```html
   <img src="images/berry-coffee.jpg" alt="Berry Coffee" class="w-full h-full object-cover">
   ```

## 📱 Vista Previa Local

Para ver la landing page en tu computadora antes de subirla:

1. Abre `index.html` directamente en tu navegador
2. O usa un servidor local:
   ```bash
   # Con Python
   python -m http.server 8000
   
   # Con Node.js (instala http-server primero)
   npx http-server
   ```
3. Abre `http://localhost:8000` en tu navegador

## �️ Tecnologías

- HTML5
- CSS3 (TailwindCSS vía CDN)
- JavaScript (Vanilla)
- Google Fonts (Montserrat, Lato)

## 🚨 Solución de Problemas

### El sitio no se despliega

- Verifica que el archivo `index.html` esté en la raíz del repositorio
- Asegúrate de que la rama sea `main` (no `master`)
- Revisa la pestaña "Actions" en GitHub para ver errores del workflow

### Los estilos no cargan

- Verifica tu conexión a internet (TailwindCSS se carga vía CDN)
- Espera unos minutos después del despliegue para que GitHub procese los cambios

### El botón de WhatsApp no funciona

- Verifica que el número de WhatsApp sea correcto (formato: código país + número)
- Asegúrate de incluir el código de país (ej: 52 para México)
- El formato debe ser: `https://wa.me/5212345678900`

### Las animaciones no se ven

- Verifica que JavaScript esté habilitado en tu navegador
- Revisa la consola para errores de JavaScript
- Las animaciones usan IntersectionObserver, soportado en navegadores modernos

## 📝 Licencia

Este proyecto es de código abierto y está disponible para uso personal y comercial.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si encuentras algún bug o tienes sugerencias:

1. Haz un fork del proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📧 Contacto

Para soporte o preguntas sobre la landing page de HGW, contacta a través de WhatsApp.

---

**Hecho con ❤️ para HGW - Bienestar que Transforma tu Vida**
