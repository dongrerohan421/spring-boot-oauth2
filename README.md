Spring Boot and OAuth2

This guide shows you how to build a sample app doing various things with "social login" using OAuth2 and Spring Boot. It starts with a simple, single-provider single-sign on, and works up to a self-hosted OAuth2 Authorization Server with a choice of authentication providers (Facebook or Github). The samples are all single-page apps using Spring Boot and Spring OAuth on the back end. They also all use plain jQuery on the front end, but the changes needed to convert to a different JavaScript framework or to use server side rendering would be minimal.

Because one of the samples is a full OAuth2 Authorization Server we have used the shim JAR which supports bridging from Spring Boot 2.0 to the old Spring Security OAuth2 library. The simpler samples could also be implemented using the native OAuth2 support in Spring Boot security features. The configuration is very similar.

There are several samples building on each other adding new features:

    simple: a very basic static app with just a home page and unconditional login through via Spring Boot’s @EnableOAuth2Sso (if you visit the home page you will be automatically redirected to Facebook).

    click: adds an explicit link that the user has to click to login.

    logout: adds a logout link as well for authenticated users.

    manual: shows how the @EnableOAuth2Sso works by unpicking it and configuring all its pieces manually.

    github: adds a second login provider in Github, so the user can choose on the home page which one to use.

    auth-server: turns the app into a fully-fledged OAuth2 Authorization Server, able to issue its own tokens, but still using the external OAuth2 providers for authentication.

    custom-error: adds an error message for unauthenticated users, and a custom authentication based on Github API.

