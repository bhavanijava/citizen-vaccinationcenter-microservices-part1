# citizen-vaccinationcenter-microservices-part1
Citizen-Service
---------------
```bhavani
URL:-http://localhost:8001/citizen/add
http method: POST
```
Json Request:
```bhavani
{
    "name":"person-1",
    "vaccinationCenterId":2001
}
```
Json Response:
```bhavani
{
    "id": 61,
    "name": "person-1",
    "vaccinationCenterId": 2001
}
```
Vaccination-Center
------------------
```bhavani
URL:-http://localhost:8002/vaccinationCenter/add
http method: POST
```

Json Request:
```bhavani
{
    "id":2001,
    "centerName":"center-1",
    "centerAddress":"hyderabad"
}
```
Json Response:
```bhavani
{
    "id": 2001,
    "centerName": "center-1",
    "centerAddress": "hyderabad"
}
```
VaccinationCenter-Citizen-Details
---------------------------------
```bhavani
URL:-http://localhost:8002/vaccinationCenter/id/2001
http method: GET
```
Json Response:
```bhavani
{
    "center": {
        "id": 2001,
        "centerName": "center-1",
        "centerAddress": "hyderabad"
    },
    "citizens": [
        {
            "id": 61,
            "name": "person-1",
            "vaccinationCenterId": 2001
        }
    ]
}
```
About Application
------------------
In this application i created 2 microservices they are 1) citizen-service 2) vaccination-center-service after i register these two applications into eureka server and also created communation between citizen-service to vaccination-center-service microservices by using RestTemplate class.
#### Conclusion :-
Finally i perform some operations on these two microservices applications.
