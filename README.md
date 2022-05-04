# CRUD Operation For Books Performed By Library Admin

Introduction

This is Django based project. The Book is the project and LMS is an aap. In this, Admin signup, signin, signout functionalities are available. Admin can perform CRUD operation for books. It means an Admin can add a book, retrieve a book, update a book or delete a book. The book data is stored in MySql database. Also Admin data is stored inside the database. For UI, Bootstrap is used. A student can view all the available books.

1. models.py

There are two models in models.py file, AllBooks and Details_admin. After this, you need to run migrations and run the server. Now tables will be created in the database. The Details_admin stores the admin data and AllBooks stores the data regarding the books in the database.

2. forms.py

In this file, there are two forms, Admin and Add_book. To create these forms, you need to import models from models.py file and forms from django. The Admin form is used for admin signup and Add_book form is used for adding the book. In Admin form, there is a function clean_email, this function is written for not accepting the email which is already exist. 

3. templates

There are six templates inside the LMS aap. These are:
    
    1. index.html
    2. show_books.html
    3. Signin.html
    4. signup.html
    5. student_view.html
    6. update.html

4. views.py

There are many functions in this file. All are explained below:

    1. index

        This function will render to index.html template. In this, the bootstrap files are loaded in the script tag.

    2. Admin_signup

        This function provides the Admin form after the post request. It saves the user data in the database and render to signup.html.

    3. signin

        This provides the signin form after the post request. It checks wheather the user information matches with the database information. If it matches then it renders to the books url that is show_books.html. If it doest not then remains on the same page.

    4. signout

        This is for logout and redirected to the home that is signup.html.

    5. add_show_books

        This provides a form to add a book into the database. Also it shows all the available books with the update and delete options.

    6. update

        It is for updating the book information. 

    7. delete_book

        This is for deleting the book.
        
    8. student_view

        This will show all the available books.

5. urls.py\Book

    This provides urls for a project.

6. urls,py\LMS

    This provides urls for an aap. You need to import views from LMS.
