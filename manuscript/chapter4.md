# Top Features You'll Want to Know About

As you start to use PhoneGap Build, you will realize that there are a wide variety of things that you can do with it. This section will teach you all about the most commonly performed tasks and most commonly used features in PhoneGap Build. 

## 1 – Git Deployment

We have talked about Git deployment in previous chapter. It is an alternative way to upload your HTML5 assets other than uploading .zip archive of your application. This is your only way to deploy open source application on PhoneGap Build. We have already knows that free account only allow us to have one private application and unlimited open source application. 















Importing native code can be done by adding `<gap:plugin>` to your `config.xml`. For example : 

	<gap:plugin name="com.phonegap.plugins.example" version="2.2.1" />

For plugins versioning, you can use the tilde `~` such as : 

	<gap:plugin name="com.phonegap.plugins.example" version="~2" />
it will load the latest 2.x version.
	
	<gap:plugin name="com.phonegap.plugins.example" version="~2.3" />
	
it will load the latest 2.x version as long as the x is greater or equal to 2

	<gap:plugin name="com.phonegap.plugins.example" version="~2.3.4" />
	
it will load the latest 2.3.x version as long as the x is greater or equal to 4.

#### Plugin Parameters
Some plugins may require additional information to work. This can be done by adding some childern to `<gap:plugin>` like this : 

	<gap:plugin name="com.phonegap.plugins.someplugin">
	  <param name="APIKey" value="myapikey" />
	  <param name="APISecret" value="myapikeyscret" />
	</gap:plugin>
	
#### Example : 
Here is an example to add Local Notification to your project : 

	<?xml version="1.0" encoding="UTF-8" ?>
	    <widget xmlns   = "http://www.w3.org/ns/widgets"
	    xmlns:gap   = "http://phonegap.com/ns/1.0"
	    id          = "com.phonegap.example"
	    versionCode = "10" 
	    version     = "1.0.0" >
	
	    <!-- versionCode is optional and Android only -->
	
	    <name>PhoneGap Example With Local Notification</name>
	
	    <description>
	      Your awesome application description 
	    </description>
	
	    <author href="https://build.phonegap.com" email="mail@domain.com">
	      Your Name 
	    </author>
	
	    <!-- We'll include the Local Notification plugin as an example -->
	    <gap:plugin name="de.appplant.cordova.plugin.local-notification" />
	</widget>

### 2 - Referencing the JavaScript code
Some plugins utilize the `js-module` element to make cordova load the plugin javascript. Then, no `<script>` refernces in your html is needed. But 3rd party plugin may need to add javascript manually. Please refer to plugin documentation. If you need to add it manually, you can add `<script>` reference like this : 

	<script src="cordova.js"></script>
	<script src="localnotification.js"></script>
	








