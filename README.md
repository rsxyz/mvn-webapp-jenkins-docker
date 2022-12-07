# mvn-webapp-jenkins-docker

### sshkey-gen --- generate devops.pub and devops.pem file

ssh-keygen -t rsa -b 4096 -m pem -f devops && mv devops devops.pem && chmod 400 devops.pem

### import key pair

aws ec2 import-key-pair --key-name "devops" --public-key-material fileb://./devops.pub
