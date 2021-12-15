<div id="top"></div>


<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="https://raw.githubusercontent.com/othneildrew/Best-README-Template/master/images/logo.png" alt="Logo" width="80" height="80">


<h3 align="center">Programa FullCycle de Aceleração: Edição Docker</h3>


</div>





<!-- ABOUT THE PROJECT -->
## About The Project


### Built With


* [Node](https://nodejs.org/en/)
* [Docker](https://www.docker.com/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started


### Prerequisites

* docker


### STEPS


1. Create a docker network
   ```bash
   docker network create pfa
   ```
2. creater a node js docker image
   ```bash
   docker build -t marcelowis/pfa-node .
   ```
3. creater a nginx docker image
   ```bash
   docker build -t marcelowis/pfa-nginx .
   ```
4. run the container with name nodecontainer
   ```bash
   docker run -d --network=pfa --name=nodecontainer marcelowis/pfa-node
   ```
5. run the container with name nodecontainer
   ```bash
   docker run -d --network=pfa -p 8080:80 marcelowis/pfa-nginx
   ```
<p align="right">(<a href="#top">back to top</a>)</p>
