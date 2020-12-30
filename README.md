# LoginAndRegister-with-phpMyAdmin-



 In this project I connected the login and register form to MySQL database using phpMyAdmin.

The first thing you need to do is download MySQL connector for accessing the database. 
Then you have to create a class (MyConnection) to connect the login and register forms to the database.

In the register form you need to create a function (checkUsername) to check if the username you want to register already exists in the database.

The following is a list of actions you will need to check when the user clicks on the register button:

- if the username field is empty
- if the password field is empty
- if the retype_password field matches the password field when creating new password.
- if the username already exists in the database.
- if the Date field (jDateChooser) is empty

The login form is straight-forward;
the user enter his or her login and password and clicks on the login button,

and all you need to do is to check if a user with this username and password already exists in the database, and if the user doesn’t exists show a warning message, else show a new form with the user username displayed on a jlabel or in this case a “welcome page”.

 This is the class "MyConnection" that connects the forms to the phpMyAdmin Database : 



![1 0-ConnectionClass](https://user-images.githubusercontent.com/20470279/60298939-970cfc00-98f9-11e9-85f2-31bc04c38f39.JPG)




The following pictures displays the functions that checks to see if the username already exist in the database table : 

![1 1-UserExists](https://user-images.githubusercontent.com/20470279/60299118-f2d78500-98f9-11e9-9b98-1d1c6f38baf3.JPG)


![1 2-UnameAlreadyExist](https://user-images.githubusercontent.com/20470279/60299150-0a167280-98fa-11e9-85d7-9b39c8a9dff8.JPG)



The following picture is an example of the user being granted access when entering the correct username and password : 


![1 3](https://user-images.githubusercontent.com/20470279/60299690-50200600-98fb-11e9-8215-d100fbe837f7.JPG)


The following code is for the register click button :


![2 0-regcode-SQLConnect](https://user-images.githubusercontent.com/20470279/60299782-88bfdf80-98fb-11e9-80e9-926e71868801.JPG)


The following is example of a jar file I downloaded for the date chooser of the netbeans palette, but happened to be bugged and it caused the register form to compile with errors :


![2 1-date error_LI](https://user-images.githubusercontent.com/20470279/60300214-7f834280-98fc-11e9-8287-31c6800b4455.jpg)

![2 11-date jar malfunction](https://user-images.githubusercontent.com/20470279/60300265-9de93e00-98fc-11e9-8082-8af467e8dabc.JPG)

The following example is the jar file I downloaded and added to the palette in netbeans. This allowed me to use the date chooser in the Register form and compiled it with no errors.


![2 20-date_jar works](https://user-images.githubusercontent.com/20470279/60300310-b6f1ef00-98fc-11e9-9b9f-003197bc806a.JPG)

The following example shows the user’s registration being added to the phpMyAdmin Database. This was successful after replacing the jDateChooser. Also, there was a message that came to the output stating the driver used for the MySQL connection driver was deprecated or no longer being used. Despite the fact, it still compiled because the new driver was automatically applied in this case. 


![2 30-datapops](https://user-images.githubusercontent.com/20470279/60300613-59aa6d80-98fd-11e9-857f-0a443900d4a2.jpg)

![2 40-data populated](https://user-images.githubusercontent.com/20470279/60300693-86f71b80-98fd-11e9-87af-7ed7637d1dc9.JPG)

The following examples below display the code for prompting the user when the wrong password is retyped in the registration and when there is NO username typed into the registration form : 

![3 1-showdialogMessage](https://user-images.githubusercontent.com/20470279/60300792-c0c82200-98fd-11e9-9fab-1a6e83643947.JPG)

![3 2-userCheck](https://user-images.githubusercontent.com/20470279/60300830-d76e7900-98fd-11e9-987f-4c92e803fed8.JPG)
![3 3-password check](https://user-images.githubusercontent.com/20470279/60300834-d9383c80-98fd-11e9-94e0-c139010fc369.JPG)
