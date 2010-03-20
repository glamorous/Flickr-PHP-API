# Flickr PHP API #

## Why this class ##

I was searching for a good PHP5 class, one without PHP4 support. One that use cURL for the REST-API from [Flickr](http://flickr.com).
With this API I wanted to give users the chance to decide in wich format they want their results and support some basic methods and
the more advanced are possible with the custom query.

## How to use ##

### Setting API-key and default return format ###

    <?php
	    include('flickr.php');
	    
	    // set the API-key
	    Flickr::setApikey('API-key'); // change 'API-key' with yours
	    
	    // set the default return format
	    // default is set to Flickr::JSON
	    Flickr::setFormat(Flickr::PHP); // Flickr::PHP is a format for returning a serialized array
	    
	    $params = array(
	       'method' => 'flickr.test.echo',
	       'foo' => 'bar',
	    );
	    
	    $flickr_results = Flickr::makeCall($params);
	?>
	
### Setting it all together in one request ###

    <?php
	    include('flickr.php');
	    
	    $params = array(
	       'api_key' => 'API-key',
	       'format' => Flickr::XML,
	       'method' => 'flickr.test.echo',
	       'foo' => 'bar',
	    );
	    
	    $flickr_results = Flickr::makeCall($params);
	?>

## Issues/Bugs ##

If you find one, please inform us with the issue tracker on [github](http://github.com/glamorous/Flickr-PHP-API/issues).

## Changelog ##

**Flickr 0.5 - 20/03/2010**

- Initial version of the PHP-wrapper  

## Feature Requests / To come ##

If you want something to add on this plugin, feel free to fork the project on [github](http://github.com/glamorous/Flickr-PHP-API) or add an [issue](http://github.com/glamorous/Flickr-PHP-API/issues) as a feature request.

## License ##

This plugin has a [BSD License](http://www.opensource.org/licenses/bsd-license.php). You can find the license in license.txt that is included with class-package