# Display RSS Component
-------

This is a Web Component that uses [Polymer](http://www.polymer-project.org/) to create it and to provide a fallback in case the browser don't support web components.

It provides a component that fetches any RSS feed and displays it (with no style, you can customize that part).

Has a dependency on `polymer-jsonp.html` but that's installed with bower.

The component uses the Google Feed JSON Url to jsonp any feed.

You can find a working demo here: http://beldar.github.io/display-rss/

To know more about web components [there](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/) [are](http://www.html5rocks.com/en/tutorials/webcomponents/shadowdom/) [tons](http://css-tricks.com/modular-future-web-components/) of [resources](https://www.google.co.uk/search?q=web+components) available.


# Installation

Via Bower
--------

    bower install --save display-rss

Otherwise...

Dependencies
------------

You have to have installed [bower](http://bower.io/), and [compass](http://compass-style.org/install/). To install the first two you'll need [node](http://nodejs.org/) too.

Install
-------

Once you have all those and cloned the repo, go to the root of the project and run:

    bower install
    
That will download all the js and css dependencies of the project.

Then run:

    npm install
    
This will download all the node dependencies (including grunt)

Finally you can launch the demo running:

    grunt serve
    
You can build the project ready for production like this:

    grunt build
    
That will leave everything ready on the `/dist` folder

# How to use

There's an example/demo on the index.html of this project, but basically, you first need to include the platform.js:

    <script src="bower_components/platform/platform.js"></script>
    
Then, just below import the html of the element:

    <link rel="import" href="elements/display-rss.html">
  
And finally place the element where you want it using the attributes that you need:

    <display-rss></display-rss>

You can also define a url, number of entries or refresh time:

    <display-rss url="http://rss.news.yahoo.com/rss/topstories" entries="20" refresh="10000"></display-rss>
    
Attributes summary
-----------

| Attribute | Functionality                        | Default        |
|-----------|--------------------------------------|----------------|
| url  | Defines the url of the feed you want | BBC News feed         |
| entries | Defines how many entries you want displayed          | 10           |
| refresh | If different than 0 refreshes the feed every X milliseconds | 0 |
