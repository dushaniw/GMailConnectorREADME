# Ballerina GMail Endpoint

[Gmail](https://www.google.com/gmail/) is a free, Web-based e-mail service provided by Google.
### Why would you use a Ballerina endpoint for Gmail

Ballerina GMail endpoint allows you to access the [Gmail REST API](https://developers.google.com/gmail/api/v1/reference/) and perfom actions like creating and sending a simple text mail, mail
with html content and inline images, mail with attachments, search and get mail etc.

## Compatibility
| Language Version                             | Endpoint Version           |
| ---------------------------------------------|:--------------------------:|
| ballerina-tools-0.970.0-alpha6-SNAPSHOT      | 0.8.5                      | 

### Getting started

* Import the package to your ballerina project.
```
import wso2/gmail;
```
This will download the Gmail artifacts from the central repository to your local repository.

##### Prerequisites
1. Download the ballerina [distribution](https://ballerinalang.org/downloads/).

2. Go through the following steps to obtain access token and refresh token for Gmail

* First, create an application to connect with Gmail API
* For that, visit Google APIs console (https://console.developers.google.com/) to create a project and create an app for the project
* After creating the project, configure the OAuth consent screen under Credentials and give a product name to shown to users.
* Then create OAuth client ID credentials. (Select webapplication -> create and give a name and a redirect URI(Get the code to request an accessToken call to Gmail API) -> create)

    (Give the redirect URI as (https://developers.google.com/oauthplayground), if you are using OAuth2 playground to obtain access token and refresh token )
* Visit OAuth 2.0 Playground (https://developers.google.com/oauthplayground/), select the needed api scopes and give the obtained client id and client secret and obtain the refresh token and access token 

* So to use GMail endpoint, you need to provide the following:
    * Client Id
    * Client Secret
    * Access Token
    * Refresh Token
    
* Please note that ClientId, Client Secret, Refresh Token are optional if you are using Access Token only.
* Similarly, please note that access token is optional if you are using ClientId, Client Secret and Refresh Token.

### References

> Visit the [package-gmail](https://github.com/wso2-ballerina/package-gmail) repository for the source code.
> Visit the [test.bal](https://github.com/wso2-ballerina/package-gmail/blob/master/gmail/tests/test.bal) file
for the sample test cases.
