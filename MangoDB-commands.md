MongoDB Commands
----------------
    -> Check existing databases
            show databases (or) show dbs

 1. Create Database
        use database-name      

 2. Create collection(tables in RDBMS)
        db.createCollection("name-of-collection")
    -> Check collections of a database
            show collections

 3. Insert Documents into that collection(rows inRDBMS)
        db.collection-name.insertOne(document)
        db.collection-name.insertMany([d1,d2,...])
        
        Structure of a mongodb Document:
                    {
                        "name":"ravi",
                        "age":21,
                        "city":"hyderabad"
                    }

4 . Read Documents
        db.collection-name.findOne()
        db.collection-name.find()

            -> Query operators  
                 db.collection-name.findOne({field:{op:value}})
                    $eq  (===)
                    $gt  (>)
                    $gte (>=)
                    $lt  (<)
                    $lte (<=)
                    $ne  (!=)
                    $in 
            -> Logical operators (Join multiple conditions)
                db.collection-name.find({$and:[cond-1,cond-2,...]})
                    $and  (&&)
                    $or   (||)
                    $not  (! )

4. Update a document
        db.collection-name.updateOne(condition,update)
        db.collection-name.updateMany(condition,update)
                
            
5. Delete a document
        db.collection-name.deleteOne(condition)
        db.collection-name.deleteMany(condition)