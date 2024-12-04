# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*


##### COST
- VM: Costs can vary significantly based on the VM size, storage, and network usage. You pay for the compute resources you provision, even if they are not fully utilized. This can be cost-effective for resource-intensive applications but may lead to higher costs for smaller or less active apps
- App Service: Generally more cost-effective for smaller applications or those with variable traffic. You pay for the tier you choose (Basic, Standard, Premium), which includes a set amount of resources and features. Scaling is easier and can be automated, potentially reducing costs during low-traffic periods

##### SCALABILITY
- VM: Scaling VMs is a manual process although you can write an automation script for it. Overall, You have full control over the scaling process but that makes it more complex as well.
- App Service: They are designed for easy scalability. You can scale with just a few clicks or automatically. 

##### AVAILABILITY
- VM: High availability can be achieved having multiple VMs that are grouped, but this requires careful planning and configuration. You are responsible for managing the infrastructure to ensure uptime.
- App Service: Built-in high availability with automatic failover and load balancing. Microsoft manages the infrastructure, ensuring that the app remains available with minimal downtime

##### WORKFLOW
- VM: Offers full control over the operating system and environment, which is a good fit for app that requires specific configurations or legacy software. This also means taking care of patching, updates, and security.
- App Service: Very simplified deployment process. You can focus on the code while Azure handles the infrastructure.


I choose Azure App Service instead of a VM because I prefer focusing on the application code rather than managing infrastructure. The Azure Cloud environment provides pipelines that make it easy to deploy changes from the repository directly into the live application. Additionally, App Service is more cost-effective than VMs and offers easy scalability, allowing me to upgrade the tier as needed.

### Assess app changes that would change your decision.

Very likely I would only move from App Service to VM only if I require access to the VM, mostly to install dependencies that are not part of a pip package
