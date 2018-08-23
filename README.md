# PayMaya External API Tester (PET)

Description 
  
	* The PET consists of two individual parts that emulate how an on-boarded partner will interact and make 
	requests to the PayMaya External API. These two parts are the server, and the client.
	
How to Use the PET
    
	* The Server

		* Before starting the server, ensure that the following are installed:

			* node

			* express

			* body-parser

			* path

			* xmlhttprequest

			* base-64

			* nodemon (optional)

		* Once all the requirements are installed, replace the client_id and the client_secret found in the server file.

		* This will allow the server to start making requests to the External API's endpoints.

		* Once the credentials are entered, the server is now ready to be run with node.

	* The Client

		* To access the functionality of the PET, an access token will first need to be acquired.

		* To do this, press the Authenticate button and login to the desired account.

		* Once logged in, the page will be redirected to the specified redirect uri and the features of the PET will now accessible.

Getting Started Guide for implementing the External API for other projects.

	* Step 1 : Authentication
    
		* From the PayMaya-Connect documentation, please follow the first step of the  Authorization Code Grant section. This step is where the authentication code will be retrieved, which is required to request for an access token.

			* Without the Authorization Code returned at the end of this step, the access token cannot be retrieved.
      
		* Following the second step of the aforementioned section will provide the user with the necessary tokens to make requests to the endpoints of the external API (provided that the endpoints are under the requested scopes).

			* Note: Although not explicitly stated in this section of the documentation, the request requires an Authorization header containing a base64 encoding of the client id and client secret.
      
			* Once the access token is retrieved the API's endpoints can now be accessed.
      
	* Step 2 : Making requests to the endpoints
  
		* To access the endpoints ensure that the proper authentication type, request bodies and headers, are followed for each individual endpoint.
    
			* If specific endpoints are inaccessible or are returning errors, please check that these endpoints are covered by the requested scopes during integration.
