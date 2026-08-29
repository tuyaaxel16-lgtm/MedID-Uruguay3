```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MedID Uruguay - Mateo Velazco</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f3f7fa;
      color: #17212b;
    }

    header {
      background: #0b7285;
      color: white;
      padding: 25px 20px;
      text-align: center;
    }

    header h1 {
      font-size: 32px;
      margin-bottom: 8px;
    }

    header p {
      font-size: 16px;
    }

    .container {
      max-width: 700px;
      margin: 30px auto;
      padding: 0 20px;
    }

    .inicio {
      background: white;
      border-radius: 18px;
      padding: 30px 25px;
      margin-bottom: 20px;
      box-shadow: 0 5px 18px rgba(0,0,0,0.08);
      text-align: center;
    }

    .inicio h2 {
      color: #0b7285;
      margin-bottom: 10px;
    }

    .inicio p {
      color: #667781;
      margin-bottom: 20px;
    }

    .boton {
      display: block;
      text-align: center;
      background: #0b7285;
      color: white;
      padding: 15px;
      border-radius: 10px;
      margin-top: 12px;
      font-weight: bold;
      cursor: pointer;
      border: none;
      width: 100%;
      font-size: 16px;
    }

    .boton:hover {
      background: #095c6b;
    }

    .boton.privado {
      background: #495057;
    }

    .boton.privado:hover {
      background: #343a40;
    }

    .card {
      background: white;
      border-radius: 18px;
      padding: 25px;
      margin-bottom: 20px;
      box-shadow: 0 5px 18px rgba(0,0,0,0.08);
    }

    .card h2 {
      color: #0b7285;
      margin-bottom: 15px;
    }

    .dato {
      padding: 12px 0;
      border-bottom: 1px solid #e5e5e5;
      line-height: 1.5;
    }

    .dato:last-child {
      border-bottom: none;
    }

    .dato strong {
      display: block;
      margin-bottom: 4px;
    }

    .alerta {
      background: #fff3cd;
      border-left: 5px solid #f0ad4e;
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
      line-height: 1.5;
    }

    .emergencia {
      background: #ffe5e5;
      border-left: 5px solid #d62828;
      padding: 18px;
      border-radius: 8px;
      margin-top: 15px;
      line-height: 1.6;
    }

    .paso {
      background: #f3f7fa;
      padding: 12px;
      border-radius: 8px;
      margin-top: 8px;
    }

    .oculto {
      display: none;
    }

    footer {
      text-align: center;
      padding: 25px;
      color: #667781;
      font-size: 14px;
    }
  </style>
</head>

<body>

<header>
  <h1>MedID Uruguay</h1>
  <p>Información médica de emergencia</p>
</header>

<div class="container">

  <!-- PANTALLA INICIAL -->
  <div class="inicio" id="inicio">

    <h2>👋 Bienvenido a MedID</h2>

    <p>
      Perfil médico de <strong>Mateo Velazco</strong>
    </p>

    <button class="boton" onclick="mostrarEmergencia()">
      🩺 Ver información de emergencia
    </button>

    <button class="boton privado" onclick="mostrarPrivado()">
      🔐 Ver información privada
    </button>

  </div>


  <!-- INFORMACIÓN DE EMERGENCIA -->
  <div id="emergencia" class="oculto">

    <div class="card">

      <h2>🩺 Identificación</h2>

      <div class="dato">
        <strong>Nombre</strong>
        Mateo Velazco
      </div>

      <div class="dato">
        <strong>Documento</strong>
        Información protegida
      </div>

      <div class="dato">
        <strong>Grupo sanguíneo</strong>
        O+
      </div>

    </div>


    <div class="card">

      <h2>🚨 Información de emergencia</h2>

      <div class="dato">
        <strong>Antecedente</strong>
        Síncope vasovagal
      </div>

      <div class="dato">
        <strong>Situación</strong>
        Puede presentar mareos, debilidad y desmayo debido a una disminución momentánea de la presión arterial.
      </div>

      <div class="dato">
        <strong>Alergias</strong>
        No especificadas
      </div>


      <div class="emergencia">

        <strong>⚠️ ¿Qué hacer si Mateo se desmaya?</strong>

        <div class="paso">
          <strong>1. Mantener la calma</strong><br>
          Evitar que se levante rápidamente.
        </div>

        <div class="paso">
          <strong>2. Acostarlo boca arriba</strong><br>
          Colocarlo en un lugar seguro.
        </div>

        <div class="paso">
          <strong>3. Elevar las piernas</strong><br>
          Puede ayudar a mejorar el retorno de sangre.
        </div>

        <div class="paso">
          <strong>4. Comprobar que respire normalmente</strong><br>
          Vigilar su estado mientras se recupera.
        </div>

        <div class="paso">
          <strong>5. Pedir ayuda si es necesario</strong><br>
          Si no responde, no respira normalmente o la situación parece grave, solicitar asistencia médica de emergencia.
        </div>

      </div>


      <div class="alerta">
        💡 <strong>Función de MedID:</strong>
        Al escanear la pulsera NFC se abre directamente el perfil de Mateo, permitiendo consultar rápidamente qué hacer ante una emergencia.
      </div>

      <button class="boton" onclick="volverInicio()">
        ← Volver
      </button>

    </div>

  </div>


  <!-- INFORMACIÓN PRIVADA -->
  <div id="privado" class="oculto">

    <div class="card">

      <h2>🔐 Información privada</h2>

      <div class="dato">
        <strong>Nombre completo</strong>
        Mateo Velazco
      </div>

      <div class="dato">
        <strong>Fecha de nacimiento</strong>
        22/09/2010
      </div>

      <div class="dato">
        <strong>Dirección</strong>
        Información protegida
      </div>

      <div class="dato">
        <strong>Contacto familiar</strong>
        Información protegida
      </div>

      <div class="dato">
        <strong>Teléfono de emergencia</strong>
        Información protegida
      </div>

      <div class="alerta">
        🔒 Esta información está destinada únicamente a personas autorizadas.
      </div>

      <button class="boton" onclick="volverInicio()">
        ← Volver
      </button>

    </div>

  </div>

</div>


<footer>
  MedID Uruguay © 2026
</footer>


<script>

  function ocultarTodo() {
    document.getElementById("inicio").style.display = "none";
    document.getElementById("emergencia").style.display = "none";
    document.getElementById("privado").style.display = "none";
  }

  function mostrarEmergencia() {
    ocultarTodo();
    document.getElementById("emergencia").style.display = "block";
  }

  function mostrarPrivado() {
    ocultarTodo();
    document.getElementById("privado").style.display = "block";
  }

  function volverInicio() {
    ocultarTodo();
    document.getElementById("inicio").style.display = "block";
  }

</script>

</body>
</html>
```