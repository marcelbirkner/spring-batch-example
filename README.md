<h2>Configuration</h2>

Run the Batch Job: 

  	gradle clean run -Pargs="applicationContext.xml customerJob"

Example result: 
   
	2013-02-23 16:34:09,076  INFO   FeedReader:37 - reading data from feed ...
	2013-02-23 16:34:09,077  INFO   FeedReader:37 - reading data from feed ...
	2013-02-23 16:34:09,081  INFO   FeedReader:37 - reading data from feed ...
	2013-02-23 16:34:09,081  INFO   DatabaseWriter:23 - writing data to database
	2013-02-23 16:34:09,082  INFO   DatabaseWriter:25 - -> Customer 19 :: de.mb.batch.model.Customer@4b2922f6[customerId=19,firstName=John,lastName=Doe]
	2013-02-23 16:34:09,082  INFO   DatabaseWriter:25 - -> Customer 41 :: de.mb.batch.model.Customer@79b66b06[customerId=41,firstName=John,lastName=Doe]
	2013-02-23 16:34:09,082  INFO   DatabaseWriter:25 - -> Customer 4 :: de.mb.batch.model.Customer@372c9557[customerId=4,firstName=John,lastName=Doe]
	2013-02-23 16:34:09,089  INFO   FeedReader:37 - reading data from feed ...
	2013-02-23 16:34:09,089  INFO   FeedReader:37 - reading data from feed ...
	2013-02-23 16:34:09,089  INFO   FeedReader:37 - reading data from feed ...
	2013-02-23 16:34:09,089  INFO   DatabaseWriter:23 - writing data to database
	2013-02-23 16:34:09,090  INFO   DatabaseWriter:25 - -> Customer 69 :: de.mb.batch.model.Customer@58ca3783[customerId=69,firstName=John,lastName=Doe]
	2013-02-23 16:34:09,090  INFO   DatabaseWriter:25 - -> Customer 48 :: de.mb.batch.model.Customer@4402a6ff[customerId=48,firstName=John,lastName=Doe]
	2013-02-23 16:34:09,090  INFO   DatabaseWriter:25 - -> Customer 91 :: de.mb.batch.model.Customer@a21d23b[customerId=91,firstName=John,lastName=Doe]
	...
	
	
To change the commit interval update the batch.properties file.

	commit.interval=3
	 
