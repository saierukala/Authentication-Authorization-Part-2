## Authentication & Authorization | Part 2

# Authentication Flow in React
# Storing JWT Token
# Handling Login Failure
# Cookies
# Cookies.set()
# Cookies.get()
# Cookies.remove()
# Handling Route Redirections
# Unauthenticated Scenario
# Authenticated Scenario
# React Router
# withRouter

worked on header loginform and app.js
------------------------------------------------------------------------

// npm install js-cookie --save
// npm install react-router-dom@5.2.0

------------------------------------------------------------------------

 # JWT Token
JSON Web Token is a standard used to create Access Tokens. These access tokens are also called JWT Tokens.

The client uses these access tokens on every subsequent request to communicate with the Server.

## Storing JWT Token in State

When we store the JWT Token in the state,

On page refresh, the JWT token won't be available
It is difficult to pass state information to every component

## Storage Mechanisms

* Client-Side Data Storage
* Storing Data on the Client
* Server-Side Data Storage
* Storing Data on the Server using some kind of Database
* Different types of Client-Side data storage mechanisms are:

Local Storage
Cookies
Session Storage
IndexedDB, etc.

# . Cookies
A cookie is a piece of data that is stored on the user's computer by the web browser.

# A cookie is made up of:

Name & Value
* Expires − The date the cookie will expire. If this is blank, the cookie will expire when the visitor quits the browser.

* Domain − The domain name of your site.

* Path − The path to the directory or web page that set the cookie. This may be blank if you want to retrieve the cookie from any directory or page.

* Secure − If this field contains the word "secure", then the cookie may only be retrieved with a secure server. If this field is blank, no such restriction exists, etc.

##  Why Cookies?
With cookies, we can set the expiry duration.

Examples:

Banking Applications - Cookies get expired in minutes
Facebook - Cookies get expired in months or years
------------------------------------------------------------------------

## Cookies 

* We can set an expiration for Cookies
* Cookies can store up to 4KB of data

## vs Local Storage

* Local storage data never expires
* Local Storage can store up to 5 to 10 MB of data
------------------------------------------------------------------------

##  Third Party Package - js-cookie
JavaScript can read, create, modify, and delete the cookies.

NPM contains a js-cookie, a third-party package to manipulate cookies easily.

# Installation Command:
npm install js-cookie --save

# js-cookie methods are:

* Cookies.set()- It is used to set the cookie
* Cookies.get()- It is used to get the cookie
* Cookies.remove()- It is used to remove the cookie

# Cookies.set()

* Cookies.set('CookieName', 'CookieValue', {expires: DAYS});

# Example:

* Cookies.set('ACCESS_TOKEN', 'Us1L90PXl...', {expires: 1});
------------------------------------------------------------------------

# 2 Cookies.get()

* It returns undefined if the cookie expires or does not exist.

 Cookies.get('CookieName');

 # Example:

 * Cookies.get('ACCESS_TOKEN');
 -----------------------------------------------------------------------

 ## 4. Redirect Component

 * The react-router-dom provides the Redirect component. It can be used whenever we want to redirect to another path.

 # Syntax:

 * <Redirect to="PATH" />

 # Example:

 * <Redirect to="/login" />
 -----------------------------------------------------------------------

 ## Redirect Component vs history Methods

* Use the Redirect Component when you have to stop displaying UI and navigate to a route. Ex: Inside Class Component - render()

* In all other cases, use history.push() or history.replace() syntax Ex: onSubmit, onClick event callback functions
 
 -----------------------------------------------------------------------

 ## . withRouter
The history prop will be available for only components which are directly given for Route.

To provide history prop to other components, we can wrap it with the withRouter function while exporting it.

## Example:

import { withRouter} from 'react-router-dom'
...
export default withRouter(ComponentName)
------------------------------------------------------------------------

## 6. E-Commerce Application
Make an Authentication Request to Login API
Handle Login API Response
On Login Success
On Login Failure
Store the JWT Token
------------------------------------------------------------------------

## Publish

# https://Sailoginout.ccbp.tech

