FROM tomcat:latest

# Remove the default Tomcat applications
RUN rm -rf /usr/local/tomcat/webapps/*

COPY . /src
# Copy your application WAR file to the Tomcat webapps directory
COPY target/secend-app-0.0.1-SNAPSHOT.jar /usr/local/tomcat/webapps/

#////////////////////////////////////////////////////////////////////////
# Set the working directory inside the container
# WORKDIR /app

# # Copy the executable JAR file into the container at /app
# COPY target/demo-0.0.1-SNAPSHOT.jar /app/demo-0.0.1-SNAPSHOT.jar
#////////////////////////////////////////////////////////////////////////


# Expose the port that your application will run on
EXPOSE 7070

# Specify the command to run your application
CMD ["java", "-jar", "/usr/local/tomcat/webapps/secend-app-0.0.1-SNAPSHOT.jar"]