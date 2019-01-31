# Miscellaneous Config Files
This is a small repo where I can put things related to my practice in Wordpress Dev work, generally miscellaneous config files that I'll need for work in other repos. What you can find here so far:

## Docker Compose YML Files
For my code demos, I'm using a few different Docker Compose yml files.

* wp-docker-compose.yml: This one sets up the Wordpress, MySQL, and PHPMyAdmin containers.
* sel-docker-compose.yml: This one sets up a Selenium grid with one Firefox node and one Chrome node.
* wp-sel-docker-compose.yml: This is a combined version of the previous two files.

### Dependencies
The sel-docker-compose.yml file explicitly assigns its containers to the wp-net network I set up in wp-docker-compose.yml. So if you want to use the two separate files (as opposed to the wp-sel version), use docker-compose to launch the wp yaml first. Then launch the sel yaml. Note that you may see warnings about orphan containers this way, but as near as I can tell you can disregard those warnings.

## Postman Files

These two Postman files are useful for doublechecking the tests run in my wp-test-demo-java repo. Both of these files assume I am running the local Wordpress instance in that demo, which is set up to use the URL wordpress.local.

* wp-test-demo.postman_collection.json: This is a Postman collection containing various service endpoints for Wordpress as defined in the Wordpress REST API docs.
* wp-local.postman_environment.json: This is a Postman Environment to go with the collection above. It holds the current values I'm using for testing purposes to plug into the URLs.
