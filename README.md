# sunbird-rc-keycloak
Sunbird Variant of Keycloak

### How to build from source
* Run the following commands
```bash 
cd keycloak-mobile-number-login-spi
./mvnw clean install
mkdir -p ../keycloak/providers && cp target/keycloak-mobile-number-login-spi-1.0-SNAPSHOT.jar ../keycloak/providers
```
* This will build the Sunbird Keycloak plugin.
* Once this is done, we will need to create the docker image and publish to our Docker repository
```bash
cd ../keycloak
docker build -t <docker_image_path>:<docker_tag> .
docker push <docker_image_path>:<docker_tag> 
```

