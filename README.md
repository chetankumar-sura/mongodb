# mongodb basic operations and syntaxes

use college // college is the database name

db

db.students.insert{{"id": 123,"name":"chethan"}}

show dbs

var x= 2
x
var y ="chethan"
y

db.createCollection("my products") #creating collections and inserting values

show collections

db.products.insertMany([{"id":143,"product_name":"ipod","Quantity":2,"price":400.0,"available":false}, // many insertions ata time into an collection
{"id":231,"product_name":"MACBOOK PROMAX","Quantity":3,"price":7909.0,"available":true},
{"id":56634,"product_name":"GOOGLE AIRBUDS","Quantity":2,"price":7999.0,"available":true}])

db.products.find({"product_name":"MACBOOK PROMAX"}).pretty()

db.products.find({"available":true}).pretty() 

db.products.find({"price":{$gt:400}}).pretty()

db.products.find({"product_name":{$regex:%a%}}).pretty()

db.products.find({"price":{$lte:400}}).pretty()

db.products.find({"price":{$lte :400} $or {$eq :7999}}).pretty()

db.products.find({"price":{$gte:100}).sort({"price":1}).pretty()


