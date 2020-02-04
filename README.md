# docker-mqtt-server
 deployment of mosquitto mqtt in docker

 Commands ::

 $ docker run -ti --name=mqtt --restart=always --net=host -v /storage/mosquitto/config:/mosquitto/config:ro -v /storage/mosquitto/data:/mosquitto/data -v /storage/mosquitto/log:/mosquitto/log aneh2killa/dtranexia

$ sudo ufw allow 1883

$ docker restart mqtt

Or other options are

$ snap install mosquitto

$ sudo systemctl status mosquitto

Test the configuration

$ mosquitto_sub -h <brokerhost> -t "test"

$ sudo nano /var/snap/mosquitto/common/mosquitto.conf

add the following
—————————————————————
listener 1883 domain_name

more elegant setup is

$ su - username

$ git clone docker-mqtt-server

$ docker-compose -up