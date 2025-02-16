# Containerization

Containerization is a method of virtualization that allows you to package an application and its dependencies into a container. This container runs across different environments, making sure that the application behaves the same, no matter where it’s deployed (developer’s machine, testing environment, production, etc.).

Docker is a platform and tool for developing, shipping, and running applications inside containers. Docker simplifies the deployment of applications by allowing you to package them along with everything they need to run into a single container.

A Docker image is a blueprint for creating containers. It contains the application, libraries, and environment necessary for the application to run. Images are immutable and read-only. When you run an image, a container is created. Images can be pulled from repositories like Docker Hub.

A container is a lightweight, isolated instance of an image. It is created from a Docker image and runs the application.Containers are isolated from each other but can interact through defined network ports or shared volumes.

Docker Hub** is an online repository where Docker images can be stored, shared, and downloaded. It contains both official images and community made images.

Benefits of Docker and Containerization

- Portability: Containers encapsulate the application and its dependencies, making it easy to run the same container across different environments (development, testing, production).

- Scalability: Docker containers can be orchestrated using tools like Kubernetes to scale applications dynamically based on demand.

- Efficiency: Containers are lightweight compared to virtual machines because they share the host OS kernel, making them faster to deploy and more resource-efficient.

Basic Docker Commands

To pinstall docker to get started you need to add dockers repository.

repository https://download.docker.com/linux/centos/docker-ce.repo
```bash
sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
Then install docker itself.
```bash
sudo dnf install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
Then you need to start and enable docker
```bash
sudo systemctl start docker
sudo systemctl enable docker
```
To verify docker is working use this
```bash
docker run hello-world
```

[Home Page](index.md)