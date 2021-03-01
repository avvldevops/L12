FROM ubuntu:20.04
RUN apt update && apt install git -y && apt install default-jdk -y && RUN apt-get install maven -y
WORKDIR /home/git/
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR /home/git/App42PaaS-Java-MySQL-Sample/
RUN echo "app42.paas.db.username = paasdb_user" > WebContent/Config.properties &&/
echo "app42.paas.db.port = 3306" >> WebContent/Config.properties &&/
echo "app42.paas.db.password = P@ssw0rd" >> WebContent/Config.properties &&/
echo "app42.paas.db.ip = db" >> WebContent/Config.properties &&/
echo "app42.paas.db.name = database1" >> WebContent/Config.properties
RUN mvn package