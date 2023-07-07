# Open Prescribing Scotland

The aim of this project is to create an easy-to-use web interface to prescribing data in Scotland. Under the team 
name of Open Prescribing Scotland (OPS), we are envisioning our project as a Scottish counterpart to the renowned 
https://openprescribing.net/ website - a platform that enables the public and healthcare enthusiasts to explore and 
analyse Scotland's openly available prescribing data.

OPS started out as a hack weekend project. Within the limited time of the weekend, we achieved to develop a prototype web application using the Django web framework and to scope out future requirements for this service.


### Deployment
Currently, a prototype of the web application is deployed on Render. Access via:
https://open-prescribing-scotland.onrender.com/

As of now, the only PoC functionalities implemented are a mapping of NHS health board name and code through live API 
access, as well as visualising the paid quantity of a prescribed drug within a selected NHS health board for the 
months of the year 2022.

### Data 
Relevant datasets and their variables include:

* [Prescribing Data](https://www.opendata.nhs.scot/dataset/prescriptions-in-the-community):
  - HBT 
  - GPPractice
  - BNFItemCode
  - BNFItemDescription
  - PaidDate
  - ClassOfPreparationCode
  - NumberOfPaidItems
  - PaidQuantity
  - GrossIngredientCost
  - PaidDate

* [Glossary of Terms](https://www.isdscotland.org/health-topics/prescribing-and-medicines/_docs/Open_Data_Glossary_of_Terms.pdf?1)

* [Health Boards](https://www.opendata.nhs.scot/dataset/geography-codes-and-labels/resource/652ff726-e676-4a20-abd-435b98dd7bdc):
corresponding name and country code for Scotland
* [GP Practices](https://www.opendata.nhs.scot/dataset/gp-practice-contact-details-and-list-sizes):
contact details and list sizes

## Project Setup

This webpage requires Python3 and uses the webframework Django.

Download python from https://www.python.org/downloads/, or install python from the terminal via:
```shell
sudo apt-get update
sudo apt-get install python3.8
```

Python dependencies are managed via pip. However, it is advised to install those dependencies into a virtual 
environment. This can be created with:
```shell
python3 -m venv venv
```

To activate the environment use:
```shell
source venv/bin/activate
```
This needs to be done in every shell that should use our newly created environment.

We suggest installing the Python dependencies through the `requirements.txt` file:
```shell
pip install -r requirements.txt
```

Once the repository is cloned, the Django Webserver can be started with:
```shell
python manage.py runserver
```


