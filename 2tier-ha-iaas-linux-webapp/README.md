# Create Two Tier Highly Available Linux IaaS Environment to run Website

This template creates multiple linux app and db servers in availabily sets to run two tier website.

### Prerequisites
1. Make sure enough core are available in Azure Subscrition to create selected number of instances and size. More detials to count core needed below.
2. New [Resource Group](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview#resource-groups) is recommneded to avoid Resource name conflicts and for easy maintenance.

### Resources being created
1. Two [Availability Sets](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/tutorial-availability-sets), one for each app and db tiers.
2. One [Azure Virtual Network](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview) and one subnet.
3. One [Azure Storage](https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction) Account to configure diagnostic settings for all the VMs.
4. One Public IP Address and one Network Interface for each VM instance.
5. All the resources are created in the same location as Resource Group.
6. VMs are created with [CentOS 6.9 images](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/overview).

#### [Environemt Size](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes) options
1. Small: 
    App- E8s_v3 (8 VCPUs, 64GB RAM), 
    DB- E16-8s_v3 (8 VCPUs, 128GB RAM)          
2.  Medium:
    App- E16-8s_v3 (8 VCPUs, 128GB RAM), 
    DB- E32-16s_v3 (16 VCPUs, 256GB RAM)
3. Large:
    App- E32-16s_v3 (16 VCPUs, 256GB RAM), 
    DB- E64-32s_v3 (32 VCPUs, 432GB RAM)

4. All VMs inlude a [4TB (P50)](https://azure.microsoft.com/en-us/pricing/details/managed-disks/) Data Disk attached (unmounted) to them.


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Faz-templates%2Fmaster%2F2tier-ha-iaas-linux-webapp%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Faz-templates%2Fmaster%2F2tier-ha-iaas-linux-webapp%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/AzureGov.png"/>
</a>
<a href="http://armviz.io/#/?https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Faz-templates%2Fmaster%2F2tier-ha-iaas-linux-webapp%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

Find a lot more sample templates to quick start your projects at [azure-quickstart-templates](https://github.com/Azure/azure-quickstart-templates)
