## Hello!

This is a proof-of-concept and work-in-progress web app created for myself and other DJs. Digital DJs have grown accustomed be being able to search and sort the music they own by tempo, key, playcount, etc, but this information is not publicly available for them on Spotify, where many of us listening to and discover new music. The goal of this project is to help DJs sort tracks on Spotify (and, perhaps, other playforms) with all available and relevant metadata to better fit it into their DJ sets or to save for purchase. 

I plan on launching a workable release by Spring 2020, with more ambitious plans down the road for spin-off project (meta data informed auto DJ!)

It is currently built on the official Spotify boilerplate authentication API. The instructions below are from Spotify and apply to the installation and operation of the basic app; operating the WIP app at this point requires some basic knowledge of JavaScript. 

---

## Spotify Accounts Authentication Examples

This project contains basic demos showing the different OAuth 2.0 flows for [authenticating against the Spotify Web API](https://developer.spotify.com/web-api/authorization-guide/).

These examples cover:

* Authorization Code flow
* Client Credentials flow
* Implicit Grant flow

## Installation

These examples run on Node.js. On [its website](http://www.nodejs.org/download/) you can find instructions on how to install it. You can also follow [this gist](https://gist.github.com/isaacs/579814) for a quick and easy way to install Node.js and npm.

Once installed, clone the repository and install its dependencies running:

    $ npm install

### Using your own credentials
You will need to register your app and get your own credentials from the Spotify for Developers Dashboard.

To do so, go to [your Spotify for Developers Dashboard](https://beta.developer.spotify.com/dashboard) and create your application. For the examples, we registered these Redirect URIs:

* http://localhost:8888 (needed for the implicit grant flow)
* http://localhost:8888/callback

Once you have created your app, replace the `client_id`, `redirect_uri` and `client_secret` in the examples with the ones you get from My Applications.

## Running the examples
In order to run the different examples, open the folder with the name of the flow you want to try out, and run its `app.js` file. For instance, to run the Authorization Code example do:

    $ cd authorization_code
    $ node app.js

Then, open `http://localhost:8888` in a browser.
