How to set up and test APIs to MongoDB

1. Open a terminal, command： mongod. 
This run a MongoDB in localhost. ctrl + c to kill process

2. Open another terminal, command: mongo. 
This run a MongoDB shell. In shell, you can interact with a mongo database directly.
quit() to kill shell process.
For more MongoDB shell commands, please reference: https://docs.mongodb.com/manual/reference/mongo-shell/

2.a In mongo shell, run: show dbs. To show each db that can be run in localhost.
2.b In mongo shell, run: db. to show which db that is currently running in localhost.

2.c In mongo shell, run: use ActorTest. to switch to ActorTest db that is used for test. 
you can also create a new db for testing, by running: use <non-exsit db name>. And please also update the db name in MongoConn.js file. 

3. Open another terminal, command: node *.js. 
This run a js file. Once you finish #1, the js code can talk to MongoDB directly.

4. Before patching csv file, please change pathToCsv to the path(include name.csv) to read the correct csv.

###########
##How to read patched data in MongoDb
###########
1. In Mongo shell, run： show collections. to check all collections name under the current db.

2. In Mongo shell, run: db.<collection name>.find(), to show all data under the collection.