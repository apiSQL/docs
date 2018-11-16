# docs
Doumentation, Tutorial, Information, Comparasion to another tools

## Why apiSQL
This is tool, which is the first step to reach in practical some parts of goals for UnitApi which will be later the main standard to build any API

# apiSQL
This tools is able to create meta data from SQL statement and SQL schema
The way from SQL to API is possbile with one step, just for configuration


## import-export generator
apisql.yaml


    version: 1.1.0
      name: Import data from localhost application  
      import:
        file:
        dump:
        db:
          host:
          password          
      export:
        file:
      

## Input
The sql file


## Output
The Code, sdk


## Parsing, Structure of schema

Source
    Collection
        Object
            Param
       
Collection
    List: 1,2,9,11
    Range: 1-11, A-M 
    Filter:
        Object,Param

Object:
    Create
    Read
    Update
    Delete
    
Param
    Get
    Set

### Routing, Example

Model: User
Structure:
User:
    id
    login
    password
    created_at

#### Routing
{Param}  = id
{items} = 1,2,3

https://domain/{source}/User/Collection/List/{Param}/{items}
https://domain/{source}/User/Collection/Range/{Param}/{items}
https://domain/{source}/User/Object/Update/{Param}/{items}

Pattern:
https://domain/{source}/{model}/param/get/{param}/{name}/

Example:
https://domain/source/{source}/model/{model}/param/{param}/get/id/10/
#### Get Login
https://domain/source/db/model/user/param/login/get/id/10/

#### Set Password
https://domain/source/db/model/user/param/password/set/id/10/





## Functionality
+ Create metada from SQL schema
+ Create REST API based on SWAGGER From Metadata
+ Generate sdk for SWAGGER API

