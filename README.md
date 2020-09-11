<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h3 align="center">Full Stack Task Manager</h3>

  <p align="center">
    A full stack task managing application built with React, TypeScript, Nest.JS, and PostgresSQL. 
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)



<!-- ABOUT THE PROJECT -->
## About The Project

![TaskManagerScreenShot][product-screenshot]


### Built With

* [React](https://reactjs.org/)
* [TypeScript](https://www.typescriptlang.org/)
* [Nest.JS](https://nestjs.com/)
* [PostgresSQL](https://www.postgresql.org/)


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm or yarn
```sh
npm install npm@latest -g
```
* PostgresSQL 12
* PgAdmin 4

**** please make sure PgAdmin4 and PostgresSQL is runnig **** 

### Installation

In the near future, I will convert this project into a docker project so that it can be run in one environment. However, until then, please follow the following steps. 

1. Clone the repo for the API and CD into new directory
```sh
git clone https://github.com/wlee367/nest-js-task-management-api
cd nest-js-task-management-api
```
1a. Adjust /config/default.yml
```yaml
server:
  port: ${your_desired_port_here} // will be set as 3001

db:
  type: 'postgres'
  port: 5432 // change to port your postgres installation is running
  database: 'taskmanagement' // name of the database. when app starts up, it will create a database with this name if it doesn't exist. 

jwt:
  expiresIn: 3600000000000

```
2. Install NPM packages
```sh
yarn install
```
3. Run project in development mode
```sh
yarn start:dev
```
4. In a new terminal window, clone the repo for the webapp, and cd into new directory.
```sh
git clone https://github.com/wlee367/nestjs-task-management-webapp
cd nestjs-task-management-webapp
```
4a. IF you changed the port number in step 1a, you will want to adjust /src/app/redux/httpService.js and adjust the `BASE_URL` variable to match your port.
```js
  BASE_URL = "http://localhost:{YOUR_PORT_NUMBER}"; 
```
5. Install NPM packages
```sh
yarn install
```
6. Run project
```sh
yarn start
```
7. Visit http://localhost:3000 to see the project connected. 


<!-- USAGE EXAMPLES -->
## Usage
In this project, you can sign up as a user by going to localhost:3000/register. 

![Register][register-screenshot]

Your password must contain one capital letter, at least one special character, and be a minimum of 8 characters long. Otherwise, you will get this error:

![RegisterError][register-error]

Once you register / login, you will be redirected to the main screen like this: 

![Main Screen][main-screen]

To create a new task, simply click on the plus icon in the bottom right, then you'll be greeted with a modal like this: 

![CreateModal][create-modal]

Once you create a task, you will be able to drag and drop it to a different column to indicate a new status, or leave a comment like this:

![comment][comment]

![comment-todo][comment-todo]

If you click on user activity - you will be able to see a history of all actions you have taken. 


<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/wlee367/TaskManager/issues) for a list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- CONTACT -->
## Contact

Jason Lee - [email](mailto:proto.rhee@gmail.com)

Project Link: [https://github.com/wlee367/repo_name](https://github.com/wlee367/TaskManager)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=flat-square
[contributors-url]: https://github.com/wlee367/TaskManager/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=flat-square
[forks-url]: https://github.com/wlee367/TaskManager/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=flat-square
[stars-url]: https://github.com/wlee367/TaskManager/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=flat-square
[issues-url]: https://github.com/wlee367/TaskManager/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/wlee367/TaskManager/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/wlee367
[product-screenshot]: images/demo.gif
[register-screenshot]: images/Reigster.png
[register-error]: images/Error.png
[main-screen]: images/MainScreen.png
[create-modal]: images/New%20Task%20Modal.png
[comment]: images/comment.png
[comment-todo]: images/commentTodo.png
