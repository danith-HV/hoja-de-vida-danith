<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hoja de Vida Interactiva | Danith Sabogal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 19px;
            top: 0;
            bottom: 0;
            width: 2px;
            background-color: #e2e8f0;
        }
        .timeline-dot {
            position: absolute;
            left: 10px;
            top: 4px;
            height: 20px;
            width: 20px;
            background-color: white;
            border: 2px solid #2c5282;
            border-radius: 50%;
            z-index: 10;
        }
        .skill-tab.active {
            border-color: #2c5282;
            background-color: #2c5282;
            color: white;
        }
        .section-fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .section-fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body class="bg-[#fdfaf6] text-[#333333]">
<!-- Chosen Palette: Warm Neutral Professional -->
<!-- Application Structure Plan: A single-page, scrolling interactive resume. The structure is designed for a recruiter's user flow: 1. Hero section with a strong title and summary. 2. A "dashboard" of key quantifiable metrics to grab immediate attention. 3. An interactive skills section with tabs to allow easy exploration without clutter. 4. A clean, vertical timeline for experience, with expandable details to keep the initial view scannable. 5. Standard sections for Education and Languages. This non-linear, interactive approach allows users to dive into the sections most relevant to them first, making it more efficient than a static PDF. -->
<!-- Visualization & Content Choices: Report Info: Core skills -> Goal: Organize/Inform -> Viz/Method: Interactive tabs -> Interaction: Click to filter skills -> Justification: Avoids a long, overwhelming list and demonstrates interactivity. Report Info: Work History -> Goal: Organize/Show Progression -> Viz/Method: Vertical Timeline with expandable cards -> Interaction: Click "details" to reveal responsibilities -> Justification: Keeps the UI clean and scannable, focusing on titles first. Report Info: Key Achievements (430+ tickets, time reduction) -> Goal: Impress/Inform -> Viz/Method: Stat cards (HTML/Tailwind) -> Interaction: Hover effects -> Justification: Highlights most impactful results upfront for immediate visibility. -->
<!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <div class="container mx-auto max-w-5xl p-4 sm:p-6 md:p-8">

        <header id="header" class="flex flex-col sm:flex-row justify-between items-center mb-10 section-fade-in">
            <div>
                <h1 class="text-4xl md:text-5xl font-bold text-[#2c5282]">Danith Sabogal</h1>
                <p class="text-xl md:text-2xl text-gray-600 mt-1">Especialista en Integridad de Datos y Analista SQL</p>
            </div>
            <div class="flex space-x-4 mt-4 sm:mt-0 text-sm">
                <a href="mailto:dazadanith@gmail.com" class="text-gray-600 hover:text-[#2c5282] transition duration-300">dazadanith@gmail.com</a>
                <a href="https://www.linkedin.com/in/danith-sabogal-a00462296" target="_blank" class="text-gray-600 hover:text-[#2c5282] transition duration-300">LinkedIn</a>
            </div>
        </header>

        <main>
            <section id="summary" class="mb-12 section-fade-in">
                <h2 class="text-2xl font-bold border-b-2 border-[#e2e8f0] pb-2 mb-4 text-[#2c5282]">Perfil Profesional</h2>
                <p class="text-gray-700 leading-relaxed">
                    Estudiante avanzada de Derecho y Técnica en Sistemas con un perfil que fusiona el rigor analítico con la eficiencia tecnológica. Mi experiencia se centra en la gestión, clasificación y análisis de grandes volúmenes de datos, incluyendo la ejecución de consultas SQL complejas. Especializada en optimizar flujos de trabajo con herramientas de IA (Certificación en ChatGPT Advanced Data Analysis), garantizando una atención meticulosa al detalle y una precisión del 100% en la entrada y reporte de información sensible. Busco activamente una oportunidad remota para aplicar mis habilidades en la integridad de datos y eficiencia de procesos.
                </p>
            </section>

            <section id="highlights" class="mb-12 section-fade-in">
                 <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 text-center">
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200">
                        <h3 class="text-3xl font-bold text-[#2c5282]">430+</h3>
                        <p class="text-gray-600">Tickets de Soporte Analizados</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200">
                        <h3 class="text-3xl font-bold text-[#2c5282]">100%</h3>
                        <p class="text-gray-600">Precisión en Data Entry</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200">
                        <h3 class="text-3xl font-bold text-[#2c5282]">95%</h3>
                        <p class="text-gray-600">Reducción Tiempo de Reportes</p>
                    </div>
                </div>
            </section>

            <section id="skills" class="mb-12 section-fade-in">
                <h2 class="text-2xl font-bold border-b-2 border-[#e2e8f0] pb-2 mb-4 text-[#2c5282]">Competencias Interactivas</h2>
                <div class="flex flex-wrap gap-2 mb-6">
                    <button class="skill-tab active px-4 py-2 border-2 border-gray-300 rounded-full text-sm font-medium transition duration-300" data-target="tech">Técnicas y Datos</button>
                    <button class="skill-tab px-4 py-2 border-2 border-gray-300 rounded-full text-sm font-medium transition duration-300" data-target="analytical">Analíticas y Administrativas</button>
                    <button class="skill-tab px-4 py-2 border-2 border-gray-300 rounded-full text-sm font-medium transition duration-300" data-target="tools">Herramientas y Software</button>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div id="tech" class="skill-content grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-center">SQL</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-center">SQLite</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-center">Data Entry</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-center">Bases de Datos</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-center">Consultas Complejas</span>
                        <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-center">Clasificación Datos</span>
                    </div>
                    <div id="analytical" class="skill-content hidden grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
                        <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-center">Integridad de Datos</span>
                        <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-center">Atención al Detalle</span>
                        <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-center">Cumplimiento Normativo</span>
                        <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-center">Optimización de Flujos</span>
                        <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-center">Resolución de Problemas</span>
                        <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-center">Redacción Técnica</span>
                    </div>
                    <div id="tools" class="skill-content hidden grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
                        <span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-center">ChatGPT (Análisis)</span>
                        <span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-center">Microsoft Office</span>
                        <span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-center">Google Workspace</span>
                        <span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-center">Excel (Avanzado)</span>
                        <span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-center">IA de Texto</span>
                    </div>
                </div>
            </section>

            <section id="experience" class="mb-12 section-fade-in">
                <h2 class="text-2xl font-bold border-b-2 border-[#e2e8f0] pb-2 mb-8 text-[#2c5282]">Experiencia Profesional</h2>
                <div class="relative">
                    <div class="timeline-item relative pl-10 pb-8">
                        <div class="timeline-dot"></div>
                        <p class="text-sm text-gray-500">Julio 2025 – Presente</p>
                        <h3 class="font-bold text-lg">Analista de Datos SQL (Proyecto Freelance)</h3>
                        <p class="text-gray-700 font-medium">Freelancer.com | Remoto</p>
                        <div class="text-gray-600 mt-2 text-sm leading-relaxed">
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Desarrollé y ejecuté scripts SQL reusables para analizar más de 430 tickets de soporte, reduciendo drásticamente el tiempo de generación de reportes.</li>
                                <li>Apliqué funciones agregadas (COUNT, GROUP BY) y operadores condicionales para segmentar datos y extraer métricas de negocio cruciales.</li>
                            </ul>
                        </div>
                    </div>
                    <div class="timeline-item relative pl-10 pb-8">
                        <div class="timeline-dot"></div>
                        <p class="text-sm text-gray-500">Abril 2025 – Junio 2025</p>
                        <h3 class="font-bold text-lg">Especialista en Data Entry y Anotación de Datos de IA</h3>
                        <p class="text-gray-700 font-medium">Fiverr | Cliente Internacional (Remoto)</p>
                        <div class="text-gray-600 mt-2 text-sm leading-relaxed">
                             <ul class="list-disc pl-5 space-y-1">
                                <li>Clasifiqué grandes volúmenes de datos textuales en español para el entrenamiento de modelos de IA, siguiendo protocolos estrictos de calidad y confidencialidad.</li>
                                <li>Realicé la entrada y actualización de información en bases de datos internas, asegurando la integridad y consistencia de los datos.</li>
                            </ul>
                        </div>
                    </div>
                    <div class="timeline-item relative pl-10">
                        <div class="timeline-dot"></div>
                        <p class="text-sm text-gray-500">Enero 2021 – Junio 2021</p>
                        <h3 class="font-bold text-lg">Auxiliar Administrativo y Asistente Virtual</h3>
                        <p class="text-gray-700 font-medium">Oficina Jurídica RR | Villavicencio, Colombia</p>
                         <div class="text-gray-600 mt-2 text-sm leading-relaxed">
                            <ul class="list-disc pl-5 space-y-1">
                                <li>Organicé el archivo físico y digital, implementando un sistema para la rápida localización de documentos y seguimiento de vencimientos.</li>
                                <li>Coordiné agendas, gestioné comunicaciones y redacté documentos legales y administrativos, garantizando el cumplimiento de plazos.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </section>
            
            <section id="education" class="mb-12 section-fade-in">
                <h2 class="text-2xl font-bold border-b-2 border-[#e2e8f0] pb-2 mb-4 text-[#2c5282]">Educación y Certificaciones</h2>
                <div class="grid md:grid-cols-2 gap-8">
                    <div>
                        <h3 class="font-bold text-lg">Formación Académica</h3>
                        <div class="mt-2 space-y-3">
                            <p><strong class="font-medium text-gray-800">Derecho:</strong> Universidad Antonio Nariño (2019-2023)</p>
                            <p><strong class="font-medium text-gray-800">Técnico en Sistemas:</strong> Servicio Nacional de Aprendizaje (SENA)</p>
                             <p><strong class="font-medium text-gray-800">Desarrollo de Software:</strong> Universidad de los Andes</p>
                        </div>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Certificaciones Destacadas</h3>
                        <div class="mt-2 space-y-2 text-gray-700">
                           <p>✓ ChatGPT Advanced Data Analysis</p>
                           <p>✓ Corrección, Estilo y Variaciones de la Lengua Española</p>
                           <p>✓ Getting started with Google Workspace</p>
                           <p>✓ Administración Efectiva del Tiempo</p>
                        </div>
                    </div>
                </div>
            </section>

            <section id="languages" class="section-fade-in">
                <h2 class="text-2xl font-bold border-b-2 border-[#e2e8f0] pb-2 mb-4 text-[#2c5282]">Idiomas</h2>
                 <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <p><strong class="font-medium">Español:</strong> Nativo</p>
                    <p class="mt-2"><strong class="font-medium">Inglés:</strong> Competencia Profesional en Lectura y Escritura.</p>
                    <p class="text-sm text-gray-500 mt-1">Capacidad para procesar, revisar y redactar documentación técnica y textual en inglés. (Limitación en fluidez conversacional oral y auditiva).</p>
                </div>
            </section>

        </main>

        <footer class="text-center mt-12 pt-6 border-t border-gray-200 text-sm text-gray-500">
            <p>&copy; 2025 Danith Sabogal. Hoja de Vida Interactiva.</p>
        </footer>

    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const skillTabs = document.querySelectorAll('.skill-tab');
            const skillContents = document.querySelectorAll('.skill-content');

            skillTabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    skillTabs.forEach(t => t.classList.remove('active'));
                    tab.classList.add('active');

                    const target = tab.getAttribute('data-target');
                    
                    skillContents.forEach(content => {
                        if (content.id === target) {
                            content.classList.remove('hidden');
                        } else {
                            content.classList.add('hidden');
                        }
                    });
                });
            });

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.section-fade-in').forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
