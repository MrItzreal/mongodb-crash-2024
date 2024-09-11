# MongoDB Crash Course Notes

### What is MongoDB?

MongoDB is a NoSQL, document-oriented database.

- **NoSQL:** It doesn't rely on the traditional table-based relational model used in SQL databases.
- **Document-oriented:** It stores data in flexible, JSON-like documents (called BSON internally), allowing for a more dynamic and adaptable schema.

### Advantages of MongoDB

- **Flexibility:** The schema-less nature of MongoDB allows you to easily adapt to changing data requirements without major database migrations.
- **Scalability:** MongoDB is designed for horizontal scaling, meaning you can add more servers to handle increased data volume and traffic.
- **High Performance:** MongoDB's architecture and indexing capabilities enable fast read and write operations, making it suitable for high-performance applications.
- **Rich Query Language:** MongoDB provides a powerful query language that supports complex queries, aggregations, and geospatial operations.
- **Developer Friendly:** MongoDB integrates well with popular programming languages and frameworks, and its document model often aligns closely with application data structures.

### Key Concepts

1. **Documents:** The fundamental unit of data in MongoDB. Documents are similar to JSON objects and can contain various data types (strings, numbers, arrays, embedded documents, etc.).
2. **Collections:** Groups of related documents. Collections are analogous to tables in relational databases, but they don't enforce a strict schema.
3. **Databases:** Containers for collections. Databases provide a logical separation of data and can be used to organize your application's data.

### Important Note: Connecting MongoDB Shell to VS Code Terminal in Windows

**If you run into the problem "mongosh is not recognizable as the name of a cmdlet" or "INFO: Could not find files for the given pattern(s). or $ mongosh $MDB_CONNECTION_STRING;
bash: mongosh: command not found" or something similar. At 5:06 in the system variables, you should click on "Path" and then add the location of the file called: mongosh.exe . Otherwise, VS Code won't recognize it.**

### MongoDB Shell Terminal Basic Commands:

**mongosh:** starts new MongoDB shell session and connect to a local MongoDB instance running on the default port.
**cls:** clears terminal screen.
**exit:** exits the current MongoDB shell session.
**show dbs:** shows current list of all databases.
**use <name of db>:** switches to specified db.
**use <name of db>:** this same command can create a new db.
**db.createCollection("<add name of collection>"):** creates a collection.
**db.dropDatabase():** drops a database.
**db.<name of collection>.insertOne({name:"My", age: 23}):** inserts documents into collection.
**db.<name of collection>.find():** shows all or specific documents within a collection.
**db.<name of collection>.insertMany([{..},{..},{..}]):** inserts multiple documents into a collection.

### Important Notes

-You can also download the extension for MongoDB on VS Code which allows connection to MongoDB & Atlas.
-If a collection doesn't exist, MongoDB will automatically create it for you when you execute the insertOne() command.
-When using the "use" command, MongoDB will not implicitly create a database if it doesn't exist. You will need to explicitly create the database or perform an operation like an "insert".
-MongoDB adds an ID automatically to data submitted.
