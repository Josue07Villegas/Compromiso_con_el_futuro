<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un Compromiso con el Futuro - ODS 6</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #e3f2fd 0%, #f0f9ff 100%);
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #1976d2, #0d47a1);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-menu a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-menu a:hover {
            color: #81d4fa;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #1976d2, #4fc3f7);
            color: white;
            text-align: center;
            padding: 120px 2rem 80px;
            margin-top: 60px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120"><path d="M0,96L48,112C96,128,192,160,288,160C384,160,480,128,576,122.7C672,117,768,139,864,149.3C960,160,1056,160,1152,149.3L1200,139L1200,0L1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z" fill="rgba(255,255,255,0.1)"/></svg>') no-repeat bottom;
            background-size: cover;
        }

        .hero-content {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease-out;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.95;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .cta-button {
            background: linear-gradient(45deg, #4caf50, #2e7d32);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.4);
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(76, 175, 80, 0.6);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Section Styles */
        .section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #1976d2;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(45deg, #4caf50, #2196f3);
            border-radius: 2px;
        }

        /* Problem Section */
        .problem {
            background: white;
            border-radius: 20px;
            padding: 3rem;
            margin: 2rem 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .stat-card {
            background: linear-gradient(135deg, #e3f2fd, #f0f9ff);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            border-left: 5px solid #2196f3;
            transition: transform 0.3s;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #1976d2;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: #666;
            font-size: 1.1rem;
        }

        /* Actions Section */
        .actions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .action-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s;
            border-top: 5px solid #4caf50;
        }

        .action-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .action-icon {
            font-size: 3rem;
            color: #4caf50;
            margin-bottom: 1rem;
        }

        .action-title {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #1976d2;
        }

        .action-description {
            color: #666;
            line-height: 1.6;
        }

        /* Results Section */
        .results {
            background: linear-gradient(135deg, #e8f5e8, #f1f8e9);
            padding: 4rem 0;
        }

        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .result-item {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        .result-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(45deg, #4caf50, #2e7d32);
        }

        .result-value {
            font-size: 2.5rem;
            font-weight: bold;
            color: #2e7d32;
            margin-bottom: 0.5rem;
        }

        .result-label {
            color: #666;
            font-size: 1.1rem;
        }

        /* Testimonials */
        .testimonials {
            padding: 4rem 0;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .testimonial {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            position: relative;
        }

        .testimonial::before {
            content: '"';
            position: absolute;
            top: -10px;
            left: 20px;
            font-size: 4rem;
            color: #4caf50;
            opacity: 0.3;
        }

        .testimonial-text {
            font-style: italic;
            color: #666;
            margin-bottom: 1rem;
            line-height: 1.6;
        }

        .testimonial-author {
            font-weight: bold;
            color: #1976d2;
        }

        /* Contact Form */
        .contact {
            background: linear-gradient(135deg, #1976d2, #0d47a1);
            color: white;
            padding: 4rem 0;
        }

        .form-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            background: rgba(255,255,255,0.9);
        }

        .form-group textarea {
            height: 120px;
            resize: vertical;
        }

        .submit-btn {
            background: linear-gradient(45deg, #4caf50, #2e7d32);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            width: 100%;
        }

        .submit-btn:hover {
            background: linear-gradient(45deg, #2e7d32, #1b5e20);
            transform: translateY(-2px);
        }

        /* Social Share */
        .social-share {
            text-align: center;
            padding: 3rem 0;
            background: #f5f5f5;
        }

        .social-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-btn {
            display: inline-flex;
            align-items: center;
            padding: 10px 20px;
            border-radius: 25px;
            text-decoration: none;
            color: white;
            font-weight: 500;
            transition: transform 0.3s;
        }

        .social-btn:hover {
            transform: translateY(-3px);
        }

        .social-btn.facebook { background: #3b5998; }
        .social-btn.twitter { background: #1da1f2; }
        .social-btn.whatsapp { background: #25d366; }
        .social-btn.linkedin { background: #0077b5; }

        /* Bibliography */
        .bibliography {
            background: white;
            padding: 3rem 0;
        }

        .bibliography-list {
            max-width: 800px;
            margin: 0 auto;
            list-style: none;
        }

        .bibliography-list li {
            margin-bottom: 1rem;
            padding: 1rem;
            background: #f9f9f9;
            border-left: 4px solid #2196f3;
            border-radius: 5px;
        }

        /* Footer */
        .footer {
            background: #263238;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .stats-grid,
            .actions-grid,
            .results-grid,
            .testimonials-grid {
                grid-template-columns: 1fr;
            }

            .social-buttons {
                flex-wrap: wrap;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease-out;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="nav-container">
            <div class="logo">
                <i class="fas fa-water"></i> Un Compromiso con el Futuro
            </div>
            <nav>
                <ul class="nav-menu">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#antecedentes">Problemática</a></li>
                    <li><a href="#acciones">Acciones</a></li>
                    <li><a href="#resultados">Resultados</a></li>
                    <li><a href="#testimonios">Testimonios</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="inicio" class="hero">
        <div class="hero-content">
            <h1>Un Compromiso con el Futuro</h1>
            <p>Transformando comunidades urbanas de Nuevo León a través del acceso al agua limpia y saneamiento. Juntos podemos lograr el ODS 6 y construir un futuro sostenible.</p>
            <a href="#contacto" class="cta-button">
                <i class="fas fa-hand-holding-water"></i> Participa Ahora
            </a>
        </div>
    </section>

    <!-- Problem Section -->
    <section id="antecedentes" class="section">
        <div class="container">
            <h2 class="section-title fade-in">La Problemática del Agua</h2>
            <div class="problem fade-in">
                <p style="font-size: 1.2rem; text-align: center; margin-bottom: 2rem; color: #666;">
                    El acceso al agua limpia y saneamiento es un derecho humano fundamental que enfrenta serios desafíos 
                    en nuestras comunidades urbanas de Nuevo León.
                </p>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number">2,200M</div>
                        <div class="stat-label">personas sin acceso a agua potable segura a nivel mundial</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">9.4M</div>
                        <div class="stat-label">mexicanos sin acceso a agua potable</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">35%</div>
                        <div class="stat-label">del agua se pierde por fugas en Nuevo León</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">5.7M</div>
                        <div class="stat-label">habitantes en Nuevo León afectados por estrés hídrico</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Actions Section -->
    <section id="acciones" class="section">
        <div class="container">
            <h2 class="section-title fade-in">Nuestras Acciones Propuestas</h2>
            <div class="actions-grid">
                <div class="action-card fade-in">
                    <div class="action-icon">
                        <i class="fas fa-bullhorn"></i>
                    </div>
                    <h3 class="action-title">Campaña "Cada Gota Cuenta"</h3>
                    <p class="action-description">
                        Talleres comunitarios, distribución de material educativo y contenido digital 
                        para concientizar sobre el uso responsable del agua en municipios urbanos.
                    </p>
                </div>
                
                <div class="action-card fade-in">
                    <div class="action-icon">
                        <i class="fas fa-cloud-rain"></i>
                    </div>
                    <h3 class="action-title">Sistemas de Recolección Pluvial</h3>
                    <p class="action-description">
                        Instalación de sistemas en centros comunitarios con capacitación para 
                        mantenimiento y monitoreo de eficiencia.
                    </p>
                </div>
                
                <div class="action-card fade-in">
                    <div class="action-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3 class="action-title">Red de Comunidades Sustentables</h3>
                    <p class="action-description">
                        Certificación "Comunidad Amiga del Agua", intercambio de mejores prácticas 
                        y competencias intermunicipales.
                    </p>
                </div>
                
                <div class="action-card fade-in">
                    <div class="action-icon">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3 class="action-title">Observatorio Ciudadano del Agua</h3>
                    <p class="action-description">
                        Monitoreo ciudadano de calidad del agua, publicación de informes trimestrales 
                        y propuestas de política pública.
                    </p>
                </div>
                
                <div class="action-card fade-in">
                    <div class="action-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3 class="action-title">App de Reporte Ciudadano</h3>
                    <p class="action-description">
                        Aplicación móvil para que los ciudadanos reporten fugas, problemas de calidad 
                        y coordinen con autoridades municipales.
                    </p>
                </div>
                
                <div class="action-card fade-in">
                    <div class="action-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3 class="action-title">Educación Comunitaria</h3>
                    <p class="action-description">
                        Talleres educativos sobre el ciclo del agua, técnicas de conservación y 
                        mejores prácticas para hogares urbanos.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Results Section -->
    <section id="resultados" class="results">
        <div class="container">
            <h2 class="section-title fade-in">Resultados Esperados</h2>
            <div class="results-grid">
                <div class="result-item fade-in">
                    <div class="result-value">1,000</div>
                    <div class="result-label">Personas Capacitadas</div>
                </div>
                <div class="result-item fade-in">
                    <div class="result-value">25%</div>
                    <div class="result-label">Reducción en Reportes de Fugas</div>
                </div>
                <div class="result-item fade-in">
                    <div class="result-value">10,000L</div>
                    <div class="result-label">Agua Pluvial Recolectada</div>
                </div>
                <div class="result-item fade-in">
                    <div class="result-value">5</div>
                    <div class="result-label">Comunidades Certificadas</div>
                </div>
                <div class="result-item fade-in">
                    <div class="result-value">20</div>
                    <div class="result-label">Voluntarios Activos</div>
                </div>
                <div class="result-item fade-in">
                    <div class="result-value">$40,000</div>
                    <div class="result-label">Inversión Total MXN</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonios" class="testimonials">
        <div class="container">
            <h2 class="section-title fade-in">Testimonios del Equipo</h2>
            <div class="testimonials-grid">
                <div class="testimonial fade-in">
                    <p class="testimonial-text">
                        "Como estudiante, puedo contribuir con acciones pequeñas pero significativas. 
                        Me entusiasma la posibilidad de llevar a cabo un proyecto que impacte de forma 
                        positiva en mi entorno urbano."
                    </p>
                    <p class="testimonial-author">- Josué Abel Villegas García</p>
                </div>
                
                <div class="testimonial fade-in">
                    <p class="testimonial-text">
                        "Tener acceso a una buena educación y a agua limpia son derechos básicos. 
                        Si cada persona pone su parte, se pueden lograr grandes cambios. El futuro 
                        depende del compromiso de todos."
                    </p>
                    <p class="testimonial-author">- Emiliano Castillo Loredo</p>
                </div>
                
                <div class="testimonial fade-in">
                    <p class="testimonial-text">
                        "Como estudiantes, tenemos la responsabilidad de ser agentes de cambio, 
                        contribuyendo activamente desde nuestro entorno con acciones concretas que 
                        impulsen el desarrollo sostenible."
                    </p>
                    <p class="testimonial-author">- Mauricio Joab Heredia Flores</p>
                </div>
                
                <div class="testimonial fade-in">
                    <p class="testimonial-text">
                        "El verdadero cambio comienza cuando cada persona asume la responsabilidad 
                        de informarse, actuar y motivar a su comunidad hacia una gestión más justa 
                        y sostenible del agua."
                    </p>
                    <p class="testimonial-author">- Sabdiel Edrei Sauza Ramirez</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="contact">
        <div class="container">
            <h2 class="section-title" style="color: white;">¡Únete a Nuestro Compromiso!</h2>
            <div class="form-container">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="nombre">Nombre Completo</label>
                        <input type="text" id="nombre" name="nombre" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Correo Electrónico</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="municipio">Municipio</label>
                        <input type="text" id="municipio" name="municipio" placeholder="ej. Monterrey, Guadalupe, San Nicolás">
                    </div>
                    <div class="form-group">
                        <label for="mensaje">¿Cómo te gustaría participar?</label>
                        <textarea id="mensaje" name="mensaje" placeholder="Cuéntanos cómo quieres contribuir al proyecto..."></textarea>
                    </div>
                    <button type="submit" class="submit-btn">
                        <i class="fas fa-paper-plane"></i> Enviar Mensaje
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Social Share -->
    <section class="social-share">
        <div class="container">
            <h3>Comparte Nuestro Compromiso</h3>
            <div class="social-buttons">
                <a href="#" class="social-btn facebook" onclick="shareOnFacebook()">
                    <i class="fab fa-facebook-f"></i> Facebook
                </a>
                <a href="#" class="social-btn twitter" onclick="shareOnTwitter()">
                    <i class="fab fa-twitter"></i> Twitter
                </a>
                <a href="#" class="social-btn whatsapp" onclick="shareOnWhatsApp()">
                    <i class="fab fa-whatsapp"></i> WhatsApp
                </a>
                <a href="#" class="social-btn linkedin" onclick="shareOnLinkedIn()">
                    <i class="fab fa-linkedin-in"></i> LinkedIn
                </a>
            </div>
        </div>
    </section>

    <!-- Bibliography -->
    <section class="bibliography">
        <div class="container">
            <h2 class="section-title">Fuentes de Información</h2>
            <ul class="bibliography-list">
                <li>Organización de las Naciones Unidas. (2024). Informe sobre el Desarrollo de los Recursos Hídricos en el Mundo 2024. UNESCO.</li>
                <li>Comisión Nacional del Agua. (2024). Estadísticas del Agua en México 2024. CONAGUA.</li>
                <li>Organización Mundial de la Salud. (2024). Agua, Saneamiento e Higiene: Datos y Cifras. OMS.</li>
                <li>Gobierno del Estado de Nuevo León. (2024). Plan Estatal de Desarrollo 2022-2027: Eje Medio Ambiente.</li>
                <li>UN-Water. (2024). SDG 6 Synthesis Report 2024 on Water and Sanitation. United Nations.</li>
            </ul>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2025 Un Compromiso con el Futuro - ODS 6. Proyecto estudiantil para el cambio social.</p>
            <p>Materia: Directrices para el Cambio Social | Maestra: Maria Antonieta Silva Herrera</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Fade in animation on scroll
        function animateOnScroll() {
            const elements = document.querySelectorAll('.fade-in');
            
            elements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < window.innerHeight - elementVisible) {
                    element.classList.add('visible');
                }
            });
        }

        window.addEventListener('scroll', animateOnScroll);
        animateOnScroll(); // Run on load

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Show success message
            alert('¡Gracias por tu interés! Te contactaremos pronto para que puedas ser parte de nuestro compromiso con el futuro.');
            
            // Reset form
            this.reset();
        });

        // Social sharing functions
        function shareOnFacebook() {
            const url = encodeURIComponent(window.location.href);
            const text = encodeURIComponent('Un Compromiso con el Futuro - Proyecto ODS 6 para comunidades urbanas de Nuevo León');
            window.open(`https://www.facebook.com/sharer/sharer.php?u=${url}`, '_blank', 'width=600,height=400');
        }

        function shareOnTwitter() {
            const url = encodeURIComponent(window.location.href);
            const text = encodeURIComponent('Un Compromiso con el Futuro - Proyecto ODS 6 para agua limpia y saneamiento en Nuevo León 💧 #ODS6 #AguaLimpia #NuevoLeon');
            window.open(`https://twitter.com/intent/tweet?text=${text}&url=${url}`, '_blank', 'width=600,height=400');
        }

        function shareOnWhatsApp() {
            const url = encodeURIComponent(window.location.href);
            const text = encodeURIComponent('¡Mira este proyecto sobre agua limpia y saneamiento en Nuevo León! Un Compromiso con el Futuro - ODS 6: ' + url);
            window.open(`https://wa.me/?text=${text}`, '_blank');
        }

        function shareOnLinkedIn() {
            const url = encodeURIComponent(window.location.href);
            const title = encodeURIComponent('Un Compromiso con el Futuro - Proyecto ODS 6');
            const summary = encodeURIComponent('Proyecto estudiantil para promover el acceso al agua limpia y saneamiento en comunidades urbanas de Nuevo León');
            window.open(`https://www.linkedin.com/sharing/share-offsite/?url=${url}`, '_blank', 'width=600,height=400');
        }

        // Counter animation for results
        function animateCounters() {
            const counters = document.querySelectorAll('.result-value');
            const speed = 200;

            counters.forEach(counter => {
                const animate = () => {
                    const value = +counter.getAttribute('data-target') || +counter.innerText.replace(/[^0-9]/g, '');
                    const data = +counter.innerText.replace(/[^0-9]/g, '');
                    
                    const time = value / speed;
                    
                    if (data < value) {
                        counter.innerText = Math.ceil(data + time);
                        setTimeout(animate, 1);
                    } else {
                        counter.innerText = counter.getAttribute('data-original') || counter.innerText;
                    }
                };
                
                // Store original text
                if (!counter.getAttribute('data-original')) {
                    counter.setAttribute('data-original', counter.innerText);
                    counter.setAttribute('data-target', counter.innerText.replace(/[^0-9]/g, ''));
                }
                
                animate();
            });
        }

        // Run counter animation when results section is visible
        const resultsSection = document.getElementById('resultados');
        let countersAnimated = false;

        function checkResultsSection() {
            if (resultsSection && !countersAnimated) {
                const rect = resultsSection.getBoundingClientRect();
                if (rect.top < window.innerHeight && rect.bottom > 0) {
                    animateCounters();
                    countersAnimated = true;
                }
            }
        }

        window.addEventListener('scroll', checkResultsSection);
        
        // Mobile menu toggle (for future enhancement)
        const createMobileMenu = () => {
            const nav = document.querySelector('.nav-menu');
            const header = document.querySelector('.header');
            
            if (window.innerWidth <= 768) {
                // Mobile menu logic can be added here
                console.log('Mobile view detected');
            }
        };

        window.addEventListener('resize', createMobileMenu);
        createMobileMenu();

        // Scroll to top functionality
        let scrollToTopBtn = document.createElement('button');
        scrollToTopBtn.innerHTML = '<i class="fas fa-chevron-up"></i>';
        scrollToTopBtn.setAttribute('id', 'scrollToTop');
        scrollToTopBtn.style.cssText = `
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: linear-gradient(45deg, #4caf50, #2e7d32);
            color: white;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.4);
            z-index: 1000;
        `;

        document.body.appendChild(scrollToTopBtn);

        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                scrollToTopBtn.style.opacity = '1';
                scrollToTopBtn.style.visibility = 'visible';
            } else {
                scrollToTopBtn.style.opacity = '0';
                scrollToTopBtn.style.visibility = 'hidden';
            }
        });

        scrollToTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        // Add hover effect to scroll to top button
        scrollToTopBtn.addEventListener('mouseenter', () => {
            scrollToTopBtn.style.transform = 'translateY(-3px)';
            scrollToTopBtn.style.boxShadow = '0 6px 20px rgba(76, 175, 80, 0.6)';
        });

        scrollToTopBtn.addEventListener('mouseleave', () => {
            scrollToTopBtn.style.transform = 'translateY(0)';
            scrollToTopBtn.style.boxShadow = '0 4px 15px rgba(76, 175, 80, 0.4)';
        });

        // Progressive loading effect
        document.addEventListener('DOMContentLoaded', function() {
            // Add loading class to body
            document.body.style.opacity = '0';
            document.body.style.transition = 'opacity 0.5s ease-in';
            
            // Fade in page
            setTimeout(() => {
                document.body.style.opacity = '1';
            }, 100);
            
            // Trigger initial animations
            setTimeout(() => {
                animateOnScroll();
            }, 500);
        });

        // Enhanced form validation
        const form = document.getElementById('contactForm');
        const inputs = form.querySelectorAll('input, textarea');
        
        inputs.forEach(input => {
            input.addEventListener('blur', validateField);
            input.addEventListener('input', clearError);
        });

        function validateField(e) {
            const field = e.target;
            const value = field.value.trim();
            
            // Remove existing error styling
            field.style.borderColor = '';
            
            if (field.hasAttribute('required') && !value) {
                showFieldError(field, 'Este campo es requerido');
                return false;
            }
            
            if (field.type === 'email' && value && !isValidEmail(value)) {
                showFieldError(field, 'Ingresa un email válido');
                return false;
            }
            
            return true;
        }

        function showFieldError(field, message) {
            field.style.borderColor = '#f44336';
            field.style.boxShadow = '0 0 5px rgba(244, 67, 54, 0.3)';
            
            // Remove existing error message
            const existingError = field.parentNode.querySelector('.error-message');
            if (existingError) {
                existingError.remove();
            }
            
            // Add error message
            const errorDiv = document.createElement('div');
            errorDiv.className = 'error-message';
            errorDiv.style.cssText = 'color: #f44336; font-size: 0.8rem; margin-top: 0.25rem;';
            errorDiv.textContent = message;
            field.parentNode.appendChild(errorDiv);
        }

        function clearError(e) {
            const field = e.target;
            field.style.borderColor = '';
            field.style.boxShadow = '';
            
            const errorMessage = field.parentNode.querySelector('.error-message');
            if (errorMessage) {
                errorMessage.remove();
            }
        }

        function isValidEmail(email) {
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailRegex.test(email);
        }

        // Enhanced form submission
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            
            let isValid = true;
            inputs.forEach(input => {
                if (!validateField({target: input})) {
                    isValid = false;
                }
            });
            
            if (isValid) {
                // Show loading state
                const submitBtn = form.querySelector('.submit-btn');
                const originalText = submitBtn.innerHTML;
                submitBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Enviando...';
                submitBtn.disabled = true;
                
                // Simulate form submission
                setTimeout(() => {
                    // Show success message
                    showSuccessMessage();
                    
                    // Reset form
                    form.reset();
                    
                    // Reset button
                    submitBtn.innerHTML = originalText;
                    submitBtn.disabled = false;
                }, 2000);
            }
        });

        function showSuccessMessage() {
            // Create success modal
            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background: rgba(0, 0, 0, 0.5);
                display: flex;
                align-items: center;
                justify-content: center;
                z-index: 2000;
                opacity: 0;
                transition: opacity 0.3s ease;
            `;
            
            const modalContent = document.createElement('div');
            modalContent.style.cssText = `
                background: white;
                padding: 3rem;
                border-radius: 15px;
                text-align: center;
                max-width: 400px;
                margin: 2rem;
                box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
                transform: translateY(20px);
                transition: transform 0.3s ease;
            `;
            
            modalContent.innerHTML = `
                <div style="color: #4caf50; font-size: 3rem; margin-bottom: 1rem;">
                    <i class="fas fa-check-circle"></i>
                </div>
                <h3 style="color: #1976d2; margin-bottom: 1rem;">¡Mensaje Enviado!</h3>
                <p style="color: #666; margin-bottom: 2rem;">
                    Gracias por tu interés en nuestro proyecto. Te contactaremos pronto para que puedas 
                    ser parte de nuestro compromiso con el futuro.
                </p>
                <button onclick="this.closest('[style*=fixed]').remove()" 
                        style="background: linear-gradient(45deg, #4caf50, #2e7d32); color: white; 
                               border: none; padding: 10px 30px; border-radius: 25px; cursor: pointer;">
                    Continuar
                </button>
            `;
            
            modal.appendChild(modalContent);
            document.body.appendChild(modal);
            
            // Animate in
            setTimeout(() => {
                modal.style.opacity = '1';
                modalContent.style.transform = 'translateY(0)';
            }, 50);
            
            // Auto close after 5 seconds
            setTimeout(() => {
                if (document.body.contains(modal)) {
                    modal.remove();
                }
            }, 5000);
        }
    </script>
</body>
</html>
