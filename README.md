## CRUD Operations Using REST API Principles

### 1. Register User(POST)

- **Endpoint**: `/user/register`
- **Method**: `POST`
- **Content-type**:`application/json`
- **Request Body**:

  ```json
  {
    "id": 123,
    "userName": "Ramprasad",
    "Email": "ramprasadboddu88@gmail.com"
  }
- **Response(200 OK)**:
  - **Validate (User Details)**:
    - **Request Sent Successfully:**

        ```json
          {
            "message": "User Details Added"
          }
    - **Error**:

      ```json
        {
          "error": "Check the Data"
        }
### 2. Getting User Details(GET)

- **Endpoint**: `/user?id=123`
- **Method**: `GET`
- **Response(200 OK)**:
 
    - **Response Received Successfully(201)**

         ```json
        {
            "id": 123,
            "userName": "Ramprasad",
            "Email": "ramprasadboddu88@gmail.com"
        }
    - **Error(404)**:
        ```json
        {
            "Error":"Data Not found"
        }

## 3. Update User Details(PUT)

- **Endpoint**: `/user?id=123`
- **Method**: `PUT`
- **Content-type**:`application/json`
    - **Request Body**:

        ```json
            {
                "userName": "RamprasadBoddu"
            }
     - **Response(200 OK)**:
  - **Update (User Details)**:
    - **User Details Successfully Updated:**

        ```json
          {
            "userName": "User Details Updated"
          }
    - **Error**:
      ```json
        {
          "error": "Check the Data"
        }
## 4. Delete User Details(DELETE)

- **Endpoint**: `/user?id=123`
- **Method**: `DELETE`
- **Content-type**:`application/json`
     - **Response(200 OK)**:
  - **Deleted (User Details)**:
    - **User Details Successfully Updated:**      
        ```json
          {
            "massage": "User Deleted Successfully"
          }
    - **Error**:
      ```json
        {
          "error": "data Not Found"
        }        

## 1.What is an API? and Benefits of API?
APIs are mechanisms that enable two software components to communicate with each other using a set of definitions and protocols. For example, the weather bureau’s software system contains daily weather data. The weather app on your phone “talks” to this system via APIs and shows you daily weather updates on your phone.

## 3.What are the different types of APIs?
APIs are classified both according to their architecture and scope of use. We have already explored the main types of API architectures so let’s take a look at the scope of use.
### Private APIs:
These are internal to an enterprise and only used for connecting systems and data within the business.
### Public APIs:
These are open to the public and may be used by anyone. There may or not be some authorization and cost associated with these types of APIs.
### Partner APIs:
These are only accessible by authorized external developers to aid business-to-business partnerships.

## 4.What are the difference between SOAP and REST?
| SOAP API| REST API |
| ----- | --- |
| Relies on SOAP (Simple Object Access Protocol) | Relies on REST (Representational State Transfer) architecture using HTTP. |
| Transports data in standard XML format. | Generally transports data in JSON. It is based on URI. Because REST follows stateless model, REST does not enforces message format as XML or JSON etc. |
| Because it is XML based and relies on SOAP, it works with WSDL|	It works with GET, POST, PUT, DELETE | 
Works over HTTP, HTTPS, SMTP, XMPP	| Works over HTTP and HTTPS | 

## 5.Methods in Soap and Rest
## 6.What is Webservice
#### A web service (WS) is either:
- A service offered by an electronic device to another electronic device, communicating with each other via the Internet, or
- A server running on a computer device, listening for requests at a particular port over a network, serving web documents (HTML, JSON, XML, images).

## 7.Types of Web services
#### 7.1 SOAP web service:

SOAP stands for Simple Object Access Protocol. It is a XML-based protocol for accessing web services.

- SOAP is a W3C recommendation for communication between two applications.
- SOAP is XML based protocol. It is platform independent and language independent. By using SOAP, you will be able to interact with other programming language applications.

#### Advantages of Soap Web Services

##### WS Security: 
- SOAP defines its own security known as WS Security.

##### Language and Platform independent: 
- SOAP web services can be written in any programming language and executed in any platform.

#### Disadvantages of Soap Web Services

##### Slow: 
- SOAP uses XML format that must be parsed to be read. It defines many standards that must be followed while developing the SOAP applications. So it is slow and consumes more bandwidth and resource.

##### WSDL dependent: 
- SOAP uses WSDL and doesn't have any other mechanism to discover the service.

#### 7.2 REST Webservice: 
REST stands for Representational State Transfer. REST defines a set of functions like GET, PUT, DELETE, etc. that clients can use to access server data. Clients and servers exchange data using HTTP.

The main feature of REST API is statelessness. Statelessness means that servers do not save client data between requests. Client requests to the server are similar to URLs you type in your browser to visit a website. The response from the server is plain data, without the typical graphical rendering of a web page.
## Advantages of REST API's
REST APIs offer four main benefits:

1. Integration 
2. Ease of Maintenance
3. Expansion

