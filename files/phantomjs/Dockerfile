FROM ubuntu

RUN apt-get update
RUN apt-get install bzip2 wget libfreetype6 libfontconfig1  -y
RUN wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-1.9.7-linux-x86_64.tar.bz2
RUN tar -xvf phantomjs-1.9.7-linux-x86_64.tar.bz2 && rm phantomjs-1.9.7-linux-x86_64.tar.bz2
RUN mv /phantomjs-1.9.7-linux-x86_64 /usr/local/phantomjs-1.9.7-linux-x86_64
RUN ln -s /usr/local/phantomjs-1.9.7-linux-x86_64/bin/phantomjs /usr/local/bin/phantomjs
ADD register-node.sh /var/register-node.sh
RUN chmod 755 /var/register-node.sh
CMD ["/bin/bash", "/var/register-node.sh"]
