# Azure-Docker-project

Link for deployed webapp on azure Link: prernatest123.azurewebsites.net

# Final Project: Deploying a Dockerized Application on a VM

## Description
This final project involves deploying a Dockerized application on a Virtual Machine (VM) to enhance deployment efficiency and management through containerization. The project covers Docker installation, image pulling, container launching, and networking configuration for application access.

## Steps to Complete the Project

### Week 1: Introduction to Docker and Containerization

1. **Understand Docker and Containers**:
   - I started by learning the basics of Docker and containerization, including the benefits of using containers for application deployment.

### Week 2: Setting Up the VM

1. **Create a Virtual Machine (VM)**:
   - I logged into the Azure portal and navigated to the "Virtual Machines" section.
   - I created a new VM with the desired configuration (e.g., Ubuntu as the operating system, resource group, size).

### Week 3: Installing Docker on the VM

1. **Connect to the VM**:
   - I connected to the VM using SSH:
     ```bash
     ssh azureuser@<VM_IP_Address>
     ```

2. **Install Docker**:
   - I installed Docker on the VM by running the following commands:
     ```bash
     sudo apt-get update
     sudo apt-get install -y docker.io
     sudo systemctl start docker
     sudo systemctl enable docker
     ```

3. **Verify Docker Installation**:
   - I verified the Docker installation by running:
     ```bash
     docker --version
     ```

### Week 4: Pulling Docker Image

1. **Pull Docker Image from Docker Hub**:
   - I pulled the Docker image for my application from Docker Hub using:
     ```bash
     docker pull <image_name>
     ```

### Week 5: Launching Docker Container

1. **Launch the Docker Container**:
   - I launched the Docker container using the pulled image:
     ```bash
     docker run -d --name myapp -p 80:80 <image_name>
     ```

2. **Verify Container Launch**:
   - I verified that the container was running by listing all running containers:
     ```bash
     docker ps
     ```

### Week 6: Networking Configuration

1. **Configure Networking for Application Access**:
   - I ensured that port 80 was open for inbound traffic in the VM's network security group (NSG) settings.

2. **Access the Application**:
   - I accessed the application using the VM's public IP address in a web browser:
     ```bash
     http://<VM_IP_Address>
     ```

### Week 7: Enhancing Deployment Efficiency and Management

1. **Use Docker Compose (Optional)**:
   - For more complex applications, I used Docker Compose to manage multiple containers. I created a `docker-compose.yml` file and deployed the application using:
     ```bash
     docker-compose up -d
     ```

2. **Automate Deployment (Optional)**:
   - I explored automating the deployment process using CI/CD pipelines with tools like GitHub Actions or Azure DevOps.

### Resources Used

- [Docker and Containerization Presentation](https://docs.google.com/presentation/d/15WcgztDbCTEUaVthe9ie731oLUqA1wyk/edit?usp=sharing&ouid=106645495933275419660&rtpof=true&sd=true)

## Conclusion

By following the above steps, I successfully deployed a Dockerized application on a VM, enhancing deployment efficiency and management through containerization. This project provided practical experience in setting up a VM, installing Docker, pulling and running Docker images.
