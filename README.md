# Dapier

Dockerized Zapier Development

## Getting Started

* Fork this project
* Clone your fork
* Login to your zapier account using a docker image with the correct tools installed
```
docker run -it --name=zapier-login wbhumphrey/zapier bash -c "zapier login"
```
* Save the zapier developer token for containers to use later
```
docker cp zapier-login:/root/.zapierrc .
docker rm zapier-login
```
* Bootstrap an app using the example zapier app on github
```
docker-compose build
docker-compose run --rm node bash -c "git clone https://github.com/zapier/zapier-platform-app-github-example.git . && rm -rf .git && rm -rf .gitignore && npm install"
```
* Build your app!

### Prerequisites

A Zapier account (https://zapier.com/)
Docker (https://docs.docker.com/machine/get-started/#prerequisite-information)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Thanks to the folks at Zapier for making a powerful platform for integrations
