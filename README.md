# infra_rubyserver
Initial scripts for ruby_mongodb_server

# gloud command
gcloud compute instances create --boot-disk-size=10GB --image=ubuntu-1604-xenial-v20170815a --image-project=ubuntu-os-cloud --machine-type=g1-small --tags puma-server --restart-on-failure --zone=europe-west1-b reddit-app --metadata startup-script='#!/bin/bash
su IvanSSHKey
git clone https://github.com/ger4ivan/infra_rubyserver.git
cd infra_rubyserver
chmod +x install_ruby_mongodb.sh
./install_ruby_mongodb.sh'


