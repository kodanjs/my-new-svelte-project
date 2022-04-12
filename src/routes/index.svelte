
  <nav>
    <div class="nav-wrapper  blue-grey darken-1">
      <a href="#" class="brand-logo">Logo</a>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
        <li><a href="sass.html">Sass</a></li>
        <li><a href="badges.html">Components</a></li>
        <li><a href="collapsible.html">JavaScript</a></li>
      </ul>
    </div>
  </nav>
  <div class="row">
    <div class="col s12 m6">
      <div class="card blue-grey darken-1">
        <div class="card-content white-text">
          <span class="card-title">Card Title</span>
          <p>I am a very simple card. I am good at containing small bits of information.
          I am convenient because I require little markup to use effectively.</p>
        </div>
        <div class="card-action">
          <a href="#">This is a link</a>
          <a href="#">This is a link</a>
        </div>
      </div>
    </div>
  </div>
  <!DOCTYPE html>
  <html lang="en">
  
  <head>
      <title>
          How to Integrate Webcam using
          JavaScript on HTML5 ?
      </title>
      <link rel="stylesheet" href="css/style.css">
      <link href=
  "https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"
              rel="stylesheet">
  
      <script src=
  "http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"
      type="text/javascript">
  
      </script>
  
      <script src=
  "https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.bundle.min.js">
      </script>
  </head>
  
  <body>
      <div class="container">
          <div class="row">
              <div class="col-sm-12">
                  <div class="card">
                      <h5 class="card-header h5 text-center">
                          HTML 5 & JS live Cam
                      </h5>
                      <div class="card-body">
                          <div class="booth">
                              <video id="video" width="100%"
                                  height="100%" autoplay>
                              </video>
                          </div>
  
                          <div class="text-right">
                              <a href="#!" class="btn btn-danger"
                                  onClick="stop()">
                                  Stop Cam
                              </a>
                              <a href="#!" class="btn btn-success"
                                  onClick="start()">
                                  Start Cam
                              </a>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
  
      <script>
          var stop = function () {
              var stream = video.srcObject;
              var tracks = stream.getTracks();
              for (var i = 0; i < tracks.length; i++) {
                  var track = tracks[i];
                  track.stop();
              }
              video.srcObject = null;
          }
          var start = function () {
              var video = document.getElementById('video'),
                  vendorUrl = window.URL || window.webkitURL;
              if (navigator.mediaDevices.getUserMedia) {
                  navigator.mediaDevices.getUserMedia({ video: true })
                      .then(function (stream) {
                          video.srcObject = stream;
                      }).catch(function (error) {
                          console.log("Something went wrong!");
                      });
              }
          }
          $(function () {
              start();
          });
      </script>
  </body>
  
  </html>
  