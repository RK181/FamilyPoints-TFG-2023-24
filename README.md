# FamilyPoints (TFG 2023-24)

## Overview

This project is a cross-platform mobile application to manage the exchange of favors/tasks between members of the same family, couple-oriented, (staying one night with the children, cooking for the whole week, etc.), which will be accumulated as points redeemable for activities/rewards (free night with friends, spa, afternoon video games, etc.). <br/><br/>
It is built using Ionic 7 and React for the frontend, and Laravel 10 for the backend. The communication between the frontend and backend is handled through a REST API, documented with the OpenAPI standard.

## Capabilities 

The prototype has the capability to register users, verify them, manage groups, and handle tasks to earn points and rewards to spend. It also includes options to adjust the logic for creating and completing tasks and rewards, depending on the level of trust between the couple.

## Technologies Used

- **Frontend**: Ionic 7, React
- **Backend**: Laravel 10
- **API Documentation**: OpenAPI Standard

  - Url to the API documentation on GitHub Pages: 
    [FamilyPoints Doc.](https://rk181.github.io/FamilyPoints-TFG-2023-24/)

## Getting Started
### Prerequisites

- Node.js
- PHP 8+
- Composer
- Ionic CLI

### Installation

1. **Clone the repository**:
    - Clone main project and all modules:
        ```
        git clone --recurse-submodules https://github.com/RK181/FamilyPoints-TFG-2023-24.git
        ```
    - Clone main project and modules, one by one:
        ```
        git clone https://github.com/RK181/FamilyPoints-TFG-2023-24.git
        cd FamilyPoints-ionic-front
        git submodule init
        git submodule update
        cd ../FamilyPoints-laravel-api
        git submodule init
        git submodule update
        ```
    - Pull main project and submodules:
        ```
        git pull --recurse-submodules
        ```
1. **Prepare frontend**:
    ```
    cd FamilyPoints-ionic-front
    npm install
    ```

3. **Prepare backend**:
    ```
    cd FamilyPoints-laravel-api
    cp .env.example .env
    php artisan key:generate
    php artisan migrate:refresh
    ```

4. **Run the development servers**:
    - **Frontend**:
        ```
        cd FamilyPoints-ionic-front
        ionic serve
        ```
    - **Backend**:
        ```
        cd cd FamilyPoints-laravel-api
        php artisan serve
        ```
