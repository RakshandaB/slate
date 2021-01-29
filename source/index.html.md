---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - "Sample Request and responses"

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction
The base URL for all requests to the Spark API is:
**Version:** 1.0.0 

**AQ4 SPARK Terminology**
 
SPARK is a customized solution to integrate different solutions of WMS(warehouse management System) and TMS(Transport Management System) to form a wholesome product that the customer can readily use for the user’s Logistics needs.
 
These are the terms that are used in  SPARK

<text style="font-weight: bold;"> Horticulture Distribution Centre:-</text>  Horticulture Distribution Centre or facility are usually smaller than a firm’s warehouse and is used for receipt, temporary storage and re-distribution of goods according to the customer orders as they are received. They are also called branch warehouse or distribution Warehouse.

<text style="font-weight: bold;"> Store:-</text> A retail operation that sells plants and related products for the domestic garden as its primary business. It is a development from the concept of the retail plant nursery but with a wider range of outdoor products and on-site facilities.
 
<text style="font-weight: bold;"> Order:</text> Order is a note designed for processes that are involved in any transaction, such as order placing for work or the supply of goods or services. This is essential for retail industries to keep track of the records for any supply orders that are being placed.
 
<text style="font-weight: bold;"> Purchase Order: </text>A purchase order is a document that is sent from a buyer to a supplier requesting an order for merchandise. The purchase order usually lists the type of item, quantity, and agreed-upon price.
 
<text style="font-weight: bold;"> Consignment:</text>is a batch of goods scheduled to be picked up or dropped off at a certain location.
 
<text style="font-weight: bold;"> Load:</text> The Quantity that can be put in or on something for conveyance or transportation via freight, cargo or any other means.

<text style="font-weight: bold;"> Manifest:</text> A manifest in material-handling context is a list of cargo either delivered to or shipped from a warehouse. In transportation, manifest describes a list of cargo carried on a ship or plane, as well as an invoice of goods carried on a truck or train.

<text style="font-weight: bold;"> Driver:</text> Is a person who drives a vehicle and pursues it as a profession.

<text style="font-weight: bold;"> Trucks:</text> A truck or lorry is a motor vehicle designed to transport Goods and cargo. They vary greatly in size, power, and configuration.

<text style="font-weight: bold;"> Trailer:</text> A trailer is a container on wheels which is pulled by a truck or car and used for transporting large or heavy items.


<text style="font-weight: bold;"> Equipment:</text> These are a set of tools or resources for a particular purpose or an activity.

<text style="font-weight: bold;"> Trolley: </text>A Danish or Dutch trolley also known as flower trolleys, are used in horticulture for moving the plants from one place to another. This particular type of trolley contains Bases that form the bottom of the structure and usually comes with wheels, the sturdy posts which forms the wall of the trolley and supports the Shelves that hold the plants and pots.

<text style="font-weight: bold;"> Pallet:</text> These are wooden trays used in vertical gardening and it also helps grower to move and distribute them easily.

<text style="font-weight: bold;"> Cages:</text> A cage is an enclosure often made of mesh, bars, or wires, used to confine, contain or protect something (refers to plants in this case).
Corrugated Boxes: Box is a package in different sizes that contains various goods. Corrugated boxes are used extensively for transporting and storing fresh produce in the horticultural industry. These boxes protect their contents from mechanical damage due to drops, impacts, vibration and compression Loads.

<text style="font-weight: bold;"> Grower:</text> A grower is nothing but a farmer who deals in cultivating a particular type of crop, fruit or plant at a larger scale with an intent to sell.

<text style="font-weight: bold;"> POD (Proof of Delivery):</text> is a significant part of the delivery process as it establishes that the package has been delivered to the customer. Proof of delivery acts like a receipt that proves that the delivery has been made. It consists of a written acknowledgment of having received the order of a specific amount of money on a specific date and time, the name of the person who has received the product and other shipping details

<text style="font-weight: bold;"> EPOD:</text> An electronic proof of delivery (E-POD) is a digital format (usually PDF) of a traditional paper Delivery Order or Delivery Note. It is a fast-growing trend that more and more companies are now implementing into their workflow. The reasons for this shift to displace traditional paper delivery orders are simple. E-PODs save time, prevent disputes, and reduce the company’s carbon footprints.
 
 
 
 
<text style="font-weight: bold;"> WMS (warehouse management system):</text> The software solution that keeps track of all warehouse operations including receiving, put away, picking, shipping, and inventory.




# Request

The base URL for all requests to the Spark API is: Version: 1.0.0

**https://spark-dev.analyticsquad4.com/spark-api/api**

Our API is REST-based. This means:

1. It makes use of standard HTTP methods like **GET, POST, PUT, DELETE** .

2. The API uses standard HTTP error responses(status codes) to indicate status of your requests – success and error codes.

**Request Header**

|    Header      |   Sample Value     |    Description         | 
| -------------  |  ---------------   | ----------------       |
| Content-Type   |  application/json  |  JSON request          |
| Authorization  |  Bearer token      |  Authentication token  |


# Response

The Spark API uses HTTP status codes to indicate the status of your requests. This includes Success and Error codes.

|     code       |    message             |          Description                                            | 
| -------------  |  ---------------       | ---------------------------------------                         |
|     200        |   Success              |  This message means that the request is successfully processed. |
|     400        |   Bad Request          |  This message means that the request is syntactically incorrect.|
|     401        |   Unauthorized         |  This message means that invalid credentials are passed.  |
|     404        |   Not Found            |  This message means that the resource could not be found. |
|     500        |   Internal Server Error|  This message means that there is an issue with the Spark api.Please try accessing the request later|

<!-- old code -->
# Admin Controller

## Create Tenancy

Create or update a tenancy with this api 

> Definition

```shell
 "https://spark-dev.analyticsquad4.com/spark-api/api/createTenancy"
```


> Request Body

```shell
{
  "tenancyCode": "B&Q1",
  "tenancyName": "Tenancy name",
  "addressLine1": "Addr1",
  "addressLine2": "Addr2",
  "phoneNumber": 1234567890,
  "cityName": "City",
  "stateName": "London",
  "postcode": 12334,
  "countryName": "UK",
  "id": 1,
  "userId": 1,
  "roleId": 9,
  "organisationId": 0,
  "postCode": 12334
}
```

> Response

```shell
{
  "errorCode" : null,
  "errorMessage" : null,
  "message" : "Successfully Created tenancy details: ",
  "tenancyName" : "Tenancy name",
  "tenancyCode" : "B&Q1",
  "activeStatus" : true
}
```

### Request
<text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/createTenancy` 

**Request Body**

| Parameters     |  DataType     |  Required  | Description         |  
| ---------      | ----------    | -----------| -----------         | 
| tenancyCode    |  String       | Mandatory  | |
| tenancyName    |  String       | Mandatory  |       |
| addressLine1   |  String       | Mandatory  |      |
| addressLine2   |  String       | Optional   |        |
| phoneNumber    |  Long         | Mandatory  |       |
| cityName       |  String       | Mandatory  |        |
| stateName      |  String       | Mandatory  |       |
| postcode       |  Integer      | Mandatory  |      |
| countryName    |  String       | Mandatory  |       |
| id             |  Long         | Conditional Mandatory  |      |
| userId         |  Long         | Optional   |       |
| roleId         |  Long         | Optional   |        |
| organisationId |  Long         | Optional   |      |





## Get Tenancy

Get a tenancy detail with this api.

> Request 

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/getTenancyDetailById?tenancyId=1&userId=30"
```

> Response

```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Successfully fetched tenancy detail",
  "tenanacyDetailDTO": {
    "tenancyId": 1,
    "tenancyCode": "B&Q1",
    "tenancyName": "Tenancy name",
    "tenancyLogoUrl": "https://storage.googleapis.com/spark-image-dev/tenancy/logo/1/logo.png?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=spark-dev-gcs%40spark-dev-269304.iam.gserviceaccount.com%2F20210113%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20210113T061241Z&X-Goog-Expires=180&X-Goog-SignedHeaders=host&X-Goog-Signature=5cb0486484ca6d82ec80bfef0c890af1b3bdb50bdebe7b70dd281a1c73d04e2edd32c935e7735f71bb337064efd873e25db53a722704901ddbbbd8bef7407dd2f1c332a30194f4728bb324f117a81e293383c11f13d86585c01eb8ef5a1100f717fa797f554cee2376f72dc56873a4dc5307dbee24f2f1d5357d318fdbb5334b2a8d0d37810877bb628166888b00bed25970835316b48269bc6118faaebf27adbca4ec5d0ae5b8ee3be7d79ed5bef50fe5e96cf9f73fdae6724ebbba83c9d053a33df1f1d517fb7945fefac572a87e9c444aa9b2a9621b045fef6eaffc25515bfbf1083ec81e73776819e7d4e636017f17873dcda3ddd106e6096a2f3ef5ad35",
    "addressLine1": "Addr1",
    "addressLine2": "Addr2",
    "phoneNumber": 1234567890,
    "postcode": 12334,
    "countryId": 1,
    "countryName": "UK",
    "stateId": 1,
    "stateName": "London",
    "cityId": 1,
    "cityName": "City"
  }
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getTenancyDetailById` 

**Request Parameters**

| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| tenancyId  |  long       | Mandatory  | Unique Id of Tenancy|
| userId     |  long       | Mandatory  | Login User Id   |


## Get All Tenancy User
Get all tenancy detail with this api.

> Request 

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/getTenancyDetailById?tenancyId=1&userId=30"
```

> Response

```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Successfully fetched all tenancy user",
  "getAllTenancyUserDTOList": [
    {
      "userId": 24,
      "userName": "Ram",
      "emailId": "ramkumar2494hosalli@gmail.com",
      "phoneNumber": 8762502494,
      "active": true,
      "userRoles": [
        {
          "roleId": 6,
          "roleName": "HDC Auditor"
        },
        {
          "roleId": 7,
          "roleName": "XPO Manager"
        },
        {
          "roleId": 8,
          "roleName": "SPARK Super User"
        },
        {
          "roleId": 10,
          "roleName": "HDC Equipment Control Manager"
        }
      ]
    }
  ]
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getAllTenancyUser` 

**Request Parameters**

| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| userId     |  long       | Mandatory  | Login User Id       |


## Get All Store
Get all Stores with this api.

 > Request 
 
 ```shell
 "https://spark-dev.analyticsquad4.com/spark-api/api/getAllStore?userId=1"
 ```
 
 > Response
 
 ```shell
 {
   "errorCode": null,
   "errorMessage": null,
   "message": "Successfully fetched all the Stores",
   "storeDetailsList": [
     {
       "storeId": 12,
       "storeName": "BRAINTREE",
       "organisationType": "Store",
       "organisationId": 33,
       "oldStoreCode": "BAT625",
       "newStoreCode": "1198",
       "format": "SC",
       "region": "REG 08",
       "division": "South",
       "phoneNumber": 1376332511,
       "address": "Chapel Hill Retail Park, Charter Way, Braintree, Essex. CM7 8YH",
       "unitManagerName": "Robert Mansbridge",
       "emailId": "robert.mansbridge@b-and-q.co.uk",
       "unitManagerPhoneNumber": 234345765,
       "sparkUser": [
         {
           "userRoles": [
             {
               "roleId": 1,
               "roleName": "STORE user"
             }
           ],
           "userName": "Sam_braintree",
           "userId": 27,
           "emailId": "sam_str2@yahoo.com",
           "phoneNumber": 23434556767,
           "active": true
         }
       ],
       "active": true
     }
   ]
 }
 ```

### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getAllStore` 
 
**Request Parameters**
 
 
| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| userId     |  Long       | Mandatory  | Login User Id       |
 


## Get All Roles
Get all Roles with this api.
  
> Request 
   
```shell
   "https://spark-dev.analyticsquad4.com/spark-api/api/getAllRoles?userId=30"
```
   
> Response
   
```shell
   {
     "errorCode": null,
     "errorMessage": null,
     "message": "Fetched all user roles successfully",
     "getAllRoleResponseDTOS": [
       {
         "roleId": 1,
         "roleName": "STORE user"
       },
       {
         "roleId": 2,
         "roleName": "GROWER user"
       },
       {
         "roleId": 3,
         "roleName": "HDC Shift Manager"
       },
       {
         "roleId": 4,
         "roleName": "HDC Team Lead"
       },
       {
         "roleId": 5,
         "roleName": "HDC Warehouse Operatives"
       },
       {
         "roleId": 6,
         "roleName": "HDC Auditor"
       },
       {
         "roleId": 7,
         "roleName": "XPO Manager"
       },
       {
         "roleId": 8,
         "roleName": "SPARK Super User"
       },
       {
         "roleId": 9,
         "roleName": "SPARK Admin"
       },
       {
         "roleId": 10,
         "roleName": "HDC Equipment Control Manager"
       }
     ]
   }
```
  
### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getAllRoles` 
   
**Request Parameters**
   
   
| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| userId     |  Long       | Mandatory  | Login User Id       |
   


## Get All Hdc
Get all HDCs with this api.
  
> Request 
   
```shell
   "https://spark-dev.analyticsquad4.com/spark-api/api/getAllHdc?userId=30"
```
   
> Response
   
```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Successfully fetched all the HDCs",
  "hdcDetailsList": [
    {
      "dcId": 1,
      "dcName": "SWINDON",
      "organisationType": "HDC",
      "organisationId": 13,
      "emailId": "swindon@yahoo.com",
      "address": "Wincanton, B&Q Distribution Centre, Highworth Road, Swindon, Wiltshire, SN3 4QS",
      "phoneNumber": 1793839135,
      "loadPrefix": "SH",
      "equipmentContactName": "Dipesh Rai",
      "equipmentContactEmail": "dipesh.rai@b-and-q.co.uk",
      "equipmentContactPhoneNumber": 17818690704,
      "planningOrSystemContactName": "Phil Marsh",
      "planningOrSystemContactEmail": "phil.marsh@wincanton.co.uk",
      "planningOrSystemContactPhoneNumber": 7971466286,
      "sparkUser": [
        {
          "userRoles": [
            {
              "roleId": 3,
              "roleName": "HDC Shift Manager"
            }
          ],
          "userName": "Tim",
          "userId": 25,
          "emailId": "Tim.tl@yahoo.com",
          "phoneNumber": 345687654,
          "active": true
        },
        {
          "userRoles": [
            {
              "roleId": 3,
              "roleName": "HDC Shift Manager"
            }
          ],
          "userName": "Spark TestSM",
          "userId": 32,
          "emailId": "spart.testsm@yahoo.com",
          "phoneNumber": 4455667788,
          "active": true
        },
        {
          "userRoles": [
            {
              "roleId": 4,
              "roleName": "HDC Team Lead"
            }
          ],
          "userName": "Peter new",
          "userId": 35,
          "emailId": "petertarly@yahoo.com",
          "phoneNumber": 1212,
          "active": true
        },
        {
          "userRoles": [
            {
              "roleId": 3,
              "roleName": "HDC Shift Manager"
            }
          ],
          "userName": "Paul",
          "userId": 54,
          "emailId": "Paul@yahoo.com",
          "phoneNumber": 9916321773,
          "active": true
        },
        {
          "userRoles": [
            {
              "roleId": 5,
              "roleName": "HDC Warehouse Operatives"
            }
          ],
          "userName": "Rex",
          "userId": 58,
          "emailId": "rex@yahoo.com",
          "phoneNumber": 45676712,
          "active": true
        }
      ],
      "active": true
    }
  ]
}
```
  
### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getAllHdc` 
   
**Request Parameters**
   
   
| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| userId     |  Long       | Mandatory  | Login User Id       |
   
## Get All Grower
Get all Growers with this api.
  
> Request 
   
```shell
   "https://spark-dev.analyticsquad4.com/spark-api/api/getAllGrower?userId=30"
```
   
> Response
   
```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Successfully fetched all Growers",
  "growerDetails": [
    {
      "growerId": 1,
      "growerName": "Allensmore Nurseries",
      "organisationType": "Grower",
      "growerEmail": null,
      "organisationId": 1,
      "growerSupplyCode": 200016,
      "equipmentContactName": "Sally-Ann Greenman",
      "equipmentContactEmailId": null,
      "equipmentContactAlternateEmailId": null,
      "equipmentContactPhoneNumber": null,
      "planningContactName": "Sally-Ann Greenman",
      "planningContactEmailId": null,
      "planningContactAlternateEmailId": null,
      "planningContactPhoneNumber": null,
      "growerTelephoneNo": 1981500946,
      "temperature": null,
      "getAllGrowerSitesDTOS": [
        {
          "growerSiteId": 1,
          "growerAddress": "Tram Inn, Hereford, HR2 9AN",
          "growerSiteName": "Tram Inn",
          "emailAddress": null,
          "country": "UNITED KINGDOM",
          "getAllGrowerSiteSubCodeDTOS": [
            {
              "growerSiteId": 1,
              "growerSubCode": "200016"
            },
            {
              "growerSiteId": 1,
              "growerSubCode": "200016W"
            }
          ]
        },
        {
          "growerSiteId": 2,
          "growerAddress": "MADLEY NURSERY, BRAMPTON LANE MADLEY, HEREFORD, HR2 9LX",
          "growerSiteName": "MADLEY NURSERY",
          "emailAddress": null,
          "country": "UNITED KINGDOM",
          "getAllGrowerSiteSubCodeDTOS": [
            {
              "growerSiteId": 2,
              "growerSubCode": "520567"
            }
          ]
        }
      ],
      "sparkUser": [],
      "active": true
    }
  ]
}
```
  
### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getAllGrower` 
   
**Request Parameters**
   
   
| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| userId     |  Long       | Mandatory  | Login User Id       |
   

## Get All Driver User
Get all driver user with this api.

> Request 

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/getAllDriverUser?userId=30"
```

> Response

```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Successfully fetched all drivers",
  "getAllDriverUserDTOList": [
    {
      "userId": 41,
      "userName": "Joey Ad",
      "emailId": "joey.ad@yahoo.com",
      "phoneNumber": 8762502494,
      "driverID": "DR0001",
      "active": true,
      "driverFlag": true
    },
    {
      "userId": 59,
      "userName": "RJ",
      "emailId": "rj@gmail.com",
      "phoneNumber": 8762502498,
      "driverID": "DR125",
      "active": true,
      "driverFlag": true
    }
  ]
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">GET </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/getAllDriverUser` 

**Request Parameters**

| Parameters |  DataType   |  Required  | Description         |  
| ---------  | ----------  | -----------| -----------         | 
| userId     |  long       | Mandatory  | Login User Id       |

   
 
## Activate Deactivate Driver

Activate or deactivate driver user with this api.

> Definition

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/activateDeactivateDriver"
```

> Request Body

```shell
{
  "active": true,
  "adminId": 1,
  "userId": 59
}
```

> Response

```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Successfully activated driver",
  "active": true
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">PUT </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/activateDeactivateDriver` 

**Request Body**

| Parameters     |  DataType     |  Required  | Description         |  
| ---------      | ----------    | -----------| -----------         | 
| active         |  boolean      | Mandatory  |                     |
| adminId        |  Long         | Mandatory  |                     |
| userId         |  Long         | Mandatory  |                     |


## Activate Deactivate Organisation

Activate or deactivate organisation with this api.

> Definition

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/activateDeactivateOrganisation"
```

> Request Body

```shell
{
  "organisationId": 35,
  "organisationType": "HDC",
  "status": false,
  "userId": 1
}
```

> Response

```shell
{
  "errorCode" : null,
  "errorMessage" : null,
  "message" : "Successfully deactivated Organisation",
  "organisationId" : 35,
  "organisationName" : "Acno HDC",
  "activeStatus" : false
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/activateDeactivateOrganisation` 

**Request Body**

| Parameters        |  DataType     |  Required  | Description         |  
| ---------         | ----------    | -----------| -----------         | 
| organisationId    |  Long         | Mandatory  |                     |
| organisationType  |  Long         | Optional   |                     |
| status            |  boolean      | Mandatory  |                     |
| userId            |  Long         | Mandatory  |                     |

  
 
## Add Driver Users
Add driver users with this api

> Definition

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/addDriverUsers"
```

> Request Body

```shell
{
  "driverUserRequestDTOS": [
    {
      "userId": null,
      "userName": "Driver2",
      "phoneNumber": 89769886799,
      "driverID": "Driver2",
      "email": "manisha@gmail.com"
    }
  ],
  "adminId": 1
}
```

> Response

```shell
{
  "errorCode" : null,
  "errorMessage" : null,
  "message" : "Successfully added/updated driver users"
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/addDriverUsers` 

**Request Body**

| Parameters        |  DataType     |  Required              | Description         |  
| ---------         | ----------    | -----------            | -----------         | 
| userId            |  Long         | Conditional Mandatory  |                     |
| userName          |  Long         | Mandatory              |                     |
| email             |  boolean      | Mandatory              |                     |
| phoneNumber       |  Long         | Mandatory              |                     |
| driverID          |  Long         | Mandatory              |                     |
| adminId          |  Long          | Mandatory              |                     |

  
 

## Add Grower
Add or update grower with this api.

> Definition

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/addGrower"
```

> Request Body

```shell
{
  "growerName": "AQ4 Grower",
  "phoneNumber": 234123412,
  "supplierCode": 123456,
  "temperature": "12",
  "equipmentContactName": "Jeff Buttar",
  "equipmentContactEmail": "eqjane@yahoo.com",
  "equipmentContactAlternateEmail": "test1@yahoo.com",
  "planningOrSystemContactName": "Sally-Ann Greenman",
  "planningOrSystemContactEmail": "sally@yahoo.com",
  "planningOrSystemContactAlternateEmail": "test1@yahoo.com",
  "growerSite": [
    {
      "siteAddress": "whitefield, bangalore",
      "emailId": "test3@yahoo.com",
      "collectionSiteSubCode": [
        "123456A",
        "123456"
      ],
      "growerSiteId": 26,
      "growerAddress": "whitefield, bangalore",
      "growerSiteName": "sarita whitefield",
      "emailAddress": "test3@yahoo.com",
      "country": "UNITED KINGDOM",
      "getAllGrowerSiteSubCodeDTOS": [
        {
          "growerSiteId": 26,
          "growerSubCode": "123456A"
        },
        {
          "growerSiteId": 26,
          "growerSubCode": "123456"
        }
      ]
    }
  ],
  "sparkUser": [
    {
      "email": "test@yahoo.com",
      "phoneNumber": 6543234567,
      "userName": "Sarita",
      "roleIds": [
        2
      ],
      "userRoles": [
        {
          "roleId": 2,
          "roleName": "GROWER user"
        }
      ],
      "userId": 48,
      "emailId": "test@yahoo.com",
      "active": true
    }
  ],
  "growerId": null,
  "userId": 1
}
```

> Response

```shell
{
  "errorCode": null,
  "errorMessage": null,
  "message": "Grower added successfully",
  "growerName": "AQ4 Grower",
  "growerId": 43
}
```

### Request 
<text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/addGrower` 

**Request Body**

| Parameters        |  DataType     |  Required              | Description         |  
| ---------         | ----------    | -----------            | -----------         | 
| growerId            |  Long         |  Mandatory  |                     |
| growerName          |  Long         | Mandatory              |                     |
| phoneNumber             |  boolean      | Mandatory              |                     |
| supplierCode       |  Long         | Mandatory              |                     |
| temperature          |  Long         | Mandatory              |                     |
| equipmentContactName          |  Long          | Mandatory              |                     |
| equipmentContactEmail          |  Long          | Mandatory              |                     |
| planningOrSystemContactName          |  Long          | Mandatory              |                     |
| planningOrSystemContactEmail          |  Long          | Mandatory              |                     |
| equipmentContactAlternateEmail          |  Long          | Mandatory              |                     |
| planningOrSystemContactAlternateEmail          |  Long          | Mandatory              |                     |
| planningOrSystemContactEmail          |  Long          | Mandatory              |                     |
| userId          |  Long          | Mandatory              |                     |
| growerSite.siteAddress          |  Long          | Mandatory              |                     |

  
 
## Add Hdc
Add or update HDC with this api.
> Definition

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/addHdc"
```

> Request Body

```shell
{
  "dcName": "SWINDON",
  "dcAddress": "Wincanton, B&Q Distribution Centre, Highworth Road, Swindon, Wiltshire, SN3 4QS",
  "dcPhoneNumber": 1793839135,
  "dcEmail": "swindon@yahoo.com",
  "loadPrefix": "SH",
  "equipmentContactName": "Dipesh Rai",
  "equipmentContactEmail": "dipesh.rai@b-and-q.co.uk",
  "equipmentContactPhoneNumber": 17818690704,
  "planningContactName": "Phil Marsh",
  "planningContactEmail": "phil.marsh@wincanton.co.uk",
  "planningContactPhoneNumber": 7971466286,
  "sparkUser": [
    {
      "email": "Tim.tl@yahoo.com",
      "roleIds": [
        3
      ],
      "userRoles": [
        {
          "roleId": 3,
          "roleName": "HDC Shift Manager"
        }
      ],
      "userName": "Tim",
      "userId": 25,
      "emailId": "Tim.tl@yahoo.com",
      "phoneNumber": 345687654,
      "active": true
    }
  ],
  "dcId": null,
  "userId": 1
}
```

> Response

```shell
{
  "errorCode" : null,
  "errorMessage" : null,
  "message" : "Successfully added/updated hdc",
  "dcId" : 1,
  "dcName" : "SWINDON"
}
```


### Request 
<text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/addHdc` 

**Request Body**

| Parameters        |  DataType     |  Required              | Description         |  
| ---------         | ----------    | -----------            | -----------         | 
| dcName            |  Long         |  Mandatory  |                     |
| dcAddress          |  Long         | Mandatory              |                     |
| dcPhoneNumber             |  boolean      | Mandatory              |                     |
| dcEmail       |  Long         | Mandatory              |                     |
| loadPrefix          |  Long         | Mandatory              |                     |
| equipmentContactName          |  Long          | Mandatory              |                     |
| equipmentContactEmail          |  Long          | Mandatory              |                     |
| equipmentContactPhoneNumber          |  Long          | Mandatory              |                     |
| planningContactName          |  Long          | Mandatory              |                     |
| planningContactEmail          |  Long          | Mandatory              |                     |
| planningContactPhoneNumber          |  Long          | Mandatory              |                     |

  
## Add Store
Add or update store with this api.
> Definition

```shell
"https://spark-dev.analyticsquad4.com/spark-api/api/addStore"
```

> Request Body

```shell
{
  "oldStoreCode": "BAT625",
  "newStoreCode": "1198",
  "storeName": "BRAINTREE",
  "storeFormat": "SC",
  "region": "REG 08",
  "division": "South",
  "storePhoneNumber": 1376332511,
  "storeAddress": "Chapel Hill Retail Park, Charter Way, Braintree, Essex. CM7 8YH",
  "unitManagerName": "Robert Mansbridge",
  "unitManagerEmailId": "robert.mansbridge@b-and-q.co.uk",
  "unitManagerPhoneNumber": 234345765,
  "sparkUserDTOList": [
    {
      "email": "sam_str2@yahoo.com",
      "roleIds": [
        1
      ],
      "userRoles": [
        {
          "roleId": 1,
          "roleName": "STORE user"
        }
      ],
      "userName": "Sam_braintree",
      "userId": 27,
      "emailId": "sam_str2@yahoo.com",
      "phoneNumber": 23434556767,
      "active": true
    }
  ],
  "storeId": null,
  "userId": 1
}
```

> Response

```shell
{
  "errorCode" : null,
  "errorMessage" : null,
  "message" : "Successfully added/updated store",
  "storeId" : 12,
  "storeName" : "BRAINTREE"
}
```


### Request 
<text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/addStore` 

**Request Body**

| Parameters        |  DataType     |  Required              | Description         |  
| ---------         | ----------    | -----------            | -----------         | 
| oldStoreCode            |  Long         |  Mandatory  |                     |
| newStoreCode          |  Long         | Mandatory              |                     |
| storeName             |  boolean      | Mandatory              |                     |
| storeFormat       |  Long         | Mandatory              |                     |
| region          |  Long         | Mandatory              |                     |
| division          |  Long          | Mandatory              |                     |
| storePhoneNumber          |  Long          | Mandatory              |                     |
| storeAddress          |  Long          | Mandatory              |                     |
| unitManagerName          |  Long          | Mandatory              |                     |
| unitManagerEmailId          |  Long          | Mandatory              |                     |
| unitManagerPhoneNumber          |  Long          | Mandatory              |                     |
| storeId          |  Long          | Mandatory              |                     |
| userId          |  Long          | Mandatory              |                     |

  


## Add Tenancy Users
 Add or update tenancy users with this api.
 
 > Definition
 
 ```shell
 "https://spark-dev.analyticsquad4.com/spark-api/api/addTenancyUsers"
 ```
 
 > Request Body
 
 ```shell
 {
   "tenancyUsers": [
     {
       "userId": null,
       "userName": "Test user",
       "phoneNumber": 67869886799,
       "roleIds": [
         8
       ],
       "email": "test@gmail.com"
     }
   ],
   "userId": 1
 }
 ```
 
 > Response
 
 ```shell
 {
   "errorCode" : null,
   "errorMessage" : null,
   "message" : "Successfully added/updated tenancy user",
   "userIds" : [ 38 ]
 }
 ```
 
 
 ### Request 
 <text style="font-weight:bold;border: 2px solid green">POST </text>    `https://spark-dev.analyticsquad4.com/spark-api/api/addTenancyUsers` 
 
 **Request Body**
 
| Parameters        |  DataType     |  Required              | Description         |  
| ---------         | ----------    | -----------            | -----------         | 
| userId            |  Long         |  Mandatory  |                     |
| tenancyUsers.userId          |  Long         | Mandatory              |                     |
| tenancyUsers.userName              |  boolean      | Mandatory              |                     |
| tenancyUsers.phoneNumber        |  Long         | Mandatory              |                     |
| tenancyUsers.roleIds           |  Long         | Mandatory              |                     |
| tenancyUsers.email           |  Long          | Mandatory              |                     |
 


## Delete Grower
Delete grower with this api

 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** deleteGrower

### HTTP Request 
<text style="color:red;font-weight: bold;">DELETE-</text>` /api/deleteGrower` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| growerId | query | growerId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 401 | Unauthorized |
| 403 | Forbidden |

## deleteHdc
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** deleteHdc

### HTTP Request 
<text style="color:red;font-weight: bold;">DELETE-</text>` /api/deleteHdc` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| hdcId | query | hdcId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 401 | Unauthorized |
| 403 | Forbidden |

## deleteStore
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** deleteStore

### HTTP Request 
<text style="color:red;font-weight: bold;">DELETE-</text>` /api/deleteStore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| storeId | query | storeId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 401 | Unauthorized |
| 403 | Forbidden |

# User Controller
## updatePersonalSettings
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updatePersonalSettings

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateProfilePic` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| profilePic | formData | profilePic | No | file |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## updatePersonalSettings
> Request Payload:

```
{
  "cityId": 0,
  "countryId": 0,
  "newAddress": "string",
  "newPhoneNumber": 0,
  "postalCode": "string",
  "stateId": 0,
  "timeZone": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updatePersonalSettings

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updatePersonalDetails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updatePersonalDetailsDTO | body | updatePersonalDetailsDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## login
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** login

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/login` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| emailId | query | emailId | Yes | string |
| Password | query | Password | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getUserDetailById
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getUserDetailById

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getUserDetailById` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getStockAuditStatus
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getStockAuditStatus

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getStockAuditStatus` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getAllTimeZones
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllTimeZones

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllTimeZones` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllStatesByCountryId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllStatesByCountryId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllStatesByCountryId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| countryId | query | countryId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllCountries
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllCountries

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllCountries` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllCities
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllCities

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllCities` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| statesId | query | statesId | Yes | long |
| countryId | query | countryId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## forgotPassword
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** forgotPassword

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/forgotPassword` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| emailId | query | emailId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## changePassword
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** changePassword

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/changePassword` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| emailId | query | emailId | Yes | string |
| newPassword | query | newPassword | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## activateDeactivateUser
> Request Payload:

```
{
  "adminId": 0,
  "organisationId": 0,
  "state": true,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** activateDeactivateUser

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/activateDeactivateUser` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| activateDeactivateUserRequestDTO | body | activateDeactivateUserRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# HDC Controller


## updateTrailerOrBayNumber
 > Request Payload:

```
{
  "bayNumber": "string",
  "loadDetailId": 0,
  "tractorNumber": "string",
  "trailerNumber": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateTrailerOrBayNumber

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/updateTrailerOrBayNumber` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateTrailerBayNumberDTO | body | updateTrailerBayNumberDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## printDriverCollectionManifest
> Request Payload:

```
{
  "loadDetailsId": [
    0
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** printDriverCollectionManifest

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/printDriverCollectionManifest` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| printDriverCollectionManifest | body | printDriverCollectionManifest | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## updateStoreLocation
> Request Payload:

```
{
  "consignmentNumber": "string",
  "loadId": "string",
  "organisationId": 0,
  "storeId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateStoreLocation

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateStoreLocation` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateStoreLocation | body | updateStoreLocation | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



## updateActualShelvesCount
> Request Payload:

```
[
  {
    "consignmentId": 0,
    "consignmentNumber": "string",
    "consignmentTrolleyDetailsId": 0,
    "numberOfShelves": 0,
    "trolleySequence": "string",
    "userId": 0
  }
]

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateActualShelvesCount

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateActualShelvesCount` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| organisationId | query | organisationId | Yes | long |
| roleId | query | roleId | Yes | long |
| updateActualShelvesCountDTOS | body | updateActualShelvesCountDTOS | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## splitTrolley
> Request Payload:

```
{
  "consignmentNumber": "string",
  "organisationId": 0,
  "trolleySequence": "string",
  "userId": 0
}


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** splitTrolley

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/splitTrolley` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| splitTrolleyRequestDTO | body | splitTrolleyRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## removeLoadFromWLs
 > Request Payload:

```
{
  "loadId": [
    0
  ],
  "userId": 0,
  "wlsScheduled": true
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** removeLoadFromWLs

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/removeLoadFromWLs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| removeFromWls | body | removeFromWls | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## printLoadingSchedule
 > Request Payload:

```
{
  "organisationId": 0,
  "requestedDate": "string",
  "userId": 0,
  "wlsInbound": true,
  "wlsOutbound": true
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** printLoadingSchedule

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/printLoadingSchedule` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| printLoadingScheduleRequestDTO | body | printLoadingScheduleRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## printDriverDeliveryManifest
  > Request Payload:

```
{
  "loadDetailsId": [
    0
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** printDriverDeliveryManifest

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/printDriverDeliveryManifest` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| printDriverCollectionManifest | body | printDriverCollectionManifest | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## printDriverControlSheet
  > Request Payload:

```
{
  "loadDetailsId": [
    0
  ],
  "userId": 0
}


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** printDriverControlSheet

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/printDriverControlSheet` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| printDriverCollectionManifest | body | printDriverCollectionManifest | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## isQcReturnEligible
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** isQcReturnEligible

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/isQcReturnEligible` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| consignmentNumber | query | consignmentNumber | Yes | string |
| consignmentDetailsId | query | consignmentDetailsId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## insertTripDetails
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** insertTripDetails

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/insertTripDetails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadDetailId | query | loadDetailId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## importPlanningSheet
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** importPlanningSheet

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/importPlanningSheet` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| planningSheet | formData | planningSheet | Yes | file |
| userId | query | userId | Yes | long |
| roleId | query | roleId | Yes | long |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getUnattachedConsignmentList
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getUnattachedConsignmentList

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getUnattachedConsignmentList` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |
| roleId | query | roleId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getTrolleyDetailsForHdc
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTrolleyDetailsForHdc

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTrolleyDetailsForHdc` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| consignmentId | query | consignmentId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getMinAndMaxDateByLoadDetailId
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getMinAndMaxDateByLoadDetailId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getMinAndMaxDateByLoadDetailId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadDetailId | query | loadDetailId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getLoadListingTripComplete
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getLoadListingTripComplete

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getLoadListingTripComplete` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getLoadListing
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getLoadListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getLoadListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadListingRequestDTO | body | loadListingRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getImportSheetErrorLogs
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getImportSheetErrorLogs

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getImportSheetErrorLogs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| roleId | query | roleId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getConsignmentsListingByLoadId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getConsignmentsListingByLoadId

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getConsignmentsListingByLoadId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| consignmentsListingByLoadIdRequestDTO | body | consignmentsListingByLoadIdRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getConsignmentsByLoadDetailId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getConsignmentsByLoadDetailId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getConsignmentsByLoadDetailId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadDetailId | query | loadDetailId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getAllTripNumber
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllTripNumber

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllTripNumber` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |
| roleId | query | roleId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getAllStores
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllStores

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllStores` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| routeId | query | routeId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllRouteNumber
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllRouteNumber

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllRouteNumber` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |
| roleId | query | roleId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getAllHdcDepot
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllHdcDepot

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllHdcDepot` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllDrivers
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllDrivers

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllDrivers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllConsignmentNumberByLoadDetailId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllConsignmentNumberByLoadDetailId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllConsignmentNumberByLoadDetailId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadDetailIds | query | loadDetailIds | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## createLoad
> Request Payload:

```SampleRequest
{
  "userId": 30,
  "loadId": "SH3090",
  "hdcDepotName": "SWINDON",
  "tripNumber": 1,
  "deliveryDepotName": "SWINDON",
  "routeNumber": 1,
  "hdcDepotDepartureDate": "12-12-2020",
  "hdcDepotDepartureTime": "15:36:14",
  "hdcDepotArrivalDate": "13-12-2020",
  "hdcDepotArrivalTime": "15:36:24",
  "deliveryDepotDepartureDate": null,
  "deliveryDepotDepartureTime": null,
  "deliveryDepotArrivalDate": null,
  "deliveryDepotArrivalTime": null
}
```

> Response Payload:

```SampleRequest
{
 "errorCode" : null,
 "errorMessage" : null,
 "message" : "successfully saved load details",
 "loadDetails" : {
  "recordStatus" : true,
  "createdBy" : 30,
  "createdOn" : "2020-12-11T10:06:36.535",
  "updatedBy" : 30,
  "updatedOn" : "2020-12-11T10:06:36.535",
  "id" : 2631,
  "loadId" : "SH3090",
  "tractor" : null,
  "driverId" : null,
  "driver" : null,
  "trailer" : null,
  "currentLocation" : null,
  "currentDestination" : null,
  "loadStatusLookupVal" : {
   "id" : 6,
   "lookupValueName" : "Not Scheduled",
   "lookup" : {
    "id" : 3,
    "lookupName" : "LOAD STATUS"
   }
  },
  "routeId" : 1,
  "remarks" : null,
  "wlsStatusLookupVal" : {
   "id" : 13,
   "lookupValueName" : "Active",
   "lookup" : {
    "id" : 4,
    "lookupName" : "WLS STATUS"
   }
  },
  "totalShelves" : 0,
  "totalBase" : 0,
  "totalPosts" : 0,
  "totalTrolley" : 0,
  "totalBox" : 0,
  "totalPallets" : 0,
  "vehicleId" : null,
  "loadType" : "Outbound",
  "tripType" : "D",
  "tripNumber" : 1,
  "tripStartDepot" : "SWINDON",
  "hdcDepot" : "SWINDON",
  "expectedHdcArrivalDate" : "2020-12-13T15:36:24",
  "actualHdcArrivalDate" : null,
  "expectedHdcDepartureDate" : "2020-12-12T15:36:14",
  "actualHdcDepartureDate" : null,
  "hdcDeliveryDepot" : "SWINDON",
  "expectedDeliveryDepotArrivalDate" : null,
  "actualDeliveryDepotArrivalDate" : null,
  "expecteDeliveryDepotDepartureDate" : null,
  "actualDeliveryDepotDepartureDate" : null,
  "state" : {
   "id" : 1,
   "stateName" : "Null",
   "stateFor" : "Load"
  },
  "trailerNumber" : null,
  "bayNumber" : null,
  "tractorNumber" : null,
  "valid" : true,
  "adhocLoad" : true,
  "inbound" : false,
  "outbound" : false
 }
} 
```

> Success response:

```


```

> Failure response:

```


```
**Summary:** This API fetches creates load.

**HTTP Request** 

<text style="color:green;font-weight: bold;">GET-</text> `https://spark-dev.analyticsquad4.com/spark-api/api/createLoad` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userEmailId | query | userEmailId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## confirmLoadListingTripComplete
 > Request Payload:

```
{
  "inTransitFlag": true,
  "loadId": "string",
  "mtCollectFromStoreDTOS": [
    {
      "mtBasesCollectFromStore": 0,
      "mtPostsCollectFromStore": 0,
      "mtShelvesCollectFromStore": 0,
      "organisationNameForStore": "string"
    }
  ],
  "userId": 0,
  "userRoleId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** confirmLoadListingTripComplete

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/confirmLoadListingTripComplete` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| confirmTripCompleteRequestDTO | body | confirmTripCompleteRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## changeTimeForAttachConsignment
 > Request Payload:

```
[
  {
    "consignmentCollectionTime": "string",
    "consignmentDeliveryTime": "string",
    "consignmentId": 0
  }
]

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** changeTimeForAttachConsignment

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/changeTimeForAttachConsignment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| consignmentTimeDTOS | body | consignmentTimeDTOS | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## addLoadToWls
 > Request Payload:

```
{
  "loadId": [
    0
  ],
  "userId": 0,
  "wlsScheduled": true
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** addLoadToWls

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/addLoadToWls` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| addToWls | body | addToWls | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## assignDriverIDToLoad
 > Request Payload:

```
{
  "driverID": "string",
  "loadDetailId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** assignDriverIDToLoad

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/assignDriverIDToLoad` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| driverAndTractorNumberRequestDTO | body | driverAndTractorNumberRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## attachedConsignmentsToLoad
 > Request Payload:

```
{
  "consignmentIds": [
    0
  ],
  "loadDetailsId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** attachedConsignmentsToLoad

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/attachedConsignmentsToLoad` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| attachedConsignmentsDTO | body | attachedConsignmentsDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## cancelMissedDeliveries
 > Request Payload:

```
{
  "loadDetailIds": [
    0
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** cancelMissedDeliveries

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/cancelMissedDeliveries` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| cancelLoadRequestDTO | body | cancelLoadRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## detachedConsignmentFromLoad
 > Request Payload:

```

{
  "consignmentId": 0,
  "ieCancelled": true,
  "loadDetailId": 0,
  "organisationId": 0,
  "qcReturn": true,
  "roleId": 0,
  "userId": 0
}


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** detachedConsignmentFromLoad

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/detachedConsignmentFromLoad` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| detachedConsignmentFromLoadDTO | body | detachedConsignmentFromLoadDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Grower Controller

## updateTrolleyDetails
 > Request Payload:

```
[
  {
    "consignmentId": 0,
    "consignmentNumber": "string",
    "consignmentTrolleyDetailsId": 0,
    "numberOfShelves": 0,
    "trolleySequence": "string",
    "userId": 0
  }
]

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** updateTrolleyDetails

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateTrolleyDetails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateTrolleyDetailsDTO | body | updateTrolleyDetailsDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## updateConsignmentsPOAndASNByUploadingFile
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateConsignmentsPOAndASNByUploadingFile

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateConsignmentsPOAndASNByUploadingFile` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentListingFile | formData | consignmentListingFile | Yes | file |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## updateConsignmentsPOAndASN  
> Request Payload:

```
[
  {
    "asnNumber": "string",
    "consignmentNumber": "string",
    "poNumber": "string",
    "userId": 0
  }
]


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateConsignmentsPOAndASN

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/updateConsignmentsPOAndASN` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateConsignmentDTO | body | updateConsignmentDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



## stockTakeWindow
> Request Payload:

```
{
  "organisationId": 0,
  "roleId": 0,
  "trolleyBaseCount": 0,
  "trolleyPostCount": 0,
  "trolleyShelvesCount": 0,
  "userId": 0
}


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** stockTakeWindow

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/stockTakeWindow` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| stockTakeWindowDTO | body | stockTakeWindowDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## removeTrolley
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** removeTrolley

### HTTP Request 
<text style="color:red;font-weight: bold;">DELETE-</text>` /api/removeTrolley` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| trolleySequence | query | trolleySequence | Yes | string |
| consignmentNumber | query | consignmentNumber | Yes | string |
| consignmentId | query | consignmentId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 401 | Unauthorized |
| 403 | Forbidden |

## printTrackHeaders
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** printTrackHeaders

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/printTrackHeaders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getTrolleySequenceByLoad
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTrolleySequenceByLoad

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getTrolleySequenceByConsignment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| getTrolleySequenceByLoadRequestDTO | body | getTrolleySequenceByLoadRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getTrolleyDetailsForpallet
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTrolleyDetailsForpallet

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTrolleyDetailsForpallet` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| consignmentId | query | consignmentId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getTrolleyDetails
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTrolleyDetails

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTrolleyDetails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| consignmentId | query | consignmentId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getGrowerByOrganisationId
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getGrowerByOrganisationId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getGrowerByOrganisationId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getConsignmentsListing
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getConsignmentsListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getConsignmentsListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| consignmentListingRequestDTO | body | consignmentListingRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## addNewTrolleyRow
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** addNewTrolleyRow

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/addNewTrolleyRow` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| consignmentId | query | consignmentId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## bulkPrintTrackHeaders
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** bulkPrintTrackHeaders

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/bulkPrintTrackHeaders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| loadId | query | loadId | Yes | string |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



## bulkShelvesUpdate
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** bulkShelvesUpdate

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/bulkShelvesUpdate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| file | formData | file | Yes | file |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## bulkTrolleyGenerate
 > Request Payload:

```
{
  "consignmentNumberList": [
    "string"
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** bulkTrolleyGenerate

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/bulkTrolleyGenerate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| bulkTrolleyGenerateRequestDTO | body | bulkTrolleyGenerateRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## deleteUser
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** deleteUser

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/deleteUser` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| deleteUserRequestDTO | body | deleteUserRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

# Equipment Controller


## saveOrUpdateConsignment
 > Request Payload:

```
{
  "baseCount": 0,
  "collectionPointId": 0,
  "consignmentId": 0,
  "consignmentNumber": "string",
  "deliveryPointId": 0,
  "growerCollectionSiteId": 0,
  "growerDeliverySiteId": 0,
  "organisationId": 0,
  "postCount": 0,
  "shelvesCount": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** saveOrUpdateConsignment

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/saveOrUpdateConsignment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| createOrUpdateMtEquipmentDTO | body | createOrUpdateMtEquipmentDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## moveCurrentStockDataToStockHistory
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** moveCurrentStockDataToStockHistory

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/moveCurrentStockDataToStockHistory` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getTenancyTotalStock
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTenancyTotalStock

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTenancyTotalStock` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getStockAuditHistory
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getStockAuditHistory

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getStockAuditHistory` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getOrganisationByTypes
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getOrganisationByTypes

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getOrganisationByTypes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| organisationTypeDTO | body | organisationTypeDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getEquipmentStockBalanceByOrganisationType
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getEquipmentStockBalanceByOrganisationType

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getEquipmentStockBalanceByOrganisationType` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationType | query | organisationType | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getEquipmentStockBalance
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getEquipmentStockBalance

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getEquipmentStockBalance` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllOrganisationType
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllOrganisationType

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllOrganisationType` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllLoadsByDateRange
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllLoadsByDateRange

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllLoadsByDateRange` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| startDate | query | startDate | Yes | string |
| endDate | query | endDate | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllEquipmentConsignment
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllEquipmentConsignment

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllEquipmentConsignment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllDeliveryPoints
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllDeliveryPoints

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllDeliveryPoints` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## generateEquipmentConsignmentNumber
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** generateEquipmentConsignmentNumber

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/generateEquipmentConsignmentNumber` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## deleteConsignment
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** deleteConsignment

### HTTP Request 
<text style="color:red;font-weight: bold;">DELETE-</text>` /api/deleteConsignment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentId | query | consignmentId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 401 | Unauthorized |
| 403 | Forbidden |


## adjustEquipmentStock
 > Request Payload:

```
[
  {
    "base": 0,
    "mtBases": 0,
    "mtPosts": 0,
    "mtShelves": 0,
    "organisationId": 0,
    "post": 0,
    "shelves": 0,
    "userId": 0
  }
]

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** adjustEquipmentStock

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/adjustEquipmentStock` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| adjustEquipmentStockInputList | body | adjustEquipmentStockInputList | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## downloadStockAuditHistory
 > Request Payload:

```
{
  "auditNumbers": [
    "string"
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** downloadStockAuditHistory

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/downloadStockAuditHistory` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| downloadStockHistoryRequestDTO | body | downloadStockHistoryRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## enableStockAuditLog
 > Request Payload:

```
{
  "auditEndDate": "string",
  "auditStartDate": "string",
  "organisationIds": [
    0
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** enableStockAuditLog

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/enableStockAuditLog` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| enableStockAuditDTO | body | enableStockAuditDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## endActiveAudit
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** endActiveAudit

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/endActiveAudit` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| auditNumber | query | auditNumber | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

# Socket Conroller
## workbench
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** workbench

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/workbench` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## tasksAndNotifications
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** tasksAndNotifications

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/tasksAndNotifications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## sendMessage
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** sendMessage

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/sendMessage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## loadListing
  > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** loadListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/loadListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getChatHistory
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getChatHistory

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/history` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## growerConsignmentListing
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** growerConsignmentListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/growerConsignmentListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## consignmentListing
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** consignmentListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/consignmentListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## approvals
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** approvals

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/approvals` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## equipments
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** equipments

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/equipments` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Mobile Api Controller

## getOrganisationDetailByName
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getOrganisationDetailByName

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getOrganisationDetailByName` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| organisationName | query | organisationName | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## validateTrolleyId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** validateTrolleyId

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/validateTrolleyId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| trolleyId | query | trolleyId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## updateLoadMTEquipmentCounts
> Request Payload:

```
{
  "base": 0,
  "loadId": "string",
  "organisationId": 0,
  "post": 0,
  "shelves": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateLoadMTEquipmentCounts

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/updateLoadEquipmentCounts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateLoadEquipmentCountDTO | body | updateLoadEquipmentCountDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



## updateHdcShelves
> Request Payload:

```
[
  {
    "consignmentNumber": "string",
    "organisationId": 0,
    "shelvesCount": 0,
    "trolleyId": 0,
    "trolleySequence": "string",
    "userId": 0
  }
]

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** updateHdcShelves

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateHdcShelves` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateShelvesDTO | body | updateShelvesDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getLoadDriverDetail
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getLoadDriverDetail

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/getLoadDriverDetail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getEquipmentStockByOrganisationIdOrName
> Request Payload:

```
{
  "organisationId": 0,
  "organisationName": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getEquipmentStockByOrganisationIdOrName

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/getEquipmentStockByOrganisationIdOrName` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| equipmentStockRequestDTO | body | equipmentStockRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getAllOrganisationByType
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllOrganisationByType

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllOrganisationByType` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| organisationType | query | organisationType | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllLoadByStore
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllLoadByStore

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllLoadByStore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getAllHdcByUser
> Response Payload:

```SampleRequest
{
"errorCode": null,
"errorMessage": null,
"message": "Successfully fetched all HDCs based on user email id",
"getAllHdcByUserResponseDTOList": [
{
"organisationId": 18,
"hdcName": "Cambuslang"
},
{
"organisationId": 14,
"hdcName": "Exeter"
},
{
"organisationId": 17,
"hdcName": "Heywood"
},
{
"organisationId": 13,
"hdcName": "Swindon"
},
{
"organisationId": 402,
"hdcName": "AQ4_WHITEFIELD"
},
{
"organisationId": 403,
"hdcName": "AQ4_BROOKFIELD"
}
]
}
```

> 

**Summary:** This API fetches all HDC users by email id.

**HTTP Request** 

<text style="color:green;font-weight: bold;">GET-</text> `https://spark-dev.analyticsquad4.com/spark-api/api/getAllHdcByUser?userEmailId=tim.tl@yahoo.com` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userEmailId | query | userEmailId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
## auditTrailForLoadByOrganisation
> Request Payload:

```
{
  "base": 0,
  "loadId": "string",
  "organisationName": "string",
  "post": 0,
  "shelves": 0,
  "userId": 0,
  "userRoleId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** auditTrailForLoadByOrganisation

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/auditTrailForLoadByOrganisation` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| auditTrailDTO | body | auditTrailDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |





# Upload Controller

## uploadDocument
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** uploadDocument

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/uploadDocument` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| documentTypes | query | documentTypes | Yes | string |
| files | body | files | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getUploadedDocument
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getUploadedDocument

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getUploadedDocuments` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| consignmentNumber | query | consignmentNumber | Yes | string |
| documentTypes | query | documentTypes | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## bulkUploadDeliveryNote
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** bulkUploadDeliveryNote

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/bulkUploadDeliveryNote` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| loadId | query | loadId | Yes | string |
| documentFile | formData | documentFile | Yes | file |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



# Reports controller

## adjustmentReport
 > Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** adjustmentReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/adjustmentReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## wlsWeeklyReport
 > Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "inbound": true,
  "outbound": true,
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** wlsWeeklyReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/wlsWeeklyReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## shelvesMismatchReport
> Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** shelvesMismatchReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/shelvesMismatchReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## locationBalanceReport
> Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** locationBalanceReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/locationBalanceReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## consignmentDefectReport

> Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** consignmentDefectReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/consignmentDefectReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## collectionAnalysisReport
> Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** collectionAnalysisReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/collectionAnalysisReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## equipmentDefectReport
> Request Payload:

```
{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** equipmentDefectReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/equipmentDefectReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## equipmentDeliveredReport
> Request Payload:

```

{
  "hdcName": [
    "string"
  ],
  "week": 0,
  "year": 0
}


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** equipmentDeliveredReport

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/equipmentDeliveredReport` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reportsRequestDTO | body | reportsRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Driver App Controller

## updateTrip
 > Request Payload:

```
{
  "emptyTrailerFlag": true,
  "equipmentBases": 0,
  "equipmentPosts": 0,
  "equipmentShelves": 0,
  "loadId": "string",
  "sealNumber": "string",
  "tractorNumber": "string",
  "trailerNumber": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateTrip

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/updateTrip` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateTripRequestDTO | body | updateTripRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



## updateDeliveryDetails

> Request Payload:

```
{
  "destination": "string",
  "loadId": "string",
  "sealOutNumber": "string",
  "signature": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** updateDeliveryDetails

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/updateDeliveryDetails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateDeliveryDetailsDTO | body | updateDeliveryDetailsDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## tripStartEnd
> Request Payload:

```
{
  "eventName": "string",
  "latitude": "string",
  "loadId": "string",
  "longitude": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** tripStartEnd

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/tripStartEnd` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| tripStartEndRequestDTO | body | tripStartEndRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## saveTripOfflineData
> Request Payload:

```
{
  "loadId": "string",
  "trip": [
    {
      "actualDateTime": "string",
      "destination": "string",
      "emptyEquipmentCollection": true,
      "emptyEquipmentDelivery": true,
      "eventName": "string",
      "growerSignature": "string",
      "latitude": "string",
      "legType": "string",
      "longitude": "string",
      "mtBaseCollection": 0,
      "mtEquipmentCollectionStoreSignature": "string",
      "mtEquipmentDeliveryGrowerSignature": "string",
      "mtPostCollection": 0,
      "mtShelvesCollection": 0,
      "sealInNumber": "string",
      "sealOutNumber": "string",
      "storeSignature": "string",
      "tripType": "string"
    }
  ],
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** saveTripOfflineData

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/saveTripOfflineData` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| saveTripOfflineDataDTO | body | saveTripOfflineDataDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getUserInfo
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getUserInfo

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getUserInfo` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| token | query | token | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getTrolleyDetailsByLoadId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTrolleyDetailsByLoadId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTrolleyDetailsByLoadId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadId | query | loadId | Yes | string |
| destination | query | destination | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getTripDetailsByLoadId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTripDetailsByLoadId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTripDetailsByLoadId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getTripDetailsByDate
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTripDetailsByDate

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTripDetailsByDate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| date | query | date | Yes | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getTrailerNumberByLoadId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTrailerNumberByLoadId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTrailerNumberByLoadId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getMtEquipmentCountsByLoadId
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getMtEquipmentCountsByLoadId

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getMtEquipmentCountsByLoadId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## confirmMtEquipmentCollection
> Request Payload:

```
{
  "destination": "string",
  "loadId": "string",
  "mtBase": 0,
  "mtPost": 0,
  "mtShelves": 0,
  "storeSignature": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** confirmMtEquipmentCollection

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/confirmMtEquipmentCollection` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| confirmMtEquipmentCollectionDTO | body | confirmMtEquipmentCollectionDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## confirmMtEquipmentDelivery
> Request Payload:

```
{
  "destination": "string",
  "growerSignature": "string",
  "loadId": "string",
  "mtBase": 0,
  "mtPost": 0,
  "mtShelves": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** confirmMtEquipmentDelivery

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/confirmMtEquipmentDelivery` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| confirmMtEquipmentDeliveryDTO | body | confirmMtEquipmentDeliveryDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Pallet Controller

## getPalletConsignmentCount
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getPalletConsignmentCount

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getPalletConsignmentCount` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |
| palletID | query | palletID | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |




## palletReceivedAtHdc
> Request Payload:

```
{
  "organisationId": 0,
  "palletId": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** palletReceivedAtHdc

### HTTP Request 
<text style="color:green;font-weight: bold;">PUT-</text>` /api/palletReceivedAtHdc` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| palletReceivedRequestDTO | body | palletReceivedRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getPalletListing
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getPalletListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/palletListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| palletListingRequestDTO | body | palletListingRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## getAllPalletID
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getAllPalletID

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getAllPalletID` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## deleteConsignmentFromPallet
> Request Payload:

```
{
  "consignmentId": 0,
  "organisationId": 0,
  "palletID": "string",
  "roleId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** deleteConsignmentFromPallet

### HTTP Request 
<text style="color:red;font-weight: bold;">DELETE-</text>` /api/deleteConsignmentFromPallet` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| deleteConsignmentFromReqestDTO | body | deleteConsignmentFromReqestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 401 | Unauthorized |
| 403 | Forbidden |


## createPallet
> Request Payload:

```
{
  "consignmentId": [
    0
  ],
  "id": 0,
  "organisationId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** createPallet

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/createPallet` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| createPalletRequestDTO | body | createPalletRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



# Generic Controller

## getLookupValueByLookupName
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getLookupValueByLookupName

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getLookupValueByLookupName` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| lookupName | query | lookupName | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## generateUniqueId
 > Request Payload:

```
{
  "columnName": "string",
  "currentTableName": "string",
  "dcId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** generateUniqueId

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/generateUniqueId` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| generateUniqueIdDTO | body | generateUniqueIdDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |



# Message Notification Controller

## saveMessages
> Request Payload:

```
{
  "consignmentNumber": "string",
  "messageDescription": "string",
  "messageTemplateId": 0,
  "organisationId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** saveMessages

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/saveMessages` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| saveMessageRequestDTO | body | saveMessageRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## reattemptTask
> Request Payload:

```
{
  "messageTemplateId": 0,
  "organisationId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** reattemptTask

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/reattemptTask` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reattemptTaskRequestDTO | body | reattemptTaskRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


## inActiveNotifications
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** inActiveNotifications

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/inActiveNotifications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getReattemptTasks
> Request Payload:

```
{
  "organisationId": 0,
  "organisationType": "string",
  "roleId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getReattemptTasks

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getReattemptTasks` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| reattemptTaskRequestDTO | body | reattemptTaskRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getMessageApprovals
> Request Payload:

```
{
  "organisationId": 0,
  "organisationType": "string",
  "roleId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getMessageApprovals

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getMessageApprovals` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| messageApprovalRequestDTO | body | messageApprovalRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getMessageNotifications
 > Request Payload:

```
{
  "organisationId": 0,
  "organisationType": "string",
  "roleId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getMessageNotifications

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getMessageNotifications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| messageNotificationRequestDTO | body | messageNotificationRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getMessageActivity
> Request Payload:

```
{
  "organisationId": 0,
  "organisationType": "string",
  "roleId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getMessageActivity

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getMessageActivity` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| messageActivityRequestDTO | body | messageActivityRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getNotifications
> Request Payload:

```
{
  "organisationId": 0,
  "organisationType": "string",
  "roleId": 0,
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** getNotifications

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getBellNotifications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| messageNotificationRequestDTO | body | messageNotificationRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Tracking Controller

## getTripTracking
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getTripTracking

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getTripTracking` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getConsignmentStatusTracking
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getConsignmentStatusTracking

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getConsignmentStatusTracking` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| consignmentNumber | query | consignmentNumber | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |




# Account Resource controller
## getOrganisationList
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getOrganisationList

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getOrganisationList` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| getOrganisationListRequestDTO | body | getOrganisationListRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |





# Store Controller
## getStoreListing
> Request Payload:

```
{
  "endDate": "string",
  "organisationId": 0,
  "roleId": 0,
  "startDate": "string",
  "userId": 0
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getStoreListing

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/getStoreListing` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| consignmentListingRequestDTO | body | consignmentListingRequestDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |




# IE Integration Controller

## updateStatusAndNextState
> Request Payload:

```
{
  "eventName": "string",
  "json": "string",
  "loadId": "string"
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateStatusAndNextState

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateStatusAndNextState` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| statusUpdateDTO | body | statusUpdateDTO | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## getLoad
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getLoad

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/load` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| loadId | query | loadId | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |




# Master Setup Controller
## masterSetup
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** masterSetup

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/masterSetup` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| excelSheet | formData | excelSheet | Yes | file |
| type | query | type | Yes | string |
| userId | query | userId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Schedular Controller


## setScheduler
> Request Payload:

```
{
  "date": "string",
  "days": [
    0
  ],
  "jobKey": "string",
  "timeOfTheDay": "string"
}

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** setScheduler

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/scheduler/setScheduler` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| sourceFrequency | body | sourceFrequency | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |


# Mail Controller
## sendFeedbackMail
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```
**Summary:** sendFeedbackMail

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/sendFeedbackMail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| files | query |  | No | array |
| subject | query |  | No | string |
| content | query |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

## sendMail
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** sendMail

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/sendMail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| emailId | query | emailId | Yes | string |
| subject | query | subject | Yes | string |
| body | query | body | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |




































# Workbench Controller

## getWorkbenchRecordCount
 > Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getWorkbenchRecordCount

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/workbenchRecordCount` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| userId | query | userId | Yes | long |
| organisationId | query | organisationId | Yes | long |
| roleId | query | roleId | Yes | long |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |




<!-- Not on swagger -->

# getUserInfoByAuthorizationCode
 
 > Request Payload:

```

```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** getUserInfoByAuthorizationCode

### HTTP Request 
<text style="color:green;font-weight: bold;">GET-</text>` /api/getUserInfoByCode` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| code | query | code | Yes | string |
| redirectURI | query | redirectURI | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |

# updateStatusOnEventT
> Request Payload:

```


```
> Response Payload:

```


```

> Success response:

```


```

> Failure response:

```


```

**Summary:** updateStatusOnEvent

### HTTP Request 
<text style="color:green;font-weight: bold;">POST-</text>` /api/updateStatusOnEvent` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header |  | No | string |
| updateStatusOnEvent | body | updateStatusOnEvent | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 201 | Created |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
