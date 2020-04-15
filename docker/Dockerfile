# Set the base image to Ubuntu
FROM ubuntu

# File Author / Maintainer
MAINTAINER reddy43k@gmail.com

# Install Nginx
# Update the repository
RUN apt-get update

# Install necessary tools
RUN apt-get install -y nano wget dialog net-tools
# Download and Install Nginx
RUN apt-get install -y nginx

# removing index.html
RUN rm -rf /usr/share/nginx/html/index.html

# Copying the index file
COPY index.html /usr/share/nginx/html/

# Append "daemon off;" to the beginning of the configuration
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80

# Set the default command to execute
# when creating a new container
CMD service nginx start
