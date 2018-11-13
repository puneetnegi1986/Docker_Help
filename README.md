# Docker_Help
Docker Installation on Linux Box Ubuntu 16.04 

(A) Official Ubuntu Repositories
$ sudo apt-get install docker.io
In the past this way was discouraged as the docker package was super outdated. The universe sources are fairly recent now.

(B) Official Docker Way
The Ubuntu installation instructions list all you need in detail, but in most cases it boils down to:

(1) Set up the docker repository

sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

(2) Install Docker CE

sudo apt-get update
sudo apt-get install docker-ce
(3) Verify the installation

sudo docker run hello-world
