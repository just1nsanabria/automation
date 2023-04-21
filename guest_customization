#!/bin/bash

# Update package list
sudo apt-get update

# Upgrade installed packages
sudo apt-get upgrade -y

# Add a new user 'otcadmin' with the password 't3mPp@$$!!'
sudo adduser --gecos "" otcadmin
echo "otcadmin:t3mPp@$$!!" | sudo chpasswd

# Add user to sudo group
sudo usermod -aG sudo otcadmin

# Install kubectl
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
