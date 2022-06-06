# PERSONAL LIBRARY APP

Go to https://github.com/MarcinPekala/ppfrontend for frontend repository

# 1. General description

> Will add a general description after publishing the final version of the application under this address:
> https://github.com/MarcinPekala/ppbackend/wiki


## 1.1 Application's name
*Personal Library App*

## 1.2 Application's purpose
The main reason behind this application development was to implicate in practice the skills I gathered regarding the development of REST API applications using Spring Boot Java on Gradle project in a form of personal project with separate repositories for frontend and backend.
</br></br>
The purpose of *Personal Library App* is to help people organize their books' collection on a web based app with multiple functions.

## 1.3 Brief summary of application

<img src="https://github.com/MarcinPekala/readme_images/blob/master/FRONT.png" width="800"/>

### Backend:
REST API writen in Java's Spring Boot with usage of following technologies in the project:

<ul>
    <li>H2 databse (or MySQL database upon personal configuration)</li>
      <li>Spring Data JPA</li>
    <li>Swagger.io</li>
    <li>Spring Actuator (Reconsidering inclusion)</li>
        <li>Google GSON</li>
        <li>Mockito for JUnit tests</li>
  <li>Spring Hibernate</li>
</ul>
In total backend side has 10 packages, totaling 12 classes, which has about 1288 lines of java according to statistic IntelliJ IDEA plugin and JUnit tests coverage of about 89%. 

### Frontend:
Frontend side was mostly written in HTML/CSS/JS with a Vaadin part currently being under a development. I also used jQuery v3.4.1 framework for js to process HTTPS requests from the REST API. I also used Google Books API and Materialize v0.100.2 for HTML/JS/CSS. Summarizing, I used the following technologies:

<ul>
  <li>HTML/CSS/JS</li>
  <li>Google Books API</li>
  <li>Materialize v0.100.2</li>
  <li>jQuery v3.4.1</li>
  <li>Vaadin (Java framework for web apps)</li>
</ul>

In total frotnend side has 5 packages with 7 java files with about 484 lines of code. Html code has about 162 lines, css about 241 and js about 652.

## 1.4 Target Users

<ul>
  <li><b>Web Admin</b> - A person who manages the server and database on which the application is deployed.</li>
  <li><b>User</b> - A web users, who use this application to manage their personal libraries. 
</ul>

# 2. Description of functionalities

## 2.1 Starting the application

### To start an application you need:
<ul>
<li>JDK and Java up to date</li>
<li>Gradle installed(Not sure if needed. To verify)</li>
</ul>

### In order to start the application you need to do the following steps:

1.	Clone or dowload repositories from: https://github.com/MarcinPekala/ppbackend.git and https://github.com/MarcinPekala/ppfrontend.git
```
You can use the following commands in terminal (for MacOS) to clone the repositories:
  git clone https://github.com/MarcinPekala/ppbackend.git
  git clone https://github.com/MarcinPekala/ppfrontend.git
```

2.	The H2 database is configured automatically but if you want to access the SQL database click the following buttton on the main page (both ppbackend and ppfrontend packages needs to be up and running to access it):

  <img src="https://github.com/MarcinPekala/readme_images/blob/master/DB1.png" width="400"/>

And use the following configuration:

  <img src="https://github.com/MarcinPekala/readme_images/blob/master/DB2.png" width="400"/>
  <img src="https://github.com/MarcinPekala/readme_images/blob/master/DB3.png" width="400"/>

3.	To start the project first we need to:

a) Open a terminal window (for MacOS) and find the location of ppbackend-master on your disk (or ppbackend when cloning the repository) using "ls" and "cd example_path" commands(for MacOS). After you opened the ppbackend-master (or ppbackend) via terminal use the following command:
```
  ./gradlew build
```
<img src="https://github.com/MarcinPekala/readme_images/blob/master/Terminal1.png" width="400"/>

If the application was build successfully then we use the following command to start the application:
```
  ./gradlew bootRun
```

<img src="https://github.com/MarcinPekala/readme_images/blob/master/Terminal2.png" width="400"/>

b) If the backend is succesfully up and running then we repeat all the steps but for ppfrontend-master (or ppfrontend when cloning) in a new terminal window. It might take some time for frontend to start, so don't get discouraged.


<img src="https://github.com/MarcinPekala/readme_images/blob/master/Terminal3.png" width="400"/>
<img src="https://github.com/MarcinPekala/readme_images/blob/master/Terminal4.png" width="400"/>

<img src="https://github.com/MarcinPekala/readme_images/blob/master/Terminal5.png" width="400"/>

4. When both ppbackend-master (or ppbackend) and ppfrontend-master (or ppfrontend) are succesfully up and running we access the following address via search engine of your choice (Google Chrome reccomended): http://localhost:8081

<img src="https://github.com/MarcinPekala/readme_images/blob/master/Localhost.png" width="400"/>

5. To close the application you need to close both terminal windows, which are locally hosting the application's frontend and backend or click "ctrl + c" to stop the apllication without closing the terminal.

## 2.2 Application's abilities and main functionalities

#### 2.2.1 Database size reminder

<img src="https://github.com/MarcinPekala/readme_images/blob/master/DBS.png" width="600"/>

First thing you'll notice is the database size alert, which appears every time when openning the website and also is set to reappear as a reminder every 10 seconds. Just click *OK* to proceed to the website. You can also find the same information in the terminal window on which the backend part is running:

<img src="https://github.com/MarcinPekala/readme_images/blob/master/CONSOLE.png"/>

#### 2.2.2 Accessing the database and endpoints documentation

<img src="https://github.com/MarcinPekala/readme_images/blob/master/TB.png" width="600"/>

On the top right you'll see two buttons. The first one on the left let's you access the endpoints documentation powered by swagger.io, and the second one let's you access the database console in SQL.

<img src="https://github.com/MarcinPekala/readme_images/blob/master/DOCS.png" width="600"/>
<img src="https://github.com/MarcinPekala/readme_images/blob/master/DB2.png" width="600"/>
<img src="https://github.com/MarcinPekala/readme_images/blob/master/DB3.png" width="600"/>

#### 2.2.3 Book form

<img src="https://github.com/MarcinPekala/readme_images/blob/master/FORM.png" width="600"/>

To submit a book into the database you simply enter a book's details into "Book author", "Book title" and "Book's year of publication" fields, and click "Add a book". Not all fields need to be filled. You can also click "Delete all books" but this proccess is irreversible.

#### 2.2.4 Switch to Vaadin front

<img src="https://github.com/MarcinPekala/readme_images/blob/master/FORMV.png" width="600"/>

Under "Add a book" and "Delete all books" button you can see "Switch to Vaadin Frontend" button, which allows you to switch frontend from HTML/CSS/JS based one to Vaadin, which is a Java framework for the web applications. Currently this part is under the development thus the notification window to confirm it will pop-up.

#### 2.2.5 Editing and deleting books from the database

<img src="https://github.com/MarcinPekala/readme_images/blob/master/DBF.png" width="600"/>

Under the form you'll see the list of all books in the database. By clicking "edit" you'll toggle the editing state, which will allow you to rewrite information regarding the book or abort this proccess if you don't want to make any changes. Some fields can be left blank. You can also click "delete" in order to delete a single book from the database by its id.

<img src="https://github.com/MarcinPekala/readme_images/blob/master/DBF2.png" width="600"/>
<img src="https://github.com/MarcinPekala/readme_images/blob/master/DELETE.gif" width="600"/>

#### 2.2.6 Book status, details and book search via Google Books
You can set a book status, from "Bought and read", "Bought but unread" and "To buy" in order to organize your collection by the purpose of the book inserted into the database.

<img src="https://github.com/MarcinPekala/readme_images/blob/master/BOOKSTATUS.gif" width="600"/>

If you want to know more about any book present in the database you can click "details" or "search". The first one will use Google Books API on the separate page where you can click "Get Details", which will initialize the API or click "Get Back" to go back to the main page. On the main page you can also use search, which will instantly direct you to the Google Books search engine.

<img src="https://github.com/MarcinPekala/readme_images/blob/master/BOOKDETAILS.gif" width="600"/>
<img src="https://github.com/MarcinPekala/readme_images/blob/master/BOOKSEARCH.gif" width="600"/>
