# What I've Learned
Just a bit of what I've learned while working through this Auth0 test.

## Deeper knowledge of SAML
* Deployed Gluu Server on Digitalocean droplet and configured SAML IDP. https://saml.lamar.io
* Articles Read: http://wso2.com/library/articles/2014/02/introduction-to-security-assertion-markup-language-2.0/

## Better understanding of setting up Auth0

### From a developer's perspective
* Deployed Auth0 test applications on Digitalocean droplet - http://auth0-test.lamar.io:3000
* Tested logging in using various social accounts.
* Troubleshooted issues with information in Auth0 dashboard logs
* Python test application removing last character of .env file.
  * This resulted in a mismatch of callback URLs -- Auth0 looking for http://auth0-test.lamar.io:3000/callback -- Python App providing http://auth0-test.lamar.io:3000/callbac 
  * Couldn’t find root cause for removal of last character, this may be something standard that I’m just not aware of. 
  * Quick and dirty fix by adding a single “space” at the end of .env file. 

### From an Enterprise seeking SSO for 3rd-party apps perspective
* Connected deployed Gluu Server SAML IDP (Shibboleth 2) to Auth0.
* Authenticated SAML users to 3rd-party app SumoLogic.
