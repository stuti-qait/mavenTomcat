# mavenTomcat

Step-1 : Create a Maven Repository

Step-2 : Add Archtype "maven-archtype-webapp"

Step-3 : Give suitable Artifact id, Group id and package name

Step-4 : Add dependencies to pom.xml
    * Add Tomcat Maven Plugin 
    use [1] http://mvnrepository.com/artifact/org.apache.tomcat.maven/tomcat7-maven-plugin
    
    * Add Maven Servlet Library
    use [2] https://mvnrepository.com/artifact/javax.servlet/javax.servlet-api/4.0.1
    
    Your pom.xml file must look like
     <dependencies>
       <dependency>
           <groupId>junit</groupId>
           <artifactId>junit</artifactId>
           <version>3.8.1</version>
           <scope>test</scope>
       </dependency>
 
       <!-- Servlet Library -->
       <dependency>
           <groupId>javax.servlet</groupId>
           <artifactId>javax.servlet-api</artifactId>
           <version>3.1.0</version>
           <scope>provided</scope>
       </dependency>
        
      </dependencies>
    
 
      <build>
       <finalName>SimpleMavenWebApp</finalName>
       <plugins>
        
           <!-- Config: Maven Tomcat Plugin -->
           <!-- http://mvnrepository.com/artifact/org.apache.tomcat.maven/tomcat7-maven-plugin -->
           <plugin>
               <groupId>org.apache.tomcat.maven</groupId>
               <artifactId>tomcat7-maven-plugin</artifactId>
               <version>2.2</version>
               <!-- Config: contextPath and Port (Default - /SimpleMavenWebApp : 8080) -->
               <!--
               <configuration>
                   <path>/</path>
                   <port>8899</port>
               </configuration>
               --> 
           </plugin>
       </plugins>
      </build>
   
Step-5 : Go to Run < Run Configuration < Maven Build (Right click and add new file)

Step-6 : Add base directory(you can browse) and set Goals : *tomcat7:run -X*

Step-7 : Apply and Run

Step-8 : copy the link that shows up on the console. Go to the browser and paste & run.
