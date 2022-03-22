
https://angular.io/guide/setup-local


npm install -g @angular/cli

ng new <my-app>

cd my-app
ng serve --open

ng serve --open --port 4201

ng generate component




npm install bootstrap 

añadir en agular.json la siguiente ruta. 

            "styles": [
              "node_modules/bootstrap/dist/css/bootstrap.min.css",
              "src/styles.css"
            ],
            "scripts": [
              "node_modules/bootstrap/dist/js/bootstrap.min.js"
            ]



crear archivo server.js 



const express = require('express');
 const path = require('path'); 
 const app = express(); 
 app.use(express.static(__dirname + '/dist/<my-angular-app>'));
  app.get('/*', function(req,res) {res.sendFile(path.join(__dirname+'/dist/<my-angular-app>/index.html'));});
   app.listen(process.env.PORT || 8080);






  