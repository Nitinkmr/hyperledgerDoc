# HyperLedgerDoc
Installation instructions for hyperledger composer and for deploying a .BNA file

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

Things you need to install and how to install them

```
Operating System: Ubuntu Linux 14.04 / 16.04 LTS (both 64-bit) (or a VM with same configuration)
Docker Engine: Version 17.03 or higher
Docker-Compose: Version 1.8 or higher
Node: 6.x (note version 7 is not supported)
npm: 3.10.x
git: 2.9.x
```

### Installing hyperledger composer

A step by step series of commands that tell you have to get a development env running

Download all the prerequisites using the following command
```
curl -O https://raw.githubusercontent.com/hyperledger/composer-sample-applications/master/packages/getting-started/scripts/prereqs-ubuntu.sh

chmod u+x prereqs-ubuntu.sh
```
once downloaded, just run the below script
```
./prereqs-ubuntu.sh
```
# Now download the development tools:

```
npm install -g composer-cli
npm install -g generator-hyperledger-composer
npm install -g composer-rest-server
npm install -g yo
```
# Starting Hyperledger Fabric:

```
docker kill $(docker ps -q)
docker rm $(docker ps -aq)
docker rmi $(docker images dev-* -q)
```
In a directory of your choice,(In a directory of your choice (will assume ~/fabric-tools) get the zip file that contains the tools)

```
mkdir ~/fabric-tools && cd ~/fabric-tools

curl -O https://raw.githubusercontent.com/hyperledger/composer-tools/master/packages/fabric-dev-servers/fabric-dev-servers.zip
unzip fabric-dev-servers.zip

```
export the fabric version (we are using V1)

```
export FABRIC_VERSION=hlfv1
```

Now are fabric resides in ~/fabric-tools
To start hyperledger composer issue following commands:

```
cd ~/fabric-tools
./downloadFabric.sh
./startFabric.sh
./createComposerProfile.sh
```

And to stop hyperledger composer issue following commans:
```
cd ~/fabric-tools
./stopFabric.sh
./teardownFabric.sh
```


```
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
