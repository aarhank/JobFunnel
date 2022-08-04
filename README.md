## JobFunnel

<img alt="Spring" src="https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white"/> <img alt="Java" src="https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white"/>

Scrapes Jobs from Twitter, Indeed and Internshala, mails them weekly.       

BASE URL: https://jobfunnel.herokuapp.com/

DOCS: https://jobfunnel.herokuapp.com/swagger-ui/index.html#/


### Required request body
- ### User
```
{
    "jobTitle":	string,
    "userEmail": string,
    "userName":	string
}
```
- ### Job Search
```
{
    "jobTitle":	string,
    "mailId":	string,
    "mailSubject": string,
    "sendMail":	boolean
}
```

### Endpoints

* ```/v1.0/user```   
  Saves the user and sends latest jobs available on twitter,internshala and indeed by mail weekly.


* ```/v1.0/indeed```    
  Get jobs from indeed.
  

* ```/v1.0/internshala```    
  Get jobs from internshala.
  

* ```/v1.0/twitter```   
  Get jobs from twitter.
  
  
## Examples

- ### Twitter
**Endpoint:**      
```https://jobfunnel.herokuapp.com/v1.0/twitter```  
**Request:**       
 ```curl -X POST "https://jobfunnel.herokuapp.com/v1.0/twitter" -H "accept: */*" -H "Content-Type: application/json" -d "{ \"jobTitle\": \"Backend developer\", \"mailId\": \"string\", \"mailSubject\": \"string\", \"sendMail\": false}"```       
**Response:**       
  ```
  [
  {
    "jobTitle": "Backend developer",
    "jobDesc": "WE Are #hiring  #nodejs  Backend Developer min 5 years Experience ",
    "jobLink": "https://t.co/SaOThz5U8I",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "Lana is hiring a Junior Backend Developer - ADDITIVE d. Ebner Matthias &amp; Leiter Joachim OHG in Lana, Trentino-Alto Adige, Remote: ",
    "jobLink": "https://t.co/Jw6LEaJSNZ",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "JObros is hiring a Front end Developer in Mestre, Veneto, Remote: ",
    "jobLink": "https://t.co/REMf5L9n9S",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "We are Hiring - Backend Developer Lead  TeamPlus Staffing Solution https://t.co/Lwl2tEtkrF. 7-10 years ",
    "jobLink": "https://t.co/7nsRhzO9e0",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "Shure is hiring! Check out our latest opening - Backend Developer / DevOps Engineer in Eppingen, DE. Apply today... ",
    "jobLink": "https://t.co/PmZRiYoW4L",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "Aavalar is hiring!  Apply now for the position of Backend Java Developer ",
    "jobLink": "https://t.co/Z5XEtdkSrz",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "Hiring! Senior Backend Developer, £65,000 - #CityofLondon. https://t.co/IbplhkwGdH ",
    "jobLink": "https://t.co/iTNZmIPDhS",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "Looking to work as Backend Developer (m/f/d)? #Engineering #bachelor'sdegree #Fulltime #experienced #Germany #hiring #jobs 👇 ",
    "jobLink": "https://t.co/LYVbFzaZSB",
    "jobSource": "twitter"
  },
  {
    "jobTitle": "Backend developer",
    "jobDesc": "#blockchain ConsolPartners is hiring for the following position: Backend developer – blockchain. Link: ",
    "jobLink": "https://t.co/Gn2owbPbY1",
    "jobSource": "twitter"
  }
]
  ```

- ### Internshala
**Endpoint:**      
```https://jobfunnel.herokuapp.com/v1.0/internshala```      
**Request:**     
 ```curl -X POST "https://jobfunnel.herokuapp.com/v1.0/internshala" -H "accept: */*" -H "Content-Type: application/json" -d "{ \"jobTitle\": \"Frontend\", \"mailId\": \"string\", \"mailSubject\": \"string\", \"sendMail\": false}"```           
**Response:**
  ```
  [
  {
    "jobTitle": "Expertrec- Frontend",
    "jobDesc": "Start date Starts Immediately CTC 5 - 6 LPA Apply By 18 Aug' 22",
    "jobLink": "https://internshala.com/job/detail/frontend-engineer-react-angular-node-fresher-jobs-in-bangalore-at-expertrec1658205756",
    "jobSource": "internshala"
  },
  {
    "jobTitle": "Epixel Software Private Limited- Frontend",
    "jobDesc": "Start date Starts Immediately CTC 3 - 4 LPA Apply By 13 Aug' 22",
    "jobLink": "https://internshala.com/job/detail/frontend-development-fresher-jobs-in-multiple-locations-at-epixel-software-private-     limited1657798608",
    "jobSource": "internshala"
  },
  {
    "jobTitle": "Velozity Global Solutions- Frontend",
    "jobDesc": "Start date Starts Immediately CTC 5.4 - 13.5 LPA Apply By 13 Aug' 22",
    "jobLink": "https://internshala.com/job/detail/remote-reactjs-frontend-developer-fresher-jobs-at-velozity-global-solutions1657739872",
    "jobSource": "internshala"
  },
  {
    "jobTitle": "MiM-Essay- Frontend",
    "jobDesc": "Start date Starts Immediately CTC 5 - 6 LPA Apply By 12 Aug' 22",
    "jobLink": "https://internshala.com/job/detail/software-engineer-frontend-fresher-jobs-in-delhi-at-mim-essay1657697653",
    "jobSource": "internshala"
  },
  {
    "jobTitle": "Velozity Global Solutions- Frontend",
    "jobDesc": "Start date Starts Immediately CTC 5.4 - 13.5 LPA Apply By 12 Aug' 22",
    "jobLink": "https://internshala.com/job/detail/reactjs-frontend-developer-fresher-jobs-in-bangalore-at-velozity-global-solutions1657688446",
    "jobSource": "internshala"
  }
]
  ```
