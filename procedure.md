## **---------------Procedural commands for the web page development--------------**






1. **First launch an instance through EC2 service in AWS.**

   
2. ##### **Second create a folder and create maven project using the commands by providing project name.**

######    (this command is used to initialize to build the maven project)
           mvn archetype:generate                               

 ###### **After using the command choose web project by choosing the particular number (EX:2292) and provide all the details according to project.**





##### **3. Next once the maven project is created then open the folder in VS code and work on the project by adding code like HTML or by adding any other files.**

##### 

##### **4. Then push the code to the GitHub repository through VS code.**

##### 

##### **5. After that open the Gitbash and paste the SSH that is obtained through the instance after that add these commands.**

##### 

##### **6. To change the user to root user**

###### 
             sudo su -



##### **7. To update the server or repo**

###### 
            apt update



##### **8. To install tomcat 9.0**

###### 
           wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.111/bin/apache-tomcat-9.0.111.tar.gz



##### **9. To install java**

###### 
          apt install openjdk-17-jre-headless -y



##### **10. Add the tar file**

###### 
         tar -zxvf apache-tomcat-9.0.111.tar.gz



##### **11. To remove the tar.gz file**

###### 
         rm -rf apache-tomcat-9.0.111.tar.gz



##### **12. Enter inside the tomcat file**

###### 
         cd apache-tomcat-9.0.111/



##### **13. Check the files or sub files**
######   
          ls
          
(use this command after ls in order come outside the sub files)

          cd    



##### **14. Insert the additional commands inside xml so first use this command**

###### 
          vi apache-tomcat-9.0.111/conf/tomcat-users.xml

###### **(after this command click i and under the rollback add this command)**

###### **#
           <role rolename="manager-gui"/>
           <role rolename="manager-script"/>
           <role rolename="manager-jmx"/>
           <role rolename="manager-status"/>
           <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>


##### **15. To configure webapps** 

###### 
           vi apache-tomcat-9.0.111/webapps/manager/META-INF/context.xml

###### **(after this comment click i and comment cookie line 3 lines from cookie statement)**



##### **16. After this clone the project by pasting the repository url**

###### 
          git clone "paste the repository url"



##### **17. Go inside the repository or inside the project**

###### 
          cd "repository name"/



##### **18. And type this**

###### 
          pwd



##### **19. After that use this command**

###### 
          mvn clean package



##### **20. If the maven is not installed then you have to install maven use**

###### 
          apt install maven



##### **21. Check the version if maven is installed**

###### 
          mvn --version



##### **22. After that go inside the repo or project**

###### 
          cd "repo name"/



##### **23. Use this command**

###### 
         mvn clean package



##### **24. Get outside the project files using**

###### 
         cd ..



##### **25. Copy the files using**

###### 
         cp "repo name"/target/"repo file".war apache-tomcat-9.0.111/webapps/



##### **26. Add the startup file command to start the tomcat**

###### 
         sh apache-tomcat-9.0.111/bin/startup.sh



##### **27. If any changes is made then you have to pull the code so make changes and push the code in VS code after that use this commands one by one **

######    (use this to get inside the repo or project)

          cd "repo name"/    
          
######    (to pull the code to remote repo)

          git pull origin main                                                         

######    (again use this command to build the package)

          mvn clean package                                                            

######    (copy the files again)

          cp "repo name"/target/"repo file".war apache-tomcat-9.0.111/webapps/         

######     (start the server again)

          sh apache-tomcat-9.0.111/bin/startup.sh                                     



##### **28. Now the code will be pulled to remote repo and changes made will be shown/visible**

##### **29. Shortcut link for Maven installation (instead of installing step by step use this to install directly)**

         bash <(curl -sL https://tinyurl.com/52ykfnu5)

 ##### **30. Shortcut link for Tomcat installation (instead of installing step by step use this to install directly)**

         bash <(curl -sL https://tinyurl.com/mrhvupt9)

 ##### **31. Shortcut link for Jenkins installation (instead of installing step by step use this to install directly)**

         bash <(curl -sL https://tinyurl.com/2r6nkffn)

 ##### **32. Docker Installation Commands**

         sudo apt update
         sudo apt  install docker.io -y
         sudo docker --version
         sudo apt install docker-compose -y
         docker-compose --version

 ##### **33. Shortcut link for Prometheus installation (instead of installing step by step use this to install directly)**

         bash <(curl -sL https://tinyurl.com/57xn7sf8)

 ##### **34. MySQL Database on Ubuntu 24.04 Instance**

         # Update and Install MySQL
         sudo apt update && sudo apt upgrade -y
         sudo apt install mysql-server -y
         sudo mysql --version

         # Configure MySQL for Password and Remote Login
         sudo mysql

         # Inside the MySQL shell, run the following:
         ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '1234';
         CREATE USER IF NOT EXISTS 'root'@'%' IDENTIFIED BY '1234';
         GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;
         FLUSH PRIVILEGES;
         EXIT;

         # Allow Remote Connections
         sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf

         # Change it to: 
         bind-address = 0.0.0.0

         # Restart MySQL to Apply Changes
         sudo systemctl restart mysql

   ##### **35. Shortcut link for MySQL installation (instead of installing step by step use this to install directly)**            

         bash <(curl -sL https://tinyurl.com/mr4brnzj)

   ##### **36. Tomcat Installation Steps**

            #  Switch to Root User
            sudo su -

            # Download Apache Tomcat v9.0.111
            wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.111/bin/apache-tomcat-9.0.111.tar.gz

            # Extract the Archive
            tar -zxvf apache-tomcat-9.0.111.tar.gz

            # Remove the Tar File
            rm -rf apache-tomcat-9.0.111.tar.gz

            # Confirgure Tomcat username admin & password admin
            vi apache-tomcat-9.0.111/conf/tomcat-users.xml

            # Configure Tomcat Remote Access
            vi apache-tomcat-9.0.111/webapps/manager/META-INF/context.xml

            # Start the Tomcat server
            sh apache-tomcat-9.0.111/bin/startup.sh

            # Shutdown the Tomcat server
            sh apache-tomcat-9.0.111/bin/shutdown.sh




