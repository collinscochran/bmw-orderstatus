bmw-tracker
===========

### About

I made this to track my BMW order. When node-red recieves a valid API request, the system logs into your MYBMW account via their auth api, downloads the contents of "my garage" and associated data, and returns that as a summary string showing your production info. I've only ever tried it on my account which has one car under order, I believe if you tried it with two, you'd get the first vehicle in the list. 

### Installation

 1. [Install node-red on platform of choice](https://nodered.org/docs/getting-started/local)
 2. [Clone project from this repo](https://nodered.org/docs/user-guide/projects/)
 3. Interface with the API using an apple shortcut or any other simple HTTP rest api client.

### API

The api only needs your username and password passed through `HTTP POST` headers, as `username` and `password`. I normally interface [using an Apple Shortcut](https://www.icloud.com/shortcuts/51df3115cede4393a9261c44715b216e) which adds those headers and makes the `HTTP POST` request

The api returns a text summary of the vehicle, order status, VIN, and date info was last refreshed.