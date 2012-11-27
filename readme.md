# StatusLights
## What is it?
A helper for changing bland and boring 'Live' or 'Deleted' text in admin index views into something more visually appealing.  

## Requirements
The styles are based on the [Twitter Bootstrap labels](http://twitter.github.com/bootstrap/components.html#labels-badges) so you'll need to include this somewhere on your page, or you can [include the labels `.less` file](https://github.com/twitter/bootstrap/blob/master/less/labels-badges.less).

You'll need to be running [CakePHP](http://www.cakephp.org/) `v2.x`

## Installation
### Get the code
**Submodule**  
`git submodule add git://github.com/davidyell/CakePHP-StatusLights.git app/Plugin/StatusLights`  

**Clone**  
`git clone git://github.com/davidyell/CakePHP-StatusLights.git app/Plugin/StatusLights`  

**Download**  
Download an archive version from here, and unzip into `app/Plugin/StatusLights`  

### Include the helper
In your `app/Config/bootstrap.php` you'll need to load the plugin.  `CakePlugin::load('StatusLights');` unless you are already using `CakePlugin::loadAll();`  

Next you need to include the helper in your controller.  

	class DavidsController extends AppController{
    	public $helpers = array('StatusLights.StatusLights');
	}

To use the helper in your views you need to call `$this->StatusLights->status()` and pass in your `status_id`. As this is a basic helper, you might want to customise the helper to use your own id's.

