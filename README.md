# Backend-Interview-Questions
A list of backend interview questions that myself and colleagues have received in the past, and my answers to them. Feel free to contribute with additional questions and/or building upon my answers.


# Databases
### What is the difference between a relational and non-relational database? 
The first thing that needs to be cleared up is there are two main database technologies, SQL, and NoSQL. SQL is relational, while NoSQL is non-relational. The most common brands of SQL are MySQL, Sqlite, PostgreSQL, and Oracle. The most common NoSQL brands are MongoDB, Cassandra, Neo4j, and Redis. It's important to note that within the category of non-relational databases, there are also various sub-categories, such as graph, column-stores, key-value stores, and document non-relational databases. Neither technology is an upgrde of the other, or can be considered 'better', they each have their use-cases. 

A SQL store is in the format of a table, where columns represent certain fields (or type of information), and each row represents a particular entry. This is similar in format to an excel sheet for example. The relationship between fields and the tables, is the SQL schema, you can envision this as the blueprint for your database. A SQL database is more rigid, each table accepts a certain type of entry, and nothing different, and each column can only accept one data type, an ID column that accepts an integer can only take an integer, you cannot store a string where an integer goes. 

NoSQL stores are in a field-value store much like a JSON object. In a similar manner, you can have a NoSQL collection, again a field-value store, where the values can be any data type (Integer, String, etc), it is much more flexible than a SQL database. Along with being flexible, a NoSQL database does not even need a pre-defined schema. This is why it is commonly referred to as "schema-less." For example, the following command will not only insert a new article, but will create a new 'article' collection if one did not previously exist:
```
db.article.insert(
  ID: 55,
  title: "My blog post",
  author: "YoshCode",
  format: "blog post",
  date: new Date(),
);
```
### What is SQL Normalization? 
To reduce data redundancy, in one table you can include a foreign key which points to another type of value. For example, let's assume we want to store more information about an 'author' such as date of birth, gender, and age. It wouldn't make sense to include all of this data on each blog post. It deserves to have it's own table. Then in the blog post table you can simply 'point' to the author with a foreign key, which references the author in it's own table. This optimazation, is referred to as SQL normalization. 

### What is NoSQL denormalization? 
### When would you use a relational database instead of a non-relational database? 

RESOURCES:
https://www.upwork.com/hiring/data/sql-vs-nosql-databases-whats-the-difference/
https://www.sitepoint.com/sql-vs-nosql-differences/
https://www.sitepoint.com/sql-vs-nosql-choose/

# Other
### How does an environment variable differ from a shell variable? 
