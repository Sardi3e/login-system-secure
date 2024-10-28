# login-system-secure
Login systems using PHP &amp; HTML
Introduction

Many web applications are a mix of public and private pages. Public pages are available to anyone, while a private page requires a user login. You can use authentication to manage which users have access to which pages. Your React application will need to handle situations where a user tries to access a private page before they are logged in, and you will need to save the login information once they have successfully authenticated.

In this tutorial, you’ll create a React application using a token-based authentication system. You’ll create a mock API that will return a user token, build a login page that will fetch the token, and check for authentication without rerouting a user. If a user is not authenticated, you’ll provide an opportunity for them to log in and then allow them to continue without navigating to a dedicated login page. As you build the application, you’ll explore different methods for storing tokens and will learn the security and experience trade-offs for each approach. This tutorial will focus on storing tokens in localStorage and sessionStorage.

By the end of this tutorial, you’ll be able to add authentication to a React application and integrate the login and token storage strategies into a complete user workflow.

Need to deploy a React project quickly? Check out DigitalOcean App Platform and deploy a React project directly from GitHub in minutes.
Prerequisites

    You will need a development environment running Node.js; this tutorial was tested on Node.js version 10.22.0 and npm version 6.14.6. To install this on macOS or Ubuntu 18.04, follow the steps in How to Install Node.js and Create a Local Development Environment on macOS or the Installing Using a PPA section of How To Install Node.js on Ubuntu 18.04.

    A React development environment set up with Create React App, with the non-essential boilerplate removed. To set this up, follow Step 1 — Creating an Empty Project of the How To Manage State on React Class Components tutorial. This tutorial will use auth-tutorial as the project name.

    You will be fetching data from APIs using React. You can learn about working with APIs in How To Call Web APIs with the useEffect Hook in React.

    You will also need a basic knowledge of JavaScript, HTML, and CSS, which you can find in our How To Build a Website With HTML series, How To Style HTML with CSS, and in How To Code in JavaScript.

Step 1 — Building a Login Page

In this step, you’ll create a login page for your application. You’ll start by installing React Router and creating components to represent a full application. Then you’ll render the login page on any route so that your users can login to the application without being redirected to a new page.

By the end of this step, you’ll have a basic application that will render a login page when a user is not logged into the application.

To begin, install react router with npm. There are two different versions: a web version and a native version for use with React Native. Install the web version:
