# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

Using an Azure Virtual Machine to deploy the Article CMS gives full control over the operating system and application environment, but it also comes with more responsibility and higher ongoing costs. With a VM, the application runs on infrastructure that must be managed manually, including operating system updates, Python environment setup, security patches, and web server configuration. Costs continue as long as the VM is running, even during periods of low usage. Scaling the application requires resizing the VM or adding additional VMs with a load balancer, which takes time and planning. Availability is also more limited by default, since a single VM can become a single point of failure unless extra resources such as availability sets or zones are configured. While this approach offers flexibility, it adds complexity that is not strictly necessary for a small CMS application.
Azure App Service provides a simpler and more efficient way to deploy the Article CMS. It offers lower and more predictable costs, especially when using the Free or Basic tiers, while removing the need to manage servers and operating systems. App Service makes it easy to scale the application up or down with minimal configuration, and it includes built-in availability features that help keep the app running even if underlying infrastructure issues occur. The deployment workflow is also much smoother, with native support for GitHub Actions, environment variables, and centralized logging through the Azure Portal. For these reasons, Azure App Service was chosen as the deployment option for this project. It allows the application to be deployed and maintained quickly, reduces operational overhead, and provides sufficient scalability and reliability for the scope of the Article CMS.
