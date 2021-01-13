
//DB SQL
CREATE  TABLE IF NOT EXISTS `Users` (
  `id` INT  AUTO_INCREMENT ,
  `first_name` VARCHAR(150) NOT NULL ,
  `last_name` VARCHAR(150) NOT NULL ,
  `email` VARCHAR(255),
  `password` VARCHAR(255),
  PRIMARY KEY (`id`) );


// Register
Method: post 
Endpoint: http://127.0.0.1:8080/api/register.php
body:(raw) application/json
{
    "first_name": "topu",
    "last_name" : "mahmud",
    "email":"mahmudtopu3@gmail.com",
    "password" : "admin123"
}

//Login
Method: post 
Endpoint: http://127.0.0.1:8080/api/register.php
body:(raw) application/json
{
    "email" : "mahmudtopu3@gmail.com",
    "password" : "admin123"
}

//Protected
Method: post 
Endpoint: http://127.0.0.1:8080/api/protected.php
headers: 
content-type:application/json
Authorization:Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJUSEVfSVNTVUVSIiwiYXVkIjoiVEhFX0FVRElFTkNFIiwiaWF0IjoxNjEwNTU2MDg2LCJuYmYiOjE2MTA1NTYwOTYsImV4cCI6MTYxMDU1NjY4NiwiZGF0YSI6eyJpZCI6IjEiLCJmaXJzdG5hbWUiOiJ0b3B1IiwibGFzdG5hbWUiOiJtYWhtdWQiLCJlbWFpbCI6Im1haG11ZHRvcHUzQGdtYWlsLmNvbSJ9fQ.pSR5KMN_p75OxphZpex0LwJQoSnI3QfpYCRBATrC8rg