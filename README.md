# spring-boot-2.7-oauth2-adfs-resource-server
## Introduction
This code is about how to set up an ADFS (Active Directory Federation Services) server to work with a Spring Boot Resource Server using the Implicit Grant Flow. The Implicit Grant Flow is a OAuth 2.0 flow that is suitable for browser-based or mobile applications where the client-side JavaScript code can directly obtain an ID token from the identity provider, in this case, ADFS. We will focus on the first step of this process - setting up ADFS for this specific flow.

## Setting Up ADFS:
Let's assume that Active Directory and users are already set on your Active Directory server. Now we need to setting Application Group on AD FS by the following step:
1. Log in to your ADFS server and open the ADFS Management Console. On left menu under "Application Groups", right click and click "Add Application Group..."
2. When "Add Application Group Wizad" appear, select "Server application accessing a web API" and given some Name then click "Next".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-01-47.png)

3. On "Server application" step add Redirect URI for example "http://localhost:8080/info" and keep "Client Identifier" we will use it in later step. Click "Next".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-03-00.png)

4. On "Configure Application Credentials" step click check box "Generate a shared secret" and copy to txt somewhere, we will use it in later step. Then click "Next".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-03-09.png)

5. On "Configure Web API" step, put "http://localhost:8091/resource" to "Identifier" and click "Add".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-03-35.png)

6. On "Apply Access Control Policy" just select "Permit everyone".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-03-44.png)

7. On "Configure Application Permissions" make sure that under "Permitted scope" the "openid" check box is selected. Then click "Next".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-03-52.png)

8. On "Summary" step, just click "Next", then click "Close".

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-04-04.png)

![Screenshort1](images/Screenshot%20from%202023-09-26%2013-04-11.png)

## Request for token using ADFS Implicit Grant Flow:
x
x
x
## Request for token using Authorization code grant flow:
x
x
x
## Request for token using Resource owner password credentials grant flow (Not recommended):
x
x
x

