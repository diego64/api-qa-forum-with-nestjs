<p align="center">
  <img src="img.shields.io/image/capa.png" width="500" alt="Capa" /></a>
</p>

<p align="center">
	Developed with the software and tools below.
</p>

<p align="center">
    <img src="img.shields.io/badge/nestjs.svg?style=flat&logo=node&logoColor=white" alt="nestjs">
    <img src="img.shields.io/badge/docker.svg?style=flat&logo=docker&logoColor=white" alt="docker">
    <img src="img.shields.io/badge/postgresql.svg?style=flat&logo=postgresql&logoColor=white" alt="postgresql">
    <img src="img.shields.io/badge/jwt.svg?style=flat&logo=jwt&logoColor=white" alt="jwt">
    <br>
    <img src="img.shields.io/badge/passport.svg?style=flat&logo=passport&logoColor=white" alt="passport">
    <img src="img.shields.io/badge/vitest.svg?style=flat&logo=vitest&logoColor=white" alt="vitest">
    <img src="img.shields.io/badge/supertest.svg?style=flat&logo=supertest&logoColor=white" alt="supertest">
    <img src="img.shields.io/badge/cloudflare.svg?style=flat&logo=cloudflare&logoColor=white" alt="cloudflare">
    <img src="img.shields.io/badge/redis.svg?style=flat&logo=redis&logoColor=white" alt="redis">
</p>

## 📝 Overview

This API was developed based on SOLID principles, ensuring a well-structured and easy-to-maintain architecture. Each principle contributes to a modular application, where each layer of code is independent and easy to modify without compromising the overall functioning of the application. Below, we explain how each SOLID principle was applied:

S - Single Responsibility Principle: Each class or module has a single responsibility. This means that when modifying a part of the code, the impact is minimized, facilitating both maintenance and testing. Each component of the API handles a specific task, making the code more understandable and easy to modify.

O - Open/Closed Principle: The API was designed so that classes are open for extension, but closed for modification. This allows new functionality to be added without changing the existing code, promoting scalability and stability of the system as it grows.

L - Liskov Substitution Principle: Subclasses can be used in place of parent classes without changing the expected behavior of the API. This principle ensures that inheritance is used effectively, allowing new types of objects to be handled transparently and without breaking functionality.

I - Interface Segregation Principle: Interfaces were created in such a way that clients are forced to depend only on the functionalities that they actually use. This prevents classes from having to implement methods that do not make sense to them, promoting cleaner and more specialized code.

D - Dependency Inversion Principle: The API was built in such a way that the dependencies of low-level modules are inverted, allowing high-level modules to define the interfaces that low-level modules must implement. This ensures that the application is easily testable and modular, allowing the replacement of components without negative impacts.

Result: The application is well divided into layers, which facilitates the maintenance and evolution of the code. Each module can be changed or replaced independently, without affecting the system as a whole. The code follows practices that allow the addition of new features with minimal risk, promoting robustness and flexibility.

---

## 📦️ Functionality

- [x] Login
- [x] Authentication
- [x] Creating Questions
- [x] Answering Questions
- [x] Sending Images
- [x] Cash System

---

## 🏷️ Getting Started

To run this application on your local machine, you will need to have some essential tools installed and configured correctly. Below are the requirements and steps to ensure that the application runs correctly in your development environment:

**System Requirements**

* **Node.Js**: `version 20.18.0`
* **Docker**: `version 27.3.1`
* **Cloudflare account**

Create an .env file based on the .env.example file to set the environment variables required for the application to run. Be sure to customize the settings as needed for your local environment.

NOTE: You will need to generate a public_key.pem and private_key.pem on your computer and convert them to .txt in order to generate the JWT keys.

---

### 🗃️ Installation

<h4>From <code>source</code></h4>

> 1. Clone the repository:
>
> ```console
> $ git clone https://github.com/diego64/api-qa-forum-with-nestjs
> ```
>
> 2. Change to the project directory:
> ```console
> $ cd api-qa-forum-with-nestjs
> ```
>
> 3. Install the dependencies:
> ```console
> $ npm install
> ```
> 4. Install the database:
> ```console
> $ docker compose up -d
> $ npx prisma migrate dev
> ```
> 5. Start the application:
> ```console
> $ npm run start:dev
> ```
---

### 🧪 Tests

Testing is a key component of this application, ensuring that the code behaves as expected and providing greater confidence and stability. It is divided into two main parts:

**Unit Testing:** Verifying the behavior of the smallest units of the application, such as functions, methods, and isolated components. Unit testing ensures that each individual piece of code works correctly, without external dependencies.

> Run the test suite using the command below:
> ```console
> $ npm run test
> ```

**End-to-End (E2E) Testing:** Test the application in an integrated manner, simulating user interaction with the complete system. E2E testing ensures that workflows, from input to output, work as expected in a real-world scenario, simulating user navigation through the application, testing routes, forms interactions, and API responses, ensuring that the end-user experience is consistent and flawless.

> Run the test suite using the command below:
> ```console
> $ npm run test:e2e
> ```
---