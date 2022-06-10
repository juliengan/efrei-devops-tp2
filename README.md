# Docker : wrapper en go qui récupère les données CurrentWeatherData de OpenWeatherMap (OWM)

Utilisation de Alpine 

docker login –u username # login

### Build image in docker hub
#### Retrieve docker image
https://hub.docker.com/repository/docker/juliengan/efrei-devops-tp2


docker build . -t efrei-devops-tp2:0.0.1

docker tag efrei-devops-tp2:0.0.1 juliengan/efrei-devops-tp2:0.0.1 # I tag it

docker push juliengan/efrei-devops-tp2:0.0.1 # I publish my image to dockerhub

### Run the code

docker run -it efrei-devops-tp2:0.0.1 go run main.go 

docker run --env API_KEY="62bd02468799bb9568074245d9b8631e" efrei-devops-tp2:0.0.1 #API returning the weather using the image with location as input



curl "http://localhost:8081/?lat=5.902785&lon=102.754175"
