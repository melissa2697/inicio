<!DOCTYPE html>
<html>
<title>E-Truck</title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Raleway">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>
  body,
  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    font-family: "Raleway", sans-serif
  }

  .popup {
  visibility: hidden;}

  .popup .show {
  visibility: visible;}
</style>

<body>

  <!-- Sidebar/menu -->

  <nav class="w3-sidebar w3-bar-block w3-white w3-animate-left" style="display:none;z-index:3;width:300px;"
    id="mySidebar">
    <div class="w3-container">
      <a href="#close" onclick="w3_close()" class="w3-button w3-right" title="Cerrar"><i
          class="fa fa-close fa-fw w3-margin-left"></i></a>
      <h4><b>MENÚ</b></h4>
    </div>
    <div class="w3-bar-block">
      <a href="#inicio" onclick="w3_close()" class="w3-bar-item w3-button w3-padding"><i
          class="fa fa-user fa-fw w3-margin-right"></i>Iniciar Sesión</a>
      <a href="#registro" onclick="w3_close() ; myFunction()" class="w3-bar-item w3-button w3-padding"><i
          class="fa fa-user-plus fa-fw w3-margin-right"></i>Registro</a>
      <a href="#reserva" onclick="w3_close()" class="w3-bar-item w3-button w3-padding"><i
          class="fa fa-search fa-fw w3-margin-right"></i>Consultar Reserva</a>
      <a href="#pregunta" onclick="w3_close()" class="w3-bar-item w3-button w3-padding"><i
          class="fa fa-question fa-fw w3-margin-right"></i>Preguntas Frecuentes</a>
      <a href="#quienesomos" onclick="w3_close()" class="w3-bar-item w3-button w3-padding"><i
          class="fa fa-users fa-fw w3-margin-right"></i>Quienes Somos</a>
      <a href="#contact" onclick="w3_close()" class="w3-bar-item w3-button w3-padding"><i
          class="fa fa-envelope fa-fw w3-margin-right"></i>Contacto</a>
    </div>
  </nav>

  <!-- Top menu -->
  <div class="w3-top">
    <div class="w3-black w3-large w3-padding-45" style="height:58px; margin:auto">
      <span class="w3-button w3-padding w3-left" onclick="w3_open()" title="Menu"><i class="fa fa-bars"></i></span>
      <a href="#login" class="w3-button w3-hide-small w3-right w3-padding" title="Login"><i
          class="fa fa-user fa-fw w3-margin-right"></i></a>
      <a href="#Preguntas_Frecuentes" class="w3-button w3-hide-small w3-right w3-padding"
        title="Preguntas Frecuentes"><i class="fa fa-question fa-fw w3-margin-right"></i></a>
      <a href="#Consulta" class="w3-button w3-hide-small w3-right w3-padding" title="Consulta Tu Reserva"><i
          class="fa fa-search fa-fw w3-margin-right"></i></a>
      <div class="w3-display-middle w3-padding">
        <h3 class="w3-xlarge"><b>E-TRUCK</b></h3>
      </div>
    </div>
  </div>


  <!--Contenedor-->

  <div class="w3-black w3-large w3-padding" style="height:165px ;margin-top:58px">
    <div class="w3-content w3-opacity" style="max-width:850px;margin-top:80px;margin-bottom:80px; margin:auto">
      <!-- Slideshow -->
      <div class="w3-container">
        <div class="w3-display-container mySlides">
          <img
            src="http://www.transportescallizo.com/wp-content/uploads/2019/07/transporte-de-mercanc%C3%ADas-por-carretera-Callizo.jpg"
            style="width:100%">
        </div>
        <div class="w3-display-container mySlides">
          <img
            src="http://www.transportescallizo.com/wp-content/uploads/2019/05/transportes-de-mercanc%C3%ADas-peligrosas-Callizo.jpg"
            style="width:100%">
        </div>
        <div class="w3-display-container mySlides">
          <img src="http://www.transportescallizo.com/wp-content/uploads/2020/07/grupaje-en-el-transporte-Callizo.jpg"
            style="width:100%">
        </div>
      </div>
    </div>
  </div>



  <!-- Overlay effect when opening sidebar on small screens -->
  <div class="w3-overlay w3-hide-large w3-animate-opacity" onclick="w3_close()" style="cursor:pointer"
    title="close side menu" id="myOverlay"></div>


  <!--Secciones-->
  <div class="w3-container">
    <div class="w3-content" style="max-width: 850px; margin-top: 80px; margin-bottom: 80px; margin: auto;">
      <di class="popup" id="registro">
        <a>Nombres:</a>
        <p><input class="w3-input w3-padding-10 w3-border" type="text" placeholder="Name" required name="Name"></p>
        <a>Email:</a>
        <p><input class="w3-input w3-padding-10 w3-border" type="text" placeholder="Email" required name="Email"></p>
        <a>Contacto:</a>
        <p><input class="w3-input w3-padding-10 w3-border" type="text" placeholder="Message" required name="Contact">
        </p>
      </di>
    </div>
  </div>

  <!--Pie de pagina-->
  <!-- <footer class="w3-padding-32 w3-black w3-center w3-margin-top">
            <a href="#RegistraReserva" class="w3-button w3-hide-small w3-right w3-padding"><i
              class="fa fa-doc-plus fa-fw w3-margin-right"></i>Iniciar Reserva</a>            
      </footer>
-->
  <script>
    // Script to open and close sidebar
    function w3_open() {
      document.getElementById("mySidebar").style.display = "block";
      document.getElementById("myOverlay").style.display = "block";
    }

    function w3_close() {
      document.getElementById("mySidebar").style.display = "none";
      document.getElementById("myOverlay").style.display = "none";
    }


    // Script Slideshow 

    var slideIndex = 0;
    carousel();

    function carousel() {
      var i;
      var x = document.getElementsByClassName("mySlides");
      for (i = 0; i < x.length; i++) {
        x[i].style.display = "none";
      }
      slideIndex++;
      if (slideIndex > x.length) { slideIndex = 1 }
      x[slideIndex - 1].style.display = "block";
      setTimeout(carousel, 2000); // Change image every 2 seconds
    }

    function myFunction() {
      var popup = document.getElementById("registro");
      popup.classList.toggle("show");
    }


  </script>

</body>

</html>
