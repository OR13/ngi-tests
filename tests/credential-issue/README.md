# How to run tests manually

This document describes how to run the issuer tests by hand.

## Prerequisites

Before getting started, you must ensure that you have the appropriate software installed locally. Installation of these items is beyond the scope of this document, but instructions can be found for your operating system at the following link:

* Download and install [Postman](https://www.postman.com/).

## Import the required resources to Postman

The following elements need to be imported to Postman before you can run the tests.

* collection with test cases
    Import **NG-auth-flow.postman_collection.json** file to Postman collections

    <img src="./resources/import-collection-button.png"/>

* global environment variables
    Import **ngi.postman_globals.json** global variables (it contain external library - pmlib_code - to sign/verify JWT as one of variable)

* remote environment variables

    Import **research remote.postman_environment.json** remote environment variables. It contain properties which point to *research* environment
    
    <img src="./resources/import-envs.png"/>

    Editing **remote.postman_environment.json** file allows to set endpoints for:
    * get pre_auth code - pre_auth_endpoint
    * get access token (authentication server) - token_endpoint
    * get VC (issuer - resource server) - resource_endpoint and issuer_uri
  
    In **remote.postman_environment.json** configuration file also following variables need to be set/updated:
    * user - user name used as user_id in get pre_auth code request 
    * type - type of credential to obtain in get VC request

## Run the tests manually

Before you run the tests make sure that your proper environment variables set is selected.
<img src="./resources/select-env.png"/>

To run the tests for the *NGI auth flow* collection:
 <img src="./resources/open-test-window.png"/>
