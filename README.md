# PROGRAMA-AMBIENTAL
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Propuesta Ambiental Cemex Verde- </title>
  <!-- Font Awesome para iconos -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    /* Estilos base */
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      transition: background-color 0.3s, color 0.3s;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    /* Colores Corporativos Cemex */
    :root {
        --cemex-blue: #003087;
        --cemex-red: #EF3340;
        --cemex-green: #28a745; /* Para botones de acción positivos */
    }

    /* Modo claro */
    body.light {
      background-color: #f4f4f4;
      color: #333;
    }

    /* Modo oscuro */
    body.dark {
      background-color: #1a1a1a;
      color: #fff;
    }

    /* Header */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 20px;
      background-color: rgba(255, 255, 255, 0.95);
      transition: background-color 0.3s;
      box-shadow: 0 1px 5px rgba(0,0,0,0.1);
      z-index: 100;
      flex-wrap: wrap;
    }
    
    body.dark header {
        background-color: rgba(30, 30, 30, 0.95);
        box-shadow: 0 1px 5px rgba(255,255,255,0.1);
    }

    .logo {
      height: 50px;
    }
    
    .logo-container {
        display: flex;
        align-items: center;
    }

    .names {
      text-align: right;
    }
    
    .names ul {
        list-style: none;
        padding: 0;
        margin: 5px 0 0 0;
        font-size: 0.9em;
    }

    .mode-toggle {
      cursor: pointer;
      padding: 8px 15px;
      background: var(--cemex-blue);
      color: white;
      border: none;
      border-radius: 20px;
      transition: background-color 0.3s, transform 0.2s;
      font-weight: bold;
    }

    .mode-toggle:hover {
        transform: scale(1.05);
    }

    body.dark .mode-toggle {
      background: var(--cemex-red);
    }

    /* Pantalla principal (ESTILO MEJORADO) */
    main {
      flex: 1;
      position: relative;
      /* Fondo de fábrica de cemento con degradado oscuro para contraste */
      background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.8)), 
                        url("https://www.comunicarseweb.com/sites/default/files/styles/galeria_noticias/public/pages/imagen-planta-dedicada.jpg?itok=yRqFv84E");
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px 20px;
    }

    .welcome {
      text-align: center;
      /* Fondo más opaco para destacar el texto */
      background: rgba(255, 255, 255, 0.98); 
      padding: 30px;
      border-radius: 15px;
      margin-bottom: 20px;
      max-width: 800px;
      /* Sombra mejorada */
      box-shadow: 0 10px 35px rgba(0,0,0,0.5);
      animation: fadeIn 0.8s;
    }

    body.dark .welcome {
      background: rgba(30, 30, 30, 0.98);
      color: #fff;
    }
    
    .welcome h1 {
        color: var(--cemex-blue);
        font-size: 2.5em;
    }
    body.dark .welcome h1 {
        color: var(--cemex-red);
    }

    .program-selector, .expert-btn {
      margin: 10px 0;
      padding: 12px 20px;
      font-size: 18px;
      border-radius: 30px;
      border: 1px solid #ccc;
      width: 100%;
      max-width: 400px;
      cursor: pointer;
      transition: all 0.2s;
    }
    
    .expert-btn {
        background: var(--cemex-green);
        color: white;
        border: none;
        font-weight: bold;
        box-shadow: 0 2px 10px rgba(40, 167, 69, 0.5);
    }
    
    .expert-btn:hover {
        background: #218838;
    }

    body.dark .program-selector {
      background: #333;
      color: #fff;
      border-color: #555;
    }

    .program-content {
      display: none;
      width: 100%;
      max-width: 900px;
      background: rgba(255, 255, 255, 0.98);
      padding: 30px;
      border-radius: 15px;
      margin-top: 30px;
      text-align: left;
      animation: fadeIn 0.5s;
      box-shadow: 0 8px 30px rgba(0,0,0,0.4);
    }

    body.dark .program-content {
      background: rgba(30, 30, 30, 0.98);
    }

    .program-content img {
      max-width: 100%;
      height: auto;
      border-radius: 10px;
      margin: 15px 0;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      object-fit: cover;
    }

    .back-btn {
      background: var(--cemex-red);
      color: white;
      border: none;
      padding: 8px 15px;
      border-radius: 20px;
      cursor: pointer;
      margin-bottom: 15px;
      font-weight: bold;
    }

    .cards-game {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 15px;
      margin: 20px 0;
    }

    .card {
      height: 120px;
      background: var(--cemex-blue);
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 8px;
      padding: 10px;
      text-align: center;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.3s, background 0.3s;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
      user-select: none;
    }

    .card:hover {
      transform: scale(1.03);
    }

    .card.flipped {
      background: var(--cemex-green);
      font-size: 0.9em;
    }
    
    /* Quiz Styles */
    .quiz-question {
        background: #f8f9fa;
        padding: 15px;
        border-radius: 8px;
        margin-bottom: 15px;
        border: 1px solid #eee;
    }
    
    body.dark .quiz-question {
        background: #2b2b2b;
        border-color: #444;
    }

    .option {
      display: block;
      padding: 10px;
      margin: 5px 0;
      cursor: pointer;
      border: 1px solid #ccc;
      border-radius: 4px;
      background: white;
      transition: background 0.2s;
    }
    
    body.dark .option {
        background: #444;
        border-color: #555;
        color: #fff;
    }

    .option:hover {
      background: #e9ecef;
    }
    
    body.dark .option:hover {
        background: #555;
    }

    /* Chatbot Styles */
    .chatbot-container {
        position: fixed;
        bottom: 20px;
        right: 20px;
        z-index: 1000;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
    }

    .chatbot {
        width: 300px;
        height: 400px;
        background: white;
        border-radius: 10px;
        display: none;
        flex-direction: column;
        box-shadow: 0 0 15px rgba(0,0,0,0.2);
        margin-bottom: 10px;
        overflow: hidden;
    }

    .chatbot.active {
        display: flex;
    }

    body.dark .chatbot { background: #333; border-color: #555; }
    
    .chat-header { 
        background: var(--cemex-red); 
        color: white; 
        padding: 10px 15px; 
        border-radius: 10px 10px 0 0; 
        display: flex; 
        justify-content: space-between; 
        align-items: center;
    }
    .chat-header h3 { margin: 0; font-size: 1em; }
    
    .chat-close-btn {
        background: none;
        border: none;
        color: white;
        cursor: pointer;
        font-size: 1.2em;
        transition: transform 0.2s;
        padding: 0;
    }
    
    .chat-close-btn:hover {
        transform: scale(1.2);
    }
    
    .chat-messages { flex: 1; padding: 10px; overflow-y: auto; background: #f9f9f9; display: flex; flex-direction: column; gap: 10px; }
    body.dark .chat-messages { background: #222; }
    
    .message { padding: 8px; border-radius: 5px; max-width: 85%; }
    .bot-message { background: #d4edda; color: #333; margin-right: auto; }
    body.dark .bot-message { background: #444; color: #fff; }

    .chat-controls {
        padding: 10px;
        border-top: 1px solid #ccc;
        background: white;
    }
    body.dark .chat-controls {
        background: #333;
    }

    .chat-select {
        width: 100%;
        padding: 8px;
        border-radius: 5px;
        border: 1px solid #ccc;
        font-size: 1em;
    }

    /* Robot Flotante */
    .robot-toggle-btn {
        width: 60px;
        height: 60px;
        background: white;
        border: 4px solid var(--cemex-blue);
        border-radius: 50%;
        box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        cursor: pointer;
        transition: transform 0.3s;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
    }

    .robot-toggle-btn:hover {
        transform: scale(1.1);
    }
    
    .robot-toggle-btn img {
        width: 100%;
        height: 100%;
        padding: 5px;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 15px;
      background: #333;
      color: white;
      margin-top: auto;
    }
    
    footer a {
        color: var(--cemex-green);
        text-decoration: none;
        margin: 0 5px;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* Responsivo */
    @media (max-width: 768px) {
        .chatbot-container { 
            width: 90%;
            right: 5%;
            bottom: 10px;
        } 
        .chatbot {
             width: 100%;
             height: 350px;
        }
        .names {
            order: 3;
            width: 100%;
            text-align: center;
            margin-top: 15px;
        }
        .names ul {
            justify-content: center;
        }
        header {
            flex-direction: column;
            align-items: center;
            gap: 10px;
            padding: 10px;
        }
    }
  </style>
</head>
<body class="light">
  <header>
    <div class="logo-container">
        <img
          src="https://www.cemex.com/documents/20182/0/Cemex+logo.png"
          alt="Logo Cemex"
          class="logo"
        />
        <!-- Logo de apoyo en CSS por si el enlace falla -->
        <div style="font-weight: 900; font-size: 30px; letter-spacing: -2px; display: flex;">
            <span style="color: var(--cemex-blue);">CE</span><span style="color: var(--cemex-blue);">MEX</span>
            <div style="width: 6px; height: 25px; background: var(--cemex-red); margin-left: 5px; transform: skewX(-20deg);"></div>
            <div style="width: 6px; height: 25px; background: var(--cemex-blue); margin-left: 2px; transform: skewX(-20deg);"></div>
        </div>
    </div>
    <div class="names">
      <p style="font-weight: bold;">Equipo Propuesta:</p>
      <ul>
        <li>Leidy Álvarez</li>
        <li>Flor Macayo</li>
        <li>Jan Turizo</li>
        <li>Mateo Acosta</li>
      </ul>
    </div>
    <button class="mode-toggle" onclick="toggleMode()"><i class="fas fa-moon"></i> Modo Oscuro</button>
  </header>

  <main>
    <div class="welcome">
      <h1>Bienvenido a la Propuesta Ambiental de Cemex Verde</h1>
      <p>
        Explora nuestros programas ambientales con actividades lúdicas. ¡Interactúa y aprende!
      </p>
      
      <select id="programSelect" class="program-selector" onchange="loadProgram()">
        <option value="">Selecciona un programa</option>
        <option value="emisiones">Control de Emisiones Atmosféricas</option>
        <option value="agua">Gestión Integral de Agua</option>
        <option value="sst">Seguridad y Salud en el Trabajo (SST)</option>
        <option value="residuos">Manejo de Residuos (Coprocesamiento)</option>
        <option value="ruido">Control de Emisiones de Ruido</option>
        <option value="responsabilidad">Responsabilidad Social</option>
        <option value="biodiversidad">Conservación de Biodiversidad</option>
        <option value="energia">Eficiencia Energética</option>
      </select>
      
      <button class="expert-btn" onclick="openExpertVideo()">Palabras de un colega</button>
      
    </div>

    <div id="programContent" class="program-content"></div>
  </main>
  
  <div class="chatbot-container">
      <div class="chatbot" id="chatbot">
          <div class="chat-header">
              <div style="display:flex; align-items:center; gap:8px;">
                  <i class="fas fa-robot"></i>
                  <h3>Nucita IA</h3>
              </div>
              <button class="chat-close-btn" onclick="toggleChat()">
                  <i class="fas fa-times"></i>
              </button>
          </div>
          <div class="chat-messages" id="chatMessages">
              <div class="message bot-message">
                  ¡Hola! Soy <strong>Nucita</strong>. 👋<br>
                  Selecciona un tema para conocer el <strong>objetivo completo</strong> del programa ambiental de Cemex.
              </div>
          </div>
          <div class="chat-controls">
              <select id="chatSelect" class="chat-select" onchange="sendMessageFromSelect()">
                <option value="">-- Elige un Programa --</option>
                <option value="emisiones">Control de Emisiones</option>
                <option value="agua">Gestión de Agua</option>
                <option value="sst">Seguridad y Salud</option>
                <option value="residuos">Manejo de Residuos</option>
                <option value="ruido">Control de Ruido</option>
                <option value="responsabilidad">Responsabilidad Social</option>
                <option value="biodiversidad">Biodiversidad</option>
                <option value="energia">Eficiencia Energética</option>
              </select>
          </div>
      </div>
      <!-- Botón Flotante para Abrir/Cerrar Chat -->
      <button class="robot-toggle-btn" onclick="toggleChat()">
          <img src="https://api.dicebear.com/7.x/bottts/svg?seed=Nucita&backgroundColor=003087" alt="Nucita Icon">
      </button>
  </div>

  <footer>
    <p>© 2025 Propuesta Ambiental. Todos los derechos reservados.</p>
  </footer>

  <script>
    // --- Data Structure for Programs, Cards, and Quiz ---
    const programsData = {
        emisiones: {
            title: "Control de Emisiones Atmosféricas",
            objective: "El objetivo principal es la descarbonización. Se busca reducir significativamente las emisiones de CO₂ y otros contaminantes mediante la sustitución de combustibles fósiles por alternos (biomasa, residuos) y la implementación de tecnologías de captura avanzada. Esto es fundamental para alcanzar la meta de Cero Emisiones Netas para 2050. La innovación se centra en el monitoreo continuo y el uso de filtros de alta eficiencia (como los filtros de mangas).",
            imageUrl: "https://www.cimelsa.com/wp-content/uploads/2021/11/Control-de-emisiones-industriales.jpg",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Uso de hidrógeno verde en el proceso de clinkerización para sustituir fuentes de carbono y descarbonizar el cemento." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Filtros de mangas de alta eficiencia que capturan el 99.9% del material particulado, garantizando la calidad del aire." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Meta de Cemex de reducción del 47% de CO₂ por tonelada de cemento al 2030, parte de la estrategia Futuro en Acción." }
            ],
            quiz: [
                { id: 1, question: "¿Cuál es el principal sustituto de combustible fósil en el proceso?", options: ["Petróleo crudo", "Biomasa y residuos", "Gas natural"], answer: 1 },
                { id: 2, question: "¿Cuál es la meta de reducción de CO₂ para el 2030?", options: ["25%", "47%", "80%"], answer: 1 },
                { id: 3, question: "¿Qué tecnología ayuda a capturar la mayoría del polvo?", options: ["Microondas", "Filtros de mangas", "Refrigeración"], answer: 1 }
            ]
        },
        agua: {
            title: "Gestión Integral de Agua",
            objective: "Se centra en la optimización del consumo de agua en todas las operaciones, priorizando el reciclaje y tratamiento para minimizar la extracción de fuentes naturales. El enfoque está en las zonas de estrés hídrico para asegurar que las operaciones no afecten la disponibilidad de agua para las comunidades vecinas, logrando la 'Cero descarga' de aguas residuales industriales.",
            imageUrl: "https://www.andinalinksmartcities.com/wp-content/uploads/2023/06/ArticuloAguaSmartCities-Foto-JESSICA-1024x576.png",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Implementación de circuitos cerrados de agua que permiten reciclar más del 90% del agua de proceso." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Sensores inteligentes de nivel hídrico y calidad que monitorean en tiempo real el recurso." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Contribuir al Objetivo de Desarrollo Sostenible (ODS) 6: Agua Limpia y Saneamiento, priorizando comunidades." }
            ],
            quiz: [
                { id: 4, question: "¿En qué porcentaje se busca reciclar el agua de proceso?", options: ["Menos del 50%", "Más del 90%", "Solo el 10%"], answer: 1 },
                { id: 5, question: "¿Cuál es el principal enfoque en la gestión del agua?", options: ["Extracción masiva", "Zonas de estrés hídrico", "Desperdicio"], answer: 1 },
                { id: 6, question: "¿Qué significa 'Cero descarga' en el programa?", options: ["No usar agua", "No emitir residuos al ambiente", "No producir"], answer: 1 }
            ]
        },
        sst: {
            title: "Seguridad y Salud en el Trabajo (SST)",
            objective: "El objetivo es Cero Accidentes. Se implementan rigurosos protocolos de seguridad, capacitaciones interactivas, y el uso obligatorio de Equipo de Protección Personal (EPP) de última generación. Se promueve una cultura de seguridad basada en el comportamiento, donde cada empleado es responsable de su seguridad y la de sus compañeros.",
            imageUrl: "https://twind.io/co/wp-content/uploads/2024/01/SST-1024x682.jpg",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Uso de drones para inspección de alturas, reduciendo la exposición del personal a riesgos críticos." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Implementación de realidad virtual (VR) para simulacros de evacuación y manejo de maquinaria pesada." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Reducción continua de la Tasa de Frecuencia de Accidentes con Tiempo Perdido (LTIFR) a niveles de clase mundial." }
            ],
            quiz: [
                { id: 7, question: "¿Cuál es el objetivo primordial del programa de SST?", options: ["Ahorrar costos", "Cero Accidentes", "Rapidez en la obra"], answer: 1 },
                { id: 8, question: "¿Qué tecnología se usa para reducir la exposición en alturas?", options: ["Escaleras manuales", "Drones de inspección", "Andamios antiguos"], answer: 1 },
                { id: 9, question: "¿Qué promueve la 'cultura de seguridad basada en el comportamiento'?", options: ["Solo supervisores responsables", "Responsabilidad individual y colectiva", "Ignorar riesgos menores"], answer: 1 }
            ]
        },
        residuos: {
            title: "Manejo de Residuos (Coprocesamiento)",
            objective: "El programa se enfoca en el coprocesamiento, que consiste en transformar residuos (peligrosos y no peligrosos) en energía y/o materiales, utilizando los hornos de cemento. Este método elimina los residuos de manera segura, sin dejar cenizas, y reduce la necesidad de usar rellenos sanitarios y combustibles fósiles, cerrando el ciclo de la economía circular.",
            imageUrl: "https://media.licdn.com/dms/image/v2/C4E12AQHr5RYNyzOaVg/article-cover_image-shrink_720_1280/article-cover_image-shrink_720_1280/0/1573395947928?e=2147483647&v=beta&t=k290SrzZP8PGcci7cescmVRBZdcm2V_PMBq73bb3acQ",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Desarrollo de la línea Pro Ambiente para la recolección y tratamiento de llantas, biomasa y aceites usados." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Hornos de cemento operando a 1500°C, que garantizan la destrucción térmica total de los contaminantes." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Conversión de toneladas de residuos municipales e industriales en una fuente de energía sostenible." }
            ],
            quiz: [
                { id: 10, question: "¿Qué proceso convierte residuos en energía en la planta?", options: ["Enterramiento", "Coprocesamiento", "Reciclaje de papel"], answer: 1 },
                { id: 11, question: "¿A qué temperatura aproximada operan los hornos en este proceso?", options: ["100°C", "500°C", "1500°C"], answer: 2 },
                { id: 12, question: "¿Cuál es el beneficio ambiental del coprocesamiento?", options: ["Aumentar rellenos sanitarios", "Eliminación total y ahorro de fósiles", "Solo ahorro de dinero"], answer: 1 }
            ]
        },
        ruido: {
            title: "Control de Emisiones de Ruido",
            objective: "Busca minimizar el impacto acústico de la planta hacia las comunidades aledañas y proteger la salud auditiva de los empleados. Se logra mediante la implementación de barreras sónicas, aislamientos en equipos, y un riguroso programa de mantenimiento preventivo para silenciar fuentes de ruido.",
            imageUrl: "https://www.satirnet.com/satirnet/wp-content/uploads/2015/05/control-de-ruidol.jpg",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Modelado acústico predictivo para identificar y mitigar las principales fuentes de ruido antes de su impacto." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Instalación de silenciadores de alta eficiencia en ventiladores y compresores." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Mejora de la calidad de vida de las comunidades y cumplimiento de normativas locales de límites de ruido." }
            ],
            quiz: [
                { id: 13, question: "¿Cuál es el principal método de mitigación del ruido hacia la comunidad?", options: ["Apagar la planta", "Barreras sónicas y aislamiento", "Avisos de disculpa"], answer: 1 },
                { id: 14, question: "¿Qué beneficio tiene el mantenimiento preventivo en el control de ruido?", options: ["Aumenta el ruido", "Silencia la maquinaria", "Ahorra combustible"], answer: 1 },
                { id: 15, question: "¿Quién es un grupo protegido por este programa?", options: ["Los pájaros", "Empleados y vecinos", "Solo directivos"], answer: 1 }
            ]
        },
        responsabilidad: {
            title: "Programas de Responsabilidad Social",
            objective: "Se enfoca en crear valor compartido, impulsando el desarrollo sostenible en las comunidades. Incluye programas de educación, proyectos de infraestructura con cemento social y apoyo a la autoconstrucción. El objetivo es ser un buen vecino y promotor del desarrollo social y económico local.",
            imageUrl: "https://programas.uniandes.edu.co/sites/programas/files/2023-11/Responsabilidad_social_empresarial.webp",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Implementación de la plataforma 'Ecomunidad' para gestionar proyectos de impacto social con transparencia." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Uso de la app 'Construye' para asesorar a comunidades en proyectos de mejora de vivienda sostenible." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Contribuir al ODS 11: Ciudades y Comunidades Sostenibles, mejorando la calidad de vida y vivienda." }
            ],
            quiz: [
                { id: 16, question: "¿Cuál es el concepto clave de la RSC de Cemex?", options: ["Ganancia máxima", "Valor compartido", "Donaciones esporádicas"], answer: 1 },
                { id: 17, question: "¿Qué tipo de proyectos apoya este programa?", options: ["Militarización", "Educación y autoconstrucción", "Solo fiestas locales"], answer: 1 },
                { id: 18, question: "¿Cuál es un objetivo de la RSC en Cemex?", options: ["Ser el más grande", "Ser un buen vecino", "Comprar toda la tierra"], answer: 1 }
            ]
        },
        biodiversidad: {
            title: "Conservación de Biodiversidad",
            objective: "El objetivo es lograr un *impacto neto positivo en la biodiversidad. Esto implica no solo la rehabilitación de las canteras agotadas, sino también la **protección y restauración* activa de los ecosistemas, como se evidencia en la *Reserva El Carmen*, protegiendo especies en peligro.",
            imageUrl: "https://geoinnova.org/wp-content/uploads/2021/08/conservacion-biodiversidad.jpg",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Monitoreo genético de especies en canteras rehabilitadas para asegurar la viabilidad de los ecosistemas." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Mapeo con drones para medir el éxito de las campañas de reforestación y rehabilitación de tierras." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Rehabilitación del 100% de las canteras activas al final de su vida útil y protección de especies clave." }
            ],
            quiz: [
                { id: 19, question: "¿Qué se busca rehabilitar al finalizar la operación?", options: ["Las carreteras", "El paisaje urbano", "Las canteras (ecosistemas)"], answer: 2 },
                { id: 20, question: "¿Qué incluye el programa en términos de especies?", options: ["Solo especies exóticas", "Reforestación con nativas y protección de endémicas", "Plantas de interior"], answer: 1 },
                { id: 21, question: "¿Qué es la Reserva El Carmen?", options: ["Una ciudad", "Una reserva natural gestionada por Cemex", "Una mina de carbón"], answer: 1 }
            ]
        },
        energia: {
            title: "Eficiencia Energética",
            objective: "El objetivo es reducir el *consumo específico de energía* (eléctrica y térmica) en la producción de cemento e incrementar significativamente el porcentaje de energía proveniente de *fuentes limpias y renovables* (eólica, solar) para disminuir la huella de carbono indirecta.",
            imageUrl: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRGrv3jPOdkvdB07NPDlOsUBeTjmAU-OMZB6A&s",
            cards: [
                { theme: "Innovación", icon: "fas fa-microchip", content: "Recuperación de calor de los gases de escape del horno para generar electricidad (WHRS - Waste Heat Recovery System)." },
                { theme: "Tecnología", icon: "fas fa-cogs", content: "Motores y ventiladores de alta eficiencia con control de velocidad para minimizar el consumo innecesario." },
                { theme: "Impacto", icon: "fas fa-chart-line", content: "Aumentar el porcentaje de energía limpia en la matriz energética total de la compañía, reduciendo la huella de carbono." }
            ],
            quiz: [
                { id: 22, question: "¿Qué sistema se usa para generar electricidad a partir del calor residual?", options: ["Calefacción", "Sistema WHRS", "Energía geotérmica"], answer: 1 },
                { id: 23, question: "¿Qué se optimiza para reducir el consumo eléctrico?", options: ["Ventas", "Procesos de molienda", "El almuerzo"], answer: 1 },
                { id: 24, question: "¿Qué tipo de energías promueve el programa?", options: ["Fósiles", "Renovables (eólica, solar)", "Nuclear"], answer: 1 }
            ]
        }
    };

    // --- FUNCIONES ---

    function toggleMode() {
      const body = document.body;
      body.classList.toggle("dark");
      body.classList.toggle("light");
      const btn = document.querySelector(".mode-toggle");
      btn.innerHTML = body.classList.contains("dark")
        ? '<i class="fas fa-sun"></i> Modo Claro'
        : '<i class="fas fa-moon"></i> Modo Oscuro';
    }
    
    // Función para abrir el video del experto en una nueva pestaña
    function openExpertVideo() {
        // Enlace de YouTube proporcionado por el usuario
        const videoUrl = "https://youtu.be/cMMLZfBLebE?si=FpCijfcrNSfmLxJa";
        window.open(videoUrl, '_blank');
    }
    
    // Función para alternar visibilidad del chat
    function toggleChat() {
        const chat = document.getElementById('chatbot');
        chat.classList.toggle('active');
    }

    function loadProgram() {
      const select = document.getElementById("programSelect");
      const content = document.getElementById("programContent");
      const key = select.value;
      
      if (!key) {
        content.style.display = "none";
        return;
      }

      const data = programsData[key];

      // Renderizado del contenido
      content.innerHTML = `
        <button class="back-btn" onclick="backToMenu()">← Volver al Menú</button>
        
        <h2 style="color: ${document.body.classList.contains('dark') ? '#EF3340' : '#003087'}; margin-bottom:10px;">${data.title}</h2>
        <img src="${data.imageUrl}" class="program-image" alt="${data.title}">
        
        <div class="objective-box">
            <h4 style="margin-top:0; color:var(--cemex-blue);"><i class="fas fa-bullseye"></i> Objetivo del Programa:</h4>
            <p style="font-size: 1.1em; line-height: 1.6;">${data.objective}</p>
        </div>

        <h3 style="border-bottom: 2px solid #ddd; padding-bottom: 10px; text-align: left;"><i class="fas fa-puzzle-piece"></i> Zona Interactiva: Impacto por Área</h3>
        <p style="text-align: left;">Haz clic en cada tarjeta para descubrir la innovación y el impacto del programa:</p>
        <div class="cards-game">
            ${data.cards.map((card, index) => `
                <div class="card" onclick="flipCard(this, '${card.content.replace(/'/g, "\\'")}', '${card.theme}', '${card.icon}')">
                    <div class="card-content">
                        <i class="${card.icon}" style="font-size: 3em; margin-bottom: 15px;"></i>
                        <span style="font-size: 1.2em;">${card.theme}</span>
                        <span style="font-size: 0.8em; margin-top: 5px;">Haga clic para ver el detalle</span>
                    </div>
                </div>
            `).join('')}
        </div>

        <div class="quiz-container">
            <h3 style="color: var(--cemex-blue);"><i class="fas fa-clipboard-check"></i> Desafío Rápido: ¿Cuánto sabes?</h3>
            <div id="quiz-area">
                ${renderQuiz(data.quiz)}
            </div>
        </div>
      `;
      content.style.display = 'block';
      content.scrollIntoView({ behavior: 'smooth' });
    }

    function backToMenu() {
      document.getElementById("programContent").style.display = "none";
      document.getElementById("programSelect").value = "";
      document.querySelector('.welcome').scrollIntoView({ behavior: 'smooth' });
    }

    function renderQuiz(questions) {
        return questions.map((q, qIndex) => `
            <div class="quiz-question question-block" data-question-id="q-${q.id}">
                <p class="question-text" style="font-weight: bold;">${qIndex + 1}. ${q.question}</p>
                ${q.options.map((opt, oIndex) => `
                    <div class="option" onclick="checkAnswer(this, ${oIndex === q.answer}, 'q-${q.id}')">${opt}</div>
                `).join('')}
            </div>
        `).join('');
    }


    function flipCard(card, text, theme, icon) {
      if (card.classList.contains("flipped")) {
        card.classList.remove("flipped");
        card.innerHTML = `<div class="card-content">
            <i class="${icon}" style="font-size: 3em; margin-bottom: 15px;"></i>
            <span style="font-size: 1.2em;">${theme}</span>
            <span style="font-size: 0.8em; margin-top: 5px;">Haga clic para ver el detalle</span>
        </div>`;
      } else {
        card.classList.add("flipped");
        card.innerHTML = <div style="padding:10px; font-size: 1em; font-weight: normal;">${text}</div>;
      }
    }

    function checkAnswer(element, isCorrect, questionId) {
      const questionDiv = element.closest('.question-block');
      // Usar la clase 'answered' para evitar que se responda dos veces
      if (questionDiv.classList.contains('answered')) return; 

      // Deshabilitar todas las opciones para esta pregunta
      questionDiv.querySelectorAll('.option').forEach(opt => {
          opt.onclick = null;
          opt.style.cursor = 'default';
      });
      
      if (isCorrect) {
        element.style.backgroundColor = "#d4edda";
        element.style.borderColor = "#28a745";
        element.innerHTML += ' ✅';
      } else {
        element.style.backgroundColor = "#f8d7da";
        element.style.borderColor = "#dc3545";
        element.innerHTML += ' ❌';
        
        // Muestra la respuesta correcta
        questionDiv.querySelectorAll('.option').forEach(opt => {
            // Se puede usar el color de fondo para saber cuál es la correcta
            if (opt.onclick && opt.onclick.toString().includes('true')) { 
                 opt.style.backgroundColor = "#fff3cd";
                 opt.style.borderColor = "#ffc107";
                 opt.innerHTML += ' (Correcta)';
            }
        });
      }
      
      questionDiv.classList.add('answered');
    }
    
    // --- LÓGICA DE NUCITA (IA) ---
    function sendMessageFromSelect() {
        const select = document.getElementById('chatSelect');
        const key = select.value;
        const messages = document.getElementById('chatMessages');

        if (!key) return;

        // Mostrar mensaje del usuario (simulado por la selección)
        messages.innerHTML += <div class="message user-message">Quiero saber sobre ${programsData[key].title}</div>;

        // Scroll al fondo
        messages.scrollTop = messages.scrollHeight;
        select.value = ""; // Resetear select

        // Simular "pensando"
        setTimeout(() => {
            const data = programsData[key];
            const response = <strong> Objetivo del Programa de ${data.title}:</strong><br><br>${data.objective};

            messages.innerHTML += <div class="message bot-message">${response}</div>;
            messages.scrollTop = messages.scrollHeight;
        }, 600);
    }

    // Inicializar chatbot (oculto por defecto)
    document.getElementById('chatbot').classList.remove('active');
  </script>
</body>
</html>
