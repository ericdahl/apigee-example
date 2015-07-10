# apigee-example
Sample project showing how to organize Apigee policy configuration and limit duplication

This project contains two proxies which share some common policies:
- weather: the standard apigee example, using Yahoo's weather API
- httpbin: a simple proxy for http://httpbin.org/ (which can be used for debugging)

Policies which are common to each proxy are held in common/ and the 
[proxy-dependency-maven-plugin](https://github.com/apigee/proxy-dependency-maven-plugin) is 
used to copy them as needed.

### Usage quick start

#### Obtain Apigee account

Sign up at http://enterprise.apigee.com/

#### Clone this repo

```
git clone git@github.com:ericdahl/apigee-example.git
```

#### Deploy

```
mvn clean install -Ptest -Dusername=$USERNAME -Dorg=$ORG -Dpassword=$PASSWORD
```
replacing the variables with your own account information.
