# Introduction to Azure Machine Learning Workbench
This file contains text you can copy and paste for the examples in Cloud Academy's _Introduction to Azure Machine Learning Workbench_ course.  

### Introduction
[Azure Free Trial](https://azure.microsoft.com/free) 

### Installation
[Install Azure Machine Learning Workbench on Windows](https://docs.microsoft.com/en-us/azure/machine-learning/preview/quickstart-installation#install-azure-machine-learning-workbench-on-windows)  
[Install Azure Machine Learning Workbench on macOS](https://docs.microsoft.com/en-us/azure/machine-learning/preview/quickstart-installation#install-azure-machine-learning-workbench-on-macos)  

### Basic Data Preparation
Rename columns to: Sepal Length, Sepal Width, Petal Length, Petal Width, Species  

### Deploying a Model
[Docker Installation](https://docs.docker.com/engine/installation/#desktop)  
[Docker Toolbox Installation](https://docs.docker.com/toolbox/overview)  
```
az ml env setup -n local --location westcentralus
az ml env show -g localrg -n local
az ml account modelmanagement set -n ModelMgmt -g ml-resources
az ml env set -n local -g localrg
az ml env show
export AML_MODEL_DC_STORAGE="<connection string>"
az ml env show -v
az ml service create realtime -f score_iris.py --model-file model.pkl -s service_schema.json -n irisapp -r python --collect-model-data true
az ml service usage realtime -i irisapp
az ml service keys realtime -i irisapp
```

### Advanced Data Preparation
[Boston Hubway dataset](https://s3.amazonaws.com/hubway-data/index.html)  
[Boston weather data](https://azuremluxcdnprod001.blob.core.windows.net/docs/azureml/bikeshare/BostonWeather.csv) from [NOAA](http://www.noaa.gov)  

### Conclusion
[Azure Machine Learning Workbench documentation](https://docs.microsoft.com/azure/machine-learning)  
support@cloudacademy.com
