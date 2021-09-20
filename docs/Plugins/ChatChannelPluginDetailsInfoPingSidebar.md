# Zuri Chat Channel Plugin Resource 
This resource contains several endpoints 

Zuri Chat is an open source slack clone. However, it offers a lot more functionality via a plugin system where each room can be provided by a different plugin provider.
```
Base URL: https://channels.zuri.chat
```
## Details Endpoint

### Endpoint path
```
Get https://channels.zuri.chat/api/v1/details
```
### Content-Type
The content type is set by default, application/json is the supported content-type.

### Status Codes 
The HTTPS secured protocol is used in communicating securely with the server, an example can be seen in the curl url

```
curl -X GET "https://channels.zuri.chat/api/v1/details/" -H  "accept: application/json" -H  "X-CSRFToken: X8PITa8QHmEY3IaYFvSOhailGivVReQtkXCH06OMcxIG7GMMl2eRXj4nZ7ZNfRwq"
```
#### Request URL 

```
https://channels.zuri.chat/api/v1/details/
```

#### Server Responses

**200 
Response Description: success**
```
Response body
{
  "message": "Welcome, to the Channels Plugin",
  "last_visted": "2021-09-17T14:47:46.401787+00:00",
  "no_of_times_visted": 33
}
```
#### Response Headers
```
access-control-allow-origin: *
allow: GET,HEAD,OPTIONS
connection: keep-alive
content-language: en
content-length: 118
content-type: application/json
date: Fri,17 Sep 2021 14:47:46 GMT
referrer-policy: same-origin
server: nginx/1.18.0 (Ubuntu)
strict-transport-security: max-age=60; includeSubDomains; preload
vary: Accept,Accept-Language,Origin
x-content-type-options: nosniff
x-frame-options: DENY
x-xss-protection: 1; mode=block
```

#### Request duration
This is the average duration of all underlying requests made to the server, and when a response was given in ms(millisecond).
Example
```
966 ms
```
## Info Endpoint

### Content-Type
The content type is set by default, application/json is the supported content-type.

### Status Codes 
The HTTPS secured protocol is used in communicating securely with the server, an example can be seen in the curl url
```
curl -X GET "https://channels.zuri.chat/api/v1/info/" -H  "accept: application/json" -H  "X-CSRFToken: X8PITa8QHmEY3IaYFvSOhailGivVReQtkXCH06OMcxIG7GMMl2eRXj4nZ7ZNfRwq"
```

#### Request URL 
```
https://channels.zuri.chat/api/v1/info/
```


### Server Responses

**200**
Response Description: success


#### Response body
```
{
  "message": "Plugin Information Retrieved",
  "data": {
    "type": "Plugin Information",
    "plugin_info": {
      "name": "Channels Plugin",
      "description": [
        "Zuri.chat plugin",
        "The Channel Plugin is a feature    that helps users create spaces for    conversation and communication on zuri.chat."
      ]
    },
    "scaffold_structure": "Monolith",
    "team": "HNG 8.0/Team Coelho",
    "sidebar_url": "https://channels.zuri.chat/api/v1/sidebar/",
    "ping_url": "https://channels.zuri.chat/api/v1/ping/",
    "homepage_url": "https://channels.zuri.chat/"
  },
  "success": true
}
```
##### Response Headers

```
access-control-allow-origin: *
allow: GET,HEAD,OPTIONS
connection: keep-alive
content-language: en
content-length: 508
content-type: application/json
date: Fri,17 Sep 2021 14:52:52 GMT
referrer-policy: same-origin
server: nginx/1.18.0 (Ubuntu)
strict-transport-security: max-age=60; includeSubDomains; preload
vary: Accept,Accept-Language,Origin
x-content-type-options: nosniff
x-frame-options: DENY
x-xss-protection: 1; mode=block
```
##### Request duration

Request Duration shows the time in ms (milliseconds) for a request to be executed.



## Ping Endpoint

### Content-Type
The content type is set by default, application/json is the supported content-type.

### Status Codes 
It uses the HTTPS secured protocol in communicating  securely with the server
An example can be seen in the curl url

```
curl -X GET "https://channels.zuri.chat/api/v1/ping/" -H  "accept: application/json" -H  "X-CSRFToken: X8PITa8QHmEY3IaYFvSOhailGivVReQtkXCH06OMcxIG7GMMl2eRXj4nZ7ZNfRwq"
```

### Request URL 
```
https://channels.zuri.chat/api/v1/ping/
```

### Server Responses

**Example**
```
200
Response Description: success
```

#### Response body
```
{
  "success": true
}
```


#### Response Headers
```
access-control-allow-origin: *
allow: GET,HEAD,OPTIONS
connection: keep-alive
content-language: en
content-length: 16
content-type: application/json
date: Fri,17 Sep 2021 14:57:33 GMT
referrer-policy: same-origin
server: nginx/1.18.0 (Ubuntu)
strict-transport-security: max-age=60; includeSubDomains; preload
vary: Accept,Accept-Language,Origin
x-content-type-options: nosniff
x-frame-options: DENY
x-xss-protection: 1; mode=block
```

#### Request duration

Request Duration shows the time in ms (milliseconds) for a request to be executed.


## Sidebar Endpoint

### Content-Type
The content type is set by default, application/json is the supported content-type.

### Parameters

|  |  |  |   | 
| ----------- | ----------- | ----------- | ----------- | 
| Name | Description | Data Type| Options|
| user| User ID| String| required|
| org | Organization ID| String| required|
| token | Token|String| required|
|  |  |  |
**Example**
using the example below a user_id = buju, org_id = 1, token = 1
will generate the server reponse below
|  |  |  
| ----------- | ----------- |
| Name | Description |
| user_id | buju|
| org_id | 1 |
| token | 1 |
|  |  |  |



**Curl**
```
curl -X GET "https://channels.zuri.chat/api/v1/sidebar/?org=buju&user=1&token=1" -H  "accept: application/json" -H  "X-CSRFToken: 2dUfHIqx8Bv86ODiWdNE9PmERKyRwDSnp2HeOE6tDMzQaMf6CK9HPY8Gaz2JUgyk"
```

**Request URL** 
```
https://channels.zuri.chat/api/v1/sidebar/?org=buju&user=1&token=1
```

### Server Responses

**200
Response Description: success**


#### Response body
```
{
  "name": "Channels Plugin",
  "description": "The Channel Plugin is a feature    that helps users create spaces for    conversation and communication on zuri.chat.",
  "plugin_id": "613654ede2358b02686503bb",
  "organisation_id": "buju",
  "user_id": "1",
  "group_name": "Zuri",
  "show_group": false,
  "joined_rooms": [],
  "public_rooms": []
}
```


#### Response Headers

a access-control-allow-origin: * 
 allow: GET,HEAD,OPTIONS 
 connection: keep-alive 
 content-language: en 
 content-length: 313 
 content-type: application/json 
 date: Fri,17 Sep 2021 16:34:29 GMT 
 referrer-policy: same-origin 
 server: nginx/1.18.0 (Ubuntu) 
 strict-transport-security: max-age=60; includeSubDomains; preload 
 vary: Accept,Accept-Language,Origin 
 x-content-type-options: nosniff 
 x-frame-options: DENY 
 x-xss-protection: 1; mode=block 


#####  Request duration

This is the average duration of all underlying requests made to the server, and when a response was given in ms(millisecond).









