# sparta-SDET-integration_testing-SOM

## Main
After practising Unit Testing with the [FizzBuzz challenge](https://github.com/coding-sue-true/sparta-SDET-unit_testing-fizzbuzz), we moved into Integration Testing.
This implied getting data from an open API (Application Performance Interface). The API used for this repository can be accessed [here](https://api.postcodes.io).

For this exercise we used Ruby language.

### What is Integration Testing?
After performing Unit Tests, where small pieces of code are written and tested against requirements, we move onto Integration Testing where, in this case, our code was tested against the data from the API.

According with ISTQB Glossary, Integration Testing is:

> Testing performed to expose defects in the interfaces and in the interactions between integrated components or systems.
>http://glossary.istqb.org/search/integration%20testing

_Please note that Component (and Module) is another term used for Unit Testing_

In order to get data from the API we had to use the HTTParty module that enables us to define the _base uri_ of the API (the url link), _GET_ that data, and _Parse_ that data into .JSON, .XML, .YML format.

To run the tests we used the RSpec gem.

### What is SOM, Service Object Model?
We've been using Ruby, which is an Object-Oriented language. The good thing of OOP languages (Object-Oriented Programming), is that is allow us to organise and structure our software more easily, and reuse it or inherit it in another file or even software.
This is achieved with the use of Classes.

As you can see in the example bellow (which is a screenshot of the code from this repo), inside the _lib_ folder, we have a file named _postcode.rb_, which is where we have stored our super class of Post Codes (namely Single and Multiple).
With Service Object Model, each class corresponds to a different service.
For example, in the _services_ folder, we can find a Service for _SinglePostCode_, and another Service for _MultiplePostCodes_.
This allow us to specifically perform certain tests for a specific service and access or reuse it later.

![SOM](/images/som.png)


## How To Test
- Git clone this repository
- On your console move into the folder where this repository is cloned.
- Run bundle to make sure you have all the required gems installed. You need to have the following gems:
  - HTTParty gem
  - json gem

```
bundle
```
If you don't have one or more, on your console, run the following, and **run bundle again**:
```
gem install httparty
gem install json
gem install rspec
bundle
```
- Run 'rspec' to run the code
```
  rspec
```
- Something like the following should be displayed in your console:

![MultiplePostCodes](/images/multiple_pc.png)
![SinglePostCode](/images/single_pc.png)

## Documentation
- http://istqbexamcertification.com/
- https://github.com/rspec/rspec
- https://rubygems.org
- https://www.ruby-lang.org/en/documentation/
- https://github.com/jnunemaker/httparty
- http://ruby-doc.org/stdlib-2.0.0/libdoc/json/rdoc/JSON.html
