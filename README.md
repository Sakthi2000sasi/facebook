# install jenkins
#shebank Line
#:bin\bash\

#Download the jenkins Repo

sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
#import the jenkin key
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
# upgrade the os
sudo dnf upgrade
# Add required dependencies for the jenkins package
sudo dnf install fontconfig java-17-openjdk
#install the jenkin
sudo dnf install jenkins
#reload the configuration of the system
sudo systemctl daemon-reload
#star the jenkins
sudo systemctl start jenkins
#check status of the jenkin
sudo systemctl status jenkins
~

