
# Eco Trash Project

### Authors: Rafał Mironko, Tomasz Smoleń, Martyna Orzechowska, Marcin Polewski, Katia Anikevich

---

## Project Setup
```sh
npm install
```

### Development Mode (used during development)
```sh
npm run serve
```

### Build (to be deployed on the server)
```sh
npm run build
```

## Documentation

### Frontend

#### Introduction
The frontend of our application is fully implemented using the Vue.js framework. The site is optimized as an interface for our REST API, allowing for efficient communication with the server. The site is responsive, adapting to both computer monitor and phone screen sizes.

#### Project Structure
The project is divided into views, which represent logically separated subpages. Access to individual views is achieved through the link tree provided by Vue Router.

Each component (view) consists of three main parts:
- HTML: Defines the structure and layout of elements on the page.
- JavaScript (Vue.js): Handles the component logic, data interaction, and dynamic interface updates.
- SCSS (cascading style sheets): Contains styles that define the appearance and layout of the component.

#### File Structure
The main folder containing the frontend is /src. It includes key elements such as:
- Assets: Resources such as images, icons, etc.
- Components: Vue.js modules representing individual parts of the page.
- Fonts: Folder containing the fonts used.
- Styles: Style sheets in SCSS format.
- Vue Router: Link tree structure for navigation between components.

#### Vue.js Version
The frontend is built using Vue.js version 3.3.12. Using the latest version of the framework allows us to leverage the newest features.

#### Project Expansion
The entire project is designed for easy future expansion. The modular project structure and the use of Vue.js as a reactive framework facilitate the addition of new features and components.

### Backend

#### Launch
```sh
cd trashAPI
python manage.py runserver
```

#### Introduction
The backend is implemented using the Django REST framework. It enables communication between the database, the microcontroller, and the website, providing data in JSON format.

#### File Structure
The main files in the project are:
- `models.py`: Contains classes corresponding to database tables.
- `serializers.py`: Contains data serializers from the models.
- `views.py`: Uses models and serializers to handle API requests and logic.

#### Functionality
The backend, in addition to its basic functionality, also allows sending emails to users after each trash disposal. It also adds current dates to the tables in the database to minimize the tasks the microcontroller has to perform. It can be interacted with through standard Python requests and also by browsing data by entering {site url}:8001 in a browser.

### HTTP Server on Linux Mint with Nginx (Vue) and Daphne (Django)

#### Project Description
The project involves implementing an HTTP server on a Linux Mint system, with two main parts: a frontend served by Nginx with the Vue framework, and a backend served by Daphne with the Django framework.

#### Project Components
1. **Frontend (Nginx + Vue)**
    - Nginx: A popular HTTP server acting as a reverse proxy, installed on a Linux Mint system. Configured as an interface between external HTTP requests and the Vue server.
    - Vue: A JavaScript framework for building user interfaces, operating on port 8001.

2. **Backend (Daphne + Django)**
    - Daphne: An HTTP server for Django applications, running on a socket port and handling asynchronous requests.
    - Django: A web framework based on Python, handling requests from Daphne.

#### HTTP Implementation on Linux Mint
1. **Nginx (Vue)**
    - Installing Nginx on Linux Mint: Nginx is installed using a package manager. The configuration includes handling traffic on port 8001 and forwarding it to the Vue application.

2. **Daphne (Django)**
    - Installing Daphne on Linux Mint: Daphne is installed as an HTTP server for handling Django applications.
    - Configuring Daphne: Daphne is configured to handle the Django application, and Nginx is set up as a reverse proxy, forwarding requests to the socket port handled by Daphne.

#### Project Structure
The project structure is organized to facilitate easy management and maintenance of both the frontend and backend. Each part (Vue and Django) is separated, making it easier to develop and scale the project.

#### Monitoring and Testing
After configuring HTTP, regular monitoring of both parts of the project is necessary. Testing should include both the frontend and backend to ensure that both functions are available and operating as expected.
