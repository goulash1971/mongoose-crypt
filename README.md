mongoose-crypt - Plugin support for basic encryption in Mongoose
==============

### Overview

Mongoose-Crypt is an extension for Mongoose that implements basic encryption support for fields in the 
Mongoose ORM.  

### Installation
	npm install mongoose-crypt

### Setup
To install all of the types, plugins, patches and utilities provided by the extension into a Mongoose 
instance:

	var mongoose = require("mongoose");
	   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");
	
	// Access the mongoose-crypt module and install everything
	var crypt = require("mongoose-crypt");
	var utils = crypt.utils
	
	// Install the types, plugins and monkey patches
	var loaded = crypt.install(mongoose);

The `loaded` value returned contains 2 properties:

- `loaded.types` : the join types that were loaded
- `loaded.plugins` : the extension plugins that were loaded

To just install the types provided by the extension (either all types or a list of named types):

	var mongoose = require("mongoose");
   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");

	// Access the mongoose-crypt module
	var crypt = require("mongoose-crypt");
	var utils = crypt.utils
	
	// Install the plugins
	var loaded = crypt.loadTypes(mongoose);

The `loaded` value returned contains the types that were loaded, keyed by the name of each type 
loaded.

To just install the plugins provided by the extension (either all plugins or list of named plugins):

	var mongoose = require("mongoose");
	   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");
	
	// Access the mongoose-crypt module
	var crypt = require("mongoose-crypt");
	var utils = crypt.utils
	
	// Install the plugins
	var loaded = crypt.installPlugins(mongoose);

The `loaded` value returned contains the plugins that were loaded, keyed by the name of each plugin 
loaded.

To just install the patches provided by the extension (either all patches or list of named patches):

	var mongoose = require("mongoose");
	   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");
	
	// Access the mongoose-crypt module and the utilities
	var crypt = require("mongoose-crypt");
	var utils = crypt.utils;
	
	// Install the monkey patches
	crypt.installPatches(mongoose);

### Contributors
- [Stuart Hudson](https://github.com/goulash1971)

### License
MIT License

### Acknowledgements
- [Brian Noguchi](https://github.com/bnoguchi) for the 'mongoose-types' extension that was used as a template for this extension

---
### Author
Stuart Hudson		 
