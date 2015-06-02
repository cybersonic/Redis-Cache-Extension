##Lucee Redis Cache Extension

The redis driver is based on Jedis. While this is a very robust driver and Redis is amazni this project has to be considered in Beta stage.
Feel free to fork it and provide your feedbacks.

###Installation

Install the extension from the Lucee extension store in Lucee server Administrator. Please note that the extension can only be installed in the *server* admin.
This means that is not possible to install it for a single web context.

###Create and configure the cache

Create a new cache selecting Redis Cache as Type.

Add some configuration:

* If you like you can use the driver to store the Session Scope. If this is your intention you can flag "Allow to use this cache as client/session storage."
* Server/Host => says to the Lucee how to connect to Redis. By default this is settled to localhost:6379.
Please tune this following your environments needs. Note that the driver actually support a single Redis Server.
* Namespace => choose the namespace that will be used to avoid keys name clashing between different cache instances.

Well. You are done.

###Important

* *Metadata*:
    * The cache will return only the hits count for any single key.
    * The general counter (missed, hits) for the cache instance itself are not updated

* *idletime*:
  Not supported. Any passed value will be ignored. Timespan is fully supported.




