# webdev_assessment2  
-npm init  
-npm install nodemon, express, mongoose, body-parser, dotenv, joi, jsonwebtoken, bcryptjs  
-Adjust the `start` file in the package.json  
    "scripts": {  
        "start": "nodemon app.js"  
    }  
- Run using `npm start`
  
URL - http://localhost:3000 (postman: localhost:3000)   
  
**POST /users/register** : register a new user  
**Request Body**:  
   {  
     "name": "Anna",  
     "email": "anna@example.com",  
     "password": "123456"  
   }  
  
**POST /users/login** : login an existing user, receive a token  
**Request Body**: 
   {  
     "email": "anna@example.com",  
     "password": "123456"  
   }  
  
**POST /posts** : create a new post, verification necessary  
**Headers**: {auth-token:######}  
**Request Body**:   
   {  
     "title": "This is a post",  
     "description": "Description of my first post"  
   }  

**GET /posts** : get all posts, no verification necessary  
  
**GET /posts/_id** : get one post, no verification necessary   
  
**PATCH /posts/_id** : update an existing post, verification necessary--must be the creator  
**Headers**: {auth-token:######}  
**Request Body**:   
   {  
     "title": "This is an updated post",  
     "description": "Description of my updated post"  
   }  
  
**DELETE /posts/_id** : delete an existing post, verification necessary--must be the creator    
**Headers**: {auth-token:######}  
