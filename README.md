# Cyber Blog Cloud Application (NEED TO ADD SCREENSHOTS)

## Objective

The objective of this project is to build and secure a cloud-hosted web application using Azure’s cloud infrastructure and security tools. By deploying a custom application, managing containers, and configuring security protocols like SSL certificates and Azure Web Application Firewall (WAF), this project provides practical experience in cloud development and cybersecurity. The project highlights my ability to design secure, scalable web applications while leveraging automation tools and cloud-based services, with a focus on real-world web security challenges and solutions.

### Skills Learned

- Cloud Deployment: Setting up and managing web apps on Azure.
- Docker: Using Docker containers for web app deployment.
- Web Customization: Editing HTML to personalize web content.
- SSL/TLS Management: Creating and managing SSL certificates.
- Cryptography: Using OpenSSL for secure communications.
- Web Application Firewall (WAF): Configuring WAF to block common attacks (SQL injection, XSS).
- Azure Security Center: Monitoring and improving app security.
- Linux Administration: Using SSH and managing files in a Linux environment.

### Tools Used

- Microsoft Azure: For web app deployment, domain management, and cloud infrastructure.
- Azure Cloud Shell: For managing and deploying Docker containers, running OpenSSL commands.
- Docker: For containerizing and deploying the web application.
- OpenSSL: For generating SSL/TLS certificates.
- Azure Key Vault: For storing and managing certificates and secrets.
- Azure Web Application Firewall (WAF): For protecting the web application against common vulnerabilities.
- Azure Security Center: For monitoring app security and providing security recommendations.
- Linux (via SSH): For accessing and managing files within Docker containers.


## Steps

In this project, I designed and deployed a custom web application using Azure’s free domain service. My first task was to create an Azure web app, which involved naming the application, selecting the necessary backend technologies, and setting up a Linux-based service plan with PHP 8.2. Once the app was created, I was assigned a unique domain and IP address, making the app accessible on the web. From there, I deployed a Docker container using a Azure’s Cloud Shell. The container, which hosted the framework for a cybersecurity blog page, was pulled from Docker Hub and configured with the appropriate settings. After deploying the container, I customized the web app with my personal details. This included updating the HTML to display my name, email, LinkedIn profile, a personal introduction, and two blog posts on cybersecurity topics.

In the next phase of the project, I focused on securing my web application using SSL certificates through Azure’s services. The first step was to create an Azure Key Vault, a secure environment for storing sensitive information such as keys, secrets, and certificates. I configured the vault with the same resource group and region I used before. I then generated a self-signed certificate using OpenSSL within the Azure Cloud Shell. I then exported this certificate into a PFX format, which combines the certificate and private key into one file, and uploaded it to my Azure Key Vault for storage and analysis.

To understand the implications of using self-signed certificates, I compared this certificate with a trusted SSL certificate. First, I accessed a site with a self-signed certificate and analyzed the warning message indicating it was not secure. Then, I examined the trusted SSL certificate provided by Azure for my web application. This allowed me to see the security benefits of using a trusted certificate from a reputable CA versus a self-signed one.

The last phase of the project involved configuring and securing my web application using Azure's Web Application Firewall (WAF) and Azure Security Center. My main focus was on protecting the application by analyzing WAF rule sets and setting up custom rules to ensure only trusted traffic can access the web app. I started by creating the WAF in Azure, a critical layer of protection designed to block various web vulnerabilities. Once it was set up, I examined the managed rules, which protect against common application attacks like SQL injections and cross-site scripting (XSS). These rules were flexible, allowing me to block, log, or redirect suspicious requests as needed. Next, I configured a custom WAF rule tailored to our scenario, where we assumed the web app had been experiencing attacks from international threats. I restricted traffic to only allow access from the United States, Canada, and Australia, blocking all other regions. This custom rule helps mitigate threats from outside trusted regions and ensured that associated partners could still access the application.

After completing the technical tasks, I answered the project review questions to document my understanding.

<a href="https://github.com/ThatBrownGuy101/Cyber-Blog-Cloud-Application/blob/main/Cyber%20Blog%20Cloud%20Application%20Technical%20Brief.docx">Cyber Blog Cloud Application Technical Brief</a>

This project has deepened my expertise in web application security, WAF configuration, and cloud security management—skills that will be valuable in future discussions with potential employers.
