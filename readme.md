# Azure Machine Learning initial setup
Here are some instructions on how to quickly get started with Azure Machine Learning.

## Pre-requisites
* Have access to an Azure Subscription
* Have access to a modern web browser (Edge, Chrome, Firefox etc.)

## Extra Reading/Resources
You may wish to learn more about the basics of Azure and Azure Machine Learning after setting up this lab. If so here are some resources I recommend below
* I would recommend getting a basic understanding of cloud technologies and Azure (storage, VMs and networking) from [Azure Fundamentals](https://docs.microsoft.com/learn/paths/azure-fundamentals/?WT.mc_id=aiml-0000-amynic) 
* (Data Science) [Using Python and Azure Notebooks](https://docs.microsoft.com/learn/paths/intro-to-ml-with-python/?WT.mc_id=aiml-0000-amynic)
    * (Bespoke Machine Learning) [Introduction to Azure Machine Learning](https://docs.microsoft.com/learn/paths/build-ai-solutions-with-azure-ml-service/?WT.mc_id=aiml-0000-amynic)
* **General other interesting learning:**
    * (Theory/approaches) [Machine Learning Crash Course](https://docs.microsoft.com/learn/paths/ml-crash-course/?WT.mc_id=aiml-0000-amynic)
    * [Principles for Responsible AI](https://docs.microsoft.com/learn/modules/responsible-ai-principles/?WT.mc_id=aiml-0000-amynic)

## Steps to get Setup
1. Create an Azure Machine Learning Instance
2. Access the Azure Machine Learning studio
3. Create a Notebook VM
4. Create a Training Cluster of Compute
5. Clone Sample .ipynb files
6. Access a Jupyter VM, Browse and Run Files

## Create an Azure Machine Learning Instance

You will create an Azure Machine Learning workspace in the cloud - so you can access remote compute, store large datasets and run your notebooks remotely

* Go to [https://azure.microsoft.com/?WT.mc_id=aiml-0000-amynic](https://azure.microsoft.com/?WT.mc_id=aiml-0000-amynic)
* Sign into your account in the top right
* You will land on the Azure Portal homepage
![Azure Homepage](/img/azure-home.PNG)

* In the top left corner click create a resource
![Create an Azure Resource](/img/create-a-resource.PNG)

* In the search box type 'Machine Learning'
* You will find the Azure Machine Learning service, click create
![Azure Machine Learning service creation](/img/machine-learning-service.PNG)

* Complete information about the Azure Machine Learning workspace
    * **Workspace Name:** 'oxford+yourinitials' (all lowercase, no punctuation)
    * **Subscription:** Choose your student subscription (do not select any subscription that says disabled)
    * **Resource Group:** Click 'Create new' and choose the same name as the workspace
    ![Create new resource group](/img/create-resource-group.PNG)
    * **Location:** West Europe is recommended (however choose any local datacenter)
    * **Workspace edition:** Choose basic for just compute and Notebook VM's, if you wish to use Automated ML choose Enterprise  
    * Click **'Review + Create'**
    ![Create ML Workspace details](/img/create-ml-workspace.PNG)

Once you see green ticks by all fields, click 'Create'
Azure will now deploy all necessary resources for Azure Machine Learning - you can review the resources being created during deployment
![Deployment in Progress](/img/deployment-underway.PNG)

## Access the Azure Machine Learning studio
Once your deployment has finished choose the 'Go to Resource' button. This will take you to the Azure Machine Learning resource page in the Azure portal. This will tell you all the infrastructure details you need about your workspace.

Now access the Azure Machine Learning studio where you can start applying and running machine learning notebooks. Select the 'Launch Now' button
![Launch Azure Machine Learning Studio](/img/launch-now.PNG)

You will land on the Azure Machine Learning studio homepage
![AML Studio homepage](/img/aml-studio.PNG)

## Create a Notebook VM
* Click on the 'Compute' tab on the left
* Select Notebook VMs
* Click New
![New notebook vm](/img/new-notebookvm.PNG)
* Enter a notebook vm name - e.g. yourinitials+vm (all lowercase, no punctuality)
* keep the standard VM type provided
* Click Create
![Create Notebook VM](/img/create-notebook-vm.PNG)

Wait until your VM is created and all links are available
![Notebook VM creating](/img/notebook-vm-creating.PNG)

## Create a Training Cluster of Compute
In order to run the notebook VM sample files on remote compute you need to setup a remote training cluster
* Click on the 'Compute' tab on the left
* Select Training Cluster
* Click New
![new training cluster](/img/new-training-cluster.PNG)
    * Compute Name: cpucompute
    * Region: already selected
    * Virtual Machine Size: Standard_DS3_v2
    * Virtual Machine priority: Low Priority
    * Minimum number of nodes: 0
    * Maximum number of nodes: 5
    * Idle seconds before scale down: 120
    * Click 'Create'
    ![Training Cluster settings](/img/training-cluster-setup.PNG)

## Clone Sample .ipynb files
Once your notebook is created we need to clone some sample notebook files you can learn from and run

* Go to the Notebooks Tab on the left
* Under Azure ML gallery
    * Open Samples
    * Open Python
    * Open 1.0.83 version
    * Open how-to-use-azureml
    * Select the 3 dots on the right
    * Select Clone
    ![Clone samples into Notebook VM](/img/clone-samples.PNG)

The sample files from this github repository are now all available in your notebook virtual machine: [https://github.com/Azure/MachineLearningNotebooks](https://github.com/Azure/MachineLearningNotebooks)

## Access a Jupyter VM, Browse and Run Files
In the compute, notebook VM tab select the 'Jupyter' link on your notebook VM
Jupyter Notebooks will open in a new browser tab
Browse the Notebooks folder:
    * how-to-use-azureml (try anything within this folder)
    * Notebooks I ran during the session
        * how-to-use-azureml/automated-machine-learning/classification-bank-marketing-all-features/auto-ml-classification-bank-marketing-all-features.ipynb
        * how-to-use-azureml/explain-model/azure-integration/scoring-time/train-explain-model-locally-and-deploy.ipynb


