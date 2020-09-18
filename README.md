**How to Execute this project**
 
 Step 1:   
 Install pipenv  
 `pip install pipenv` 
 
 Step 2:  
 Goto the root directory of the project and start a shell  
 `pipenv shell`
 
 Step 3:  
 Install all the required packages  
 `pipenv install`  
 
 Step 4:  
 Create the tables in the database  
 Goto garbageCollectionProject and execute  
 `python manage.py makemigrations`  
 `python manage.py migrate`  
 
 Step 5:
 Start the server  
 python manage.py runserver  
 
 
 **Descriptions of the End Points**  

* `127.0.0.1:8000/refuse/burough=<burough>&communitydistrict=<community district>&month=2020 / 01/`  
Tons of refuse were collected during the month in a given burough and community district during. If the parameter month is not provided then data is fetched for `2015 / 01`  
 
| Params | Legal values | optional | format |  
| ------------- | ------------- | -------------|  -------------|
| borough  | `Brooklyn`, `Manhattan`, `Bronx`, `Queens`, `Statenisland`  | NO | borough=Manhattan |  
| communitydistrict  | 01-18 | NO | communitydistrict=01 |
| month  | 2020 / 01 | YES  (`default= 2015 / 01`) | month= YYYY / MM|  

 
*`127.0.0.1:8000/paper/burough=<burough>&communitydistrict=<community district>&month=2020 / 01/`  
Tons of paper were collected during the month in a given burough and community district during January 2015 (2015/01)  
 
| Params | Legal values | optional | format |  
| ------------- | ------------- | -------------|  -------------|
| borough  | `Brooklyn`, `Manhattan`, `Bronx`, `Queens`, `Statenisland`  | NO | borough=Manhattan |  
| communitydistrict  | 01-18 | NO | communitydistrict=01 |
| month  | 2020 / 01 | YES  (`default= 2015 / 01`) | month= YYYY / MM|  
 
 
* `127.0.0.1:8000/mgp/burough=<burough>&communitydistrict=<community district>&month=2020 / 01/`  
Tons of metal, glass, and plastic (MGP) were collected during the month in a given burough and community district during January 2015 (2015/01)
 
| Params | Legal values | optional | format |  
| ------------- | ------------- | -------------|  -------------|
| borough  | `Brooklyn`, `Manhattan`, `Bronx`, `Queens`, `Statenisland`  | NO | borough=Manhattan |  
| communitydistrict  | 01-18 | NO | communitydistrict=01 |
| month  | 2020 / 01 | YES  (`default= 2015 / 01`) | month= YYYY / MM|  
  
 
*`127.0.0.1:8000/total/`  
Total amount garbage, refuse + paper + MGP, collected during the month for the community districts that have been queried
