<!DOCTYPE html>
<html ng-app="myMod">
<head>
  <title>Bootstrap 5 Website Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.8.3/angular.min.js" integrity="sha512-KZmyTq3PLx9EZl0RHShHQuXtrvdJ+m35tuOiwlcZfs/rE7NZv29ygNA8SFCkMXTnYZQK2OX0Gm2qKGfvWEtRXA==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
  <script src="routing.js"></script>
  <style>
    .row {
      height: 400px;
    }
    .content {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
      background-image: "home.jpeg"; /* Optional: to make ng-view background white */
    }
    .fa-twitter{
      float:right;
      
    }
    .fa-youtube{
      float:right;
    }
    .fa-instagram{
      float:right;
    }
    .fa-facebook{
      float:right;
    }
    .fa-brands{
      margin-right:25px;
      padding: 5px;
    }
    
  </style>
</head>
<body ng-controller="myctrl">

<div class="p-1 bg-danger text-black text-left">
  <h1>SHARDA  DEVI  COLLEGE &nbsp;

  <i class="fa-solid fa-building-columns"></i></h1>
</div>
 


  <div class="row">
    <div class="col-sm-2 bg-black text-white p-3">
      <ul class="list-unstyled">
        <li><a href="#!Home" class="text-white">Home</a></li><br>
        <li><a href="#!Abouts" class="text-white">Abouts</a></li><br>
        <li><a href="#!Academics" class="text-white">Academics</a></li><br>
        <li><a href="#!Administration" class="text-white">Administration</a></li><br>
        <li><a href="#!Admission" class="text-white">Admission</a></li><br>
      </ul>
    </div>
    <div class="col-sm-6 content">
      <div ng-view></div>
    </div>
  </div>
</div>
<div class="p-1 bg-warning text-black text-right">
  Get connected with us on social networks:
  <i class="fa-brands fa-twitter"></i>  
  <i class="fa-brands fa-youtube"></i> 
  <i class="fa-brands fa-instagram"></i> 
  <i class="fa-brands fa-facebook"></i>
  </div>


  <footer class="bg-primary text-white text-center text-lg-start">
    <!-- Grid container -->
    <div class="container p-4">
      <!--Grid row-->
      <div class="row">
        <!--Grid column-->
        <div class="col-lg-6 col-md-12 mb-4 mb-md-0">
          <h5 class="text-uppercase">CONTACT</h5>
  
          <p>
            SHARDA DEVI COLLEGE
            KOLKATA
            <br>
            <br>
            <i class="fa-solid fa-house"></i> &nbsp;
            30, Mother Teresa Sarani,
            Kolkata - 700016,<br>
            &nbsp; &nbsp; &nbsp; &nbsp; West Bengal, India
            <br>
            <i class="fa-solid fa-envelope"></i> &nbsp;
            
            &nbsp;contact@sdc.edu<br>
            <i class="fa-solid fa-phone"></i> &nbsp;

            &nbsp;Reception: 033-2255-1101
          </p>
        </div>
        <!--Grid column-->
  
        <!--Grid column-->
        <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
          <h5 class="text-uppercase">Academics</h5>
  
          <ul class="list-unstyled mb-0">
            <li>
              <a href="#!" class="text-white">Departments</a>
            </li>
            <li>
              <a href="#!" class="text-white">Programs Offered</a>
            </li>
            <li>
              <a href="#!" class="text-white">Academic Calendar</a>
            </li>
            <li>
              <a href="#!" class="text-white">Syllabi</a>
            </li>
          </ul>
        </div>
        <!--Grid column-->
  
        <!--Grid column-->
        <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
          <h5 class="text-uppercase mb-0">Facilities</h5>
  
          <ul class="list-unstyled">
            <li>
              <a href="#!" class="text-white">Library</a>
            </li>
            <li>
              <a href="#!" class="text-white">Online Payment</a>
            </li>
            <li>
              <a href="#!" class="text-white">Student's Counselling</a>
            </li>
            <li>
              <a href="#!" class="text-white">Campus Placement Cell</a>
            </li>
          </ul>
        </div>
        <!--Grid column-->
      <!--Grid row-->
    </div>
    <!-- Grid container -->
  
    <!-- Copyright -->
    <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2);">
      © 2024 Copyright:
      <a class="text-white" href="https://shardadevicollege.com/">shardadevicollege.com</a>
    </div>
    <!-- Copyright -->
  </footer>
</div>

<script>
  var app = angular.module("myMod", ['ngRoute']);
  app.config(["$routeProvider", function($routeProvider) {
    $routeProvider
      .when("/Home", {
        templateUrl: "views/Home.html"
      })
      .when("/Abouts", {
        templateUrl: "views/Abouts.html"
      })
      .when("/Academics", {
        templateUrl: "views/Academics.html"
      })
      .when("/Administration", {
        templateUrl: "views/Administration.html"
      })
      .when("/Admission", {
        templateUrl: "views/Admission.html"
      })
      .otherwise({
        redirectTo: "project.html"  // Use a valid redirect path
      });
  }]);

  app.controller("myctrl", function($scope) {
    // Controller logic here
  });
</script>

</body>
</html>
