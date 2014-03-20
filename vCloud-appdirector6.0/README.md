Initial configuration
==============
- Follow the vFabric App Director instructions for creating a Windows Server 2008 R2 Enterprise SP1 virtual machine containing the AppDirector agent. 
- Before converting this virtual machine into a VM template, install the CloudVolumes Agent into this virtual machine.
- Add this VM template in the "Cloud Template Mapping" in the "Windows Server 2008 R2 Enterprise SP1 VM" logical template.

Provision a new application
==============
- To create a new AppStack use the "CloudVolumes Provisioner" application.
- In the blueprint, set the VOLUME property to the name of the AppStack you want to create.
- Drag-and-drop the service you want to install into the provisioner VM
- Create a dependency between the CloudVolumes_Provisioner_Service and service you want to install to make sure CloudVolumes_Provisioner_Service will run first

To deploy a new application
==============
- Use the existing "CloudVolumes Clustered Wordpress" as a model for multi-tier applications leveraging CloudVolumes
