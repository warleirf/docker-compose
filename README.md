# docker-compose
Projetos aprendizagem docker


Install Docker on Ubuntu 20.04
There are two options when for installing Docker on your Ubuntu system:

Installing using the official Docker repository
Installing using the default repositories
When you download a package from the default Ubuntu repository, it may not be the latest version. If installing the latest (or a specific) version of Docker is important, use the official repository.

Option 1: Installing Docker from Official Repository
Step 1: Updating the Software Repository
Start by opening a terminal window and updating the local repository:

sudo apt update
Wait for the process to complete.

Step 2: Downloading Dependencies
Allow your Ubuntu 20.04 system to access the Docker repositories over HTTPS by running:

sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
The above-mentioned command:

Gives the package manager permission to transfer files and data over https.
Allows the system to check security certificates.
Installs curl, a a tool for transferring data.
Adds scripts for managing software.
Step 3: Adding Docker’s GPG Key
Next, add the GPG key to ensure the authenticity of the software package:

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
Add the GPG key for Docker.
Step 4: Installing the Docker Repository
Now install the Docker repository using the command:

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu  $(lsb_release -cs)  stable"
The command installs the latest repository for your specific Ubuntu release (in this case, 20.04 Focal Fossa).

Step 5: Installing the Latest Docker
Start by updating the repository again:

sudo apt update
Now you can install the latest Docker version with:

sudo apt-get install docker-ce
Step 6: Verifying Docker Installation
To confirm the installation check the version of Docker:

docker --version
docker version 19.03.8 installed sucessfully
It should show the Docker version, as in the image above.

Step 7: Enable Docker Service 
To start the Docker service run the following commands:

sudo systemctl start docker
Enable Docker to run at startup with:

sudo systemctl enable docker
To check the status of the service, use the command:

sudo systemctl status docker
The output should show Docker is active (running).

example of docker active and running on Ubuntu 20.04
