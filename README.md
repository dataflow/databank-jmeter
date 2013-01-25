Jmeter test results for Databank    
It also includes Jmeter test results for  in comparison to Fedora

Visit https://github.com/futures/ff-jmeter-madness for details on setting up jmeter and the data used (gov docs were used for these tests)
Jmx file: https://github.com/futures/ff-jmeter-madness/blob/3973031877090f64f0356b205a91d123ae146868/FuturesJmeterAggregation.jmx

Databank and Fedora were throwing 404 for object deletion . To avoid this,    
Fedora - Need to run the test a 2nd time    
Databank - Need to disable test purge at beginning of test

In terms of the numbers obtained, in a nutshell    
  The mean creation time for Fedora is 80ms    
  The mean creation time for Databank is 110ms

  The mean upload time for Fedora is 80ms    
  The mean upload time for Databank is 193ms

  The mean deletion time for Fedora is 15ms    
  The mean deletion time for Databank is 62ms

It would be worth to note here that these test were performed on the Pylons version of Databank, where we have identified issues 
mainly with file uploads and permission handling of the web framework (as seen in the file upload and delete times). We have started on the migration of databank from the Pylons web framework to the Django web framework. The enhanced databank is underway and is not yet ready for running these jmeter tests.

