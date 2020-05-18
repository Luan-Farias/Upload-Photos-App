<h1 align="center">Photo Upload App (backend)</h1>
<p>This is backend of a photo upload app, here where the photo will be treated</p>

---

<p>The application's backend has only three routes></p>

- - -
- One to upload photos
- One to get photos informations from database
- One to delete photos

# Post Route
<p>The post route have the funcion to upload photos. The route can be acessed by base_url/posts in a post request. In the body of request may have the photo that will be trated</p>

<h3>How the photos is uploaded?</h3>

<p>The steps of upload of photo are simple</p>

- - -
- First step: a request is maden to backend and in the body of request are a file
- Second step: the app verify if the file has less that 2MB
- Third step: the file is validated to the program have sure that is a photo
- Fourth step: the file is send to s3 of aws
- Fifth step: a  new record is created on mongodb to have acess to photo
- Sixth step: is returned in json a response with the informations of the phot

# Get Route
<p>The get route have the funcion to get informations of the photos. The route can be acessed by base_url/posts in a get request. </p>

<h3>How the photos is get?</h3>

<p>The steps of upload of photo are this</p>

- - -
- First step: a request is maden to backend
- Second step: the app get all records of database
- Third step: the app response with a json all photos information

# Delete Route
<p>The delete route have the funcion to delete photos. The route can be acessed by base_url/posts/:id in a delete request. </p>

<h3>How the photos is deleted?</h3>

<p>The steps of upload of photo are this</p>

- - -
- First step: a request is maden to backend
- Second step: the app get the id of photo that is passed in the route
- Third step: the app delete the photo in database 
- Fourth step: the photo is deleted in aws

---

<p>Simple, isn't it? For development ambient you can change to use aws and use localstorage</p>

