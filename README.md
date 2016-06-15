# Docker Jenkins Extended
This Dockerfile is based on officed jenkins docker image on dockerhub. I've extend to support ansible....
Software installed:
OpenVPN, Tmux, Ansible....

#Requirements
DockerEngine 1.11
#How to build image from Dockerfile

<code>git clone https://github.com/thuannvn/Docker-Jenkins-Extend.git</code>

<code>cd Docker-Jenkins-Extend</code>

<code>docker build -t="thuannvn/my-jenkins" .</code>

# Start your jenkins
<code>docker run -p 8080:8080 -p 50000:50000 -v /opt/jenkins:/var/jenkins_home thuanvn/my-jenkins</code>

Then access jenkins http://ip-host:8088
#FAQ
Error when su root: 'su : must be run from a terminal'

Solved:

<code>echo "import pty; pty.spawn('/bin/bash')" > /tmp/asdf.py</code>
<code>python /tmp/asdf.py</code>
