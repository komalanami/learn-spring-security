### When creating a project with only the Spring Security and Spring Web dependencies

By default, Spring Security enables basic form login and HTTP Basic authentication.
A default user is created, and a generated password is displayed in the console when the application starts.

### Exploring Form Based Authentication
1. Used by most web applications.
2. Provides a default login page.
3. Users are redirected to a login page when they try to access a protected resource.
4. After successful login, users are redirected to the originally requested resource.
5. Uses a Session Cookie 
 - JSessionID:
   - A session is created when a user logs in.
   - The session is stored on the server, and the session ID is sent to the client as a cookie. 
   - The session ID is used to identify the user in subsequent requests. 
   - The session is invalidated when the user logs out or the session expires.
6. User can log out by clicking a logout link(/logout), which invalidates the session and redirects to the login page.


### Exploring Basic Authentication
1. Most Basic options to secure a REST API.
  - BUT Has many flaws
  - Credentials are sent in the HTTP header with every request.
  - Credentials are Base64 encoded, not encrypted.
  - Not suitable for production use.
2. Base 64 encoded credentials are sent in the HTTP header with every request.
  - Authorization: Basic <base64 encoded credentials>
