IoTFeb2019

Descriptif du projet 
Nous allons réaliser une station météo avec les caractéristiques suivantes :

Heure et Date

Prévision Météo
  5 icones météo
  prévisons à 4 jours
  
Infotmation intérieur
  température en °C
  résolution O,1°C
  humidité en %
    relevé toutes les n secondes
  
Température extérieur  
  température en °C
  résolution O,1°C
  humidité en %
    relevé toutes les n secondes
    
 
 Transmission Wifi
 
 
 
 
 
 
Technologies utilisées
 
Dans le cadre du projet, nous utilisons deux cartes Nodemcu v3. Une va être placée à l'intérieur, l'autre à l'extérieur.
Les deux cartes sont équipées de deux capteurs : un capteur de température et un capteur d'humidité.
 
Nous connectons les deux cartes en Wifi. Nous avons choisi de ne pas utiliser la technologie Sigfox car nous n'avons pas besoin de communiquer à grande distance. 

 
Nous utilisons la technologie MQTT

Nous avons utilisé le capteur DHT11 afin de relever les températures extérieures. Le capteur DHT11 est capable de mesurer des températures de 0 à +50°C avec une précision de +/- 2°C et des taux d'humidité relative de 20 à 80% avec une précision de +/- 5%. Une mesure peut être réalisée toutes les secondes. Il faudra cependant faire attention car le DHT11 ne peut pas mesurer (et supporter) des températures négatives ou des températures supérieures à 50°C. 



image






Les topics sont les suivants
* home/inside/temperature
* home/inside/humidity
* home/outside/temperature
* home/outside/humidity
* apiweather/



Choix du niveau de service


Serveur MQTT : mosquitto
