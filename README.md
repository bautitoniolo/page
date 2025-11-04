<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mis Proyectos</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: #101020;
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 0;
      min-height: 100vh;
    }

    h1 {
      margin-top: 30px;
    }

    .projects {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }

    .project-card {
      background: #1e1e2f;
      padding: 20px;
      border-radius: 15px;
      width: 250px;
      cursor: pointer;
      text-align: center;
      transition: 0.3s;
      box-shadow: 0 6px 15px rgba(0,0,0,0.3);
    }

    .project-card:hover {
      transform: translateY(-5px);
      background: #2a2a40;
    }

    .project-card img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 10px;
    }

    .project-detail {
      display: none;
      width: 90%;
      max-width: 900px;
      background: #1e1e2f;
      margin-top: 40px;
      border-radius: 20px;
      padding: 20px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.4);
    }

    iframe {
      width: 100%;
      height: 500px;
      border: none;
      border-radius: 10px;
    }

    .back-btn {
      margin-bottom: 15px;
      padding: 10px 15px;
      background: #00b894;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .back-btn:hover {
      background: #00d8aa;
    }
  </style>
</head>
<body>
  <h1>NUESTROS PROYECTOS</h1>

  <div class="projects">
    <div class="project-card" onclick="showProject('proyecto1')">
      <img src="index.html" alt="">
      <h3>Calculadora Moderna</h3>
      <p>Proyecto interactivo hecho en HTML, CSS y JS</p>
    </div>

    <div class="project-card" onclick="showProject('proyecto2')">
      <img src="temporizador.html" alt="">
      <h3>Gestor de Stock</h3>
      <p>CRM con base de datos en Firebase</p>
    </div>

    <div class="project-card" onclick="showProject('proyecto3')">
      <img src="conversor de unidades.html" alt="">
      <h3>Asistente Legal</h3>
      <p>Aplicación con IA y automatización</p>
    </div>
  </div>

  <!-- Contenedor del proyecto 1 -->
  <div id="proyecto1" class="project-detail">
    <button class="back-btn" onclick="goBack()">← Volver</button>
    <iframe src="index.html"></iframe>
  </div>

  <!-- Contenedor del proyecto 2 -->
  <div id="proyecto2" class="project-detail">
    <button class="back-btn" onclick="goBack()">← Volver</button>
    <iframe src="temporizador.html"></iframe>
  </div>

  <!-- Contenedor del proyecto 3 -->
  <div id="proyecto3" class="project-detail">
    <button class="back-btn" onclick="goBack()">← Volver</button>
    <iframe src="conversor de unidades.html"></iframe>
  </div>

  <script>
    function showProject(id) {
      document.querySelector('.projects').style.display = 'none';
      document.getElementById(id).style.display = 'block';
    }

    function goBack() {
      document.querySelectorAll('.project-detail').forEach(div => div.style.display = 'none');
      document.querySelector('.projects').style.display = 'flex';
    }
  </script>
</body>
</html>
