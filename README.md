# ITER - Innovative Technologies and Renewable Energy

A modern, responsive website for ITER, a company specializing in renewable energy solutions, photovoltaic systems, and energy efficiency training.

## Features

- Fully responsive design optimized for all devices
- Modern and clean UI with attractive animations
- Interactive elements including sliders, counters, and filtering systems
- Contact forms with validation
- SEO-friendly structure
- Cross-browser compatible
- Complete blog system with categories and comments
- Detailed blog post pages with related articles
- Social media sharing options

## Pages

1. **Home** - Company overview and featured services
2. **Solutions** - Detailed information about renewable energy solutions
3. **Academy** - Educational programs and courses
4. **Contact** - Contact information and form
5. **About Us** - Company history and team information
6. **Blog** - Articles, news, and insights about renewable energy
7. **Blog Post** - Individual blog article page with comments

## Technology Stack

- HTML5
- CSS3 (with custom variables and flexbox/grid layouts)
- JavaScript (vanilla)
- AOS Animation Library
- Font Awesome Icons
- Google Fonts (Montserrat)

## Color Palette

- Primary: #1D3557 (Dark Blue)
- Secondary: #457B9D (Medium Blue)
- Accent: #A8DADC (Light Blue)
- Light: #F1FAEE (Off White)
- Dark: #333333 (Dark Gray)

## WordPress Integration Guide

### 1. Setting Up WordPress

1. **Install WordPress**: Set up a fresh WordPress installation on your hosting provider.
2. **Choose a Theme**: Select a minimal theme that you can customize extensively, such as:
   - Astra
   - GeneratePress
   - OceanWP
   - Blocksy

### 2. Converting HTML to WordPress Theme

#### Option 1: Using a Child Theme (Recommended for non-developers)

1. **Create a Child Theme** of your selected theme
2. **Copy CSS**: Copy all styles from `css/style.css` and `css/responsive.css` into your child theme's `style.css`
3. **Add JavaScript**: Create a `js` folder in your child theme and copy `main.js`
4. **Enqueue Scripts and Styles**: Add the following to your child theme's `functions.php`:

```php
function iter_enqueue_scripts() {
    // Enqueue AOS Animation Library
    wp_enqueue_style('aos-css', 'https://unpkg.com/aos@2.3.1/dist/aos.css');
    wp_enqueue_script('aos-js', 'https://unpkg.com/aos@2.3.1/dist/aos.js', array(), '2.3.1', true);
    
    // Enqueue Font Awesome
    wp_enqueue_style('fontawesome', 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css');
    
    // Enqueue Google Fonts
    wp_enqueue_style('google-fonts', 'https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap');
    
    // Enqueue custom scripts
    wp_enqueue_script('iter-main-js', get_stylesheet_directory_uri() . '/js/main.js', array('jquery'), '1.0', true);
}
add_action('wp_enqueue_scripts', 'iter_enqueue_scripts');
```

#### Option 2: Creating a Custom Theme (For developers)

1. **Create a Basic Theme Structure**:
   - `index.php`
   - `style.css` (with theme information)
   - `header.php`
   - `footer.php`
   - `functions.php`
   - `page-templates/` directory for custom page templates

2. **Convert HTML Pages to Templates**:
   - Create a template for each page (home, solutions, academy, etc.)
   - Move the common header to `header.php`
   - Move the common footer to `footer.php`

3. **Make Content Editable**:
   - Replace static content with WordPress functions like `the_content()`, `the_title()`, etc.
   - Use Advanced Custom Fields (ACF) plugin for complex content sections

### 3. Using Page Builders (Easiest Option)

1. **Install a Page Builder**:
   - Elementor
   - Beaver Builder
   - Divi Builder

2. **Import HTML Content**:
   - Create pages for each section (Home, Solutions, Academy, etc.)
   - Copy HTML content from the static files
   - Use the page builder to recreate the layouts

3. **Add Custom CSS**:
   - Add the custom CSS from `style.css` and `responsive.css` to the theme customizer or page builder's CSS section

4. **Add Custom JavaScript**:
   - Add the JavaScript from `main.js` to the theme customizer or use a custom JavaScript plugin

### 4. Setting Up Contact Forms

1. **Install Contact Form 7** or another form plugin
2. **Create Forms** that match the design of the contact forms in the static site
3. **Style the Forms** using custom CSS to match the design
4. **Add Form Shortcodes** to the appropriate pages

### 5. Adding Call-to-Action Elements

1. **Create Reusable Blocks** for the call-to-action sections
2. **Add the CTA HTML** to these blocks
3. **Insert the Blocks** on all relevant pages
4. **Style with CSS** to match the design

### 6. Optimizing for SEO

1. **Install Yoast SEO** or another SEO plugin
2. **Configure Meta Titles and Descriptions** for all pages
3. **Add Alt Text** to all images
4. **Create an XML Sitemap**
5. **Connect to Google Search Console**

### 7. Adding the Floating Contact Button

1. **Use a Plugin** like "Floating Button" or "Sticky Buttons"
2. **Configure the Button** to match the design in the static site
3. **Add Custom CSS** to style the button

### 8. Performance Optimization

1. **Install a Caching Plugin** like WP Rocket or W3 Total Cache
2. **Optimize Images** using a plugin like Smush or ShortPixel
3. **Minify CSS and JavaScript**
4. **Enable GZIP Compression**
5. **Use a CDN** for faster content delivery

### 9. Testing and Launching

1. **Test Responsiveness** on multiple devices
2. **Check Browser Compatibility**
3. **Test Form Submissions**
4. **Verify All Links Work**
5. **Launch the Site**

## Maintenance

Regular updates are recommended for:
- WordPress core
- Theme and plugins
- Content freshness
- Security monitoring
- Performance optimization

## Support

For any questions or support needs, please contact:
- Email: info@iterge.com
- Phone: +123 456 789

## Estructura del Proyecto

```
ITER WEB/
├── index.html                # Página principal
├── soluciones.html           # Página de soluciones
├── academia.html             # Página de academia
├── contacto.html             # Página de contacto
├── about-us.html             # Página sobre nosotros
├── blog.html                 # Página de blog
├── blog-post.html            # Página de artículo individual del blog
├── css/
│   ├── style.css             # Estilos principales
│   ├── responsive.css        # Estilos responsivos
│   └── animations.css        # Animaciones
├── js/
│   └── main.js               # JavaScript principal
└── images/                   # Directorio de imágenes
```

## Características

- Diseño moderno y atractivo
- Totalmente responsive (adaptable a móviles, tablets y escritorio)
- Animaciones suaves con AOS (Animate On Scroll)
- Sección de servicios con diseño masonry
- Slider de testimonios
- Contador de estadísticas animado
- Filtro de proyectos
- Formulario de contacto con validación
- Sección de FAQ con acordeón
- Optimizado para SEO

## Tecnologías Utilizadas

- HTML5
- CSS3 (Variables CSS, Flexbox, Grid)
- JavaScript (ES6+)
- Font Awesome (iconos)
- Google Fonts
- AOS (Animate On Scroll)

## Implementación

1. Clona este repositorio:
```
git clone https://github.com/tu-usuario/iter-web.git
```

2. Abre el archivo `index.html` en tu navegador para ver el sitio localmente.

3. Para implementar en producción, sube todos los archivos a tu servidor web o plataforma de hosting.

## Personalización

- **Colores**: Los colores principales se definen como variables CSS en el archivo `style.css`.
- **Fuentes**: El sitio utiliza la fuente Montserrat de Google Fonts.
- **Imágenes**: Reemplaza las imágenes en el directorio `images/` con tus propias imágenes.
- **Contenido**: Edita los archivos HTML para actualizar el contenido según tus necesidades.

## Compatibilidad con Navegadores

El sitio es compatible con las últimas versiones de:
- Google Chrome
- Mozilla Firefox
- Safari
- Microsoft Edge
- Opera

## Optimización

Para mejorar el rendimiento en producción:
- Minifica los archivos CSS y JavaScript
- Optimiza las imágenes
- Considera implementar un sistema de caché
- Utiliza un CDN para los recursos estáticos

## Licencia

Este proyecto está bajo la licencia MIT.

## Contacto

Para cualquier consulta o sugerencia, por favor contacta a [info@iterge.com](mailto:info@iterge.com).

---

© 2024 Innovative Technologies and Renewable Energy (ITER) 