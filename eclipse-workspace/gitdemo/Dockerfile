FROM tomcat:10.1-jdk17-corretto

# Set the working directory inside the container
WORKDIR /usr/local/tomcat

# Remove the default webapps to avoid conflicts
RUN rm -rf webapps/*

# Copy the WAR file to Tomcat's webapps directory
COPY target/yourapp.war /usr/local/tomcat/webapps/ROOT.war

# Print out the contents of the webapps directory to confirm WAR deployment
RUN ls -la /usr/local/tomcat/webapps/

# Expose port 8080
EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]

