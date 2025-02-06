# MongoDB Task
## Setup:

1. **Connect to MongoDB Cluster**

Enter Below command in command line and enter password of the user

```bash 
mongosh "mongodb+srv://cluster0.azzjb.mongodb.net/" --apiVersion 1 --username viratjinjala
```

2. **Check current Database**
   
To check the current databases available:

```bash
show dbs
```

![Image](https://github.com/user-attachments/assets/335d4099-f6af-4347-a2ae-eb304dfa7ccd)

3. **Create & Switch to database**

This will create the database and switch:

```bash
use DBMS-2
```

![Image](https://github.com/user-attachments/assets/f200b9c3-ec90-42eb-8a21-3b70cc70f1f6)

4. **Create Collection**
```bash
db.createCollection("my_collection")
```

![Image](https://github.com/user-attachments/assets/b2044653-3b62-4104-91af-b45403ca0f13)

5. **List down Collections**
```bash
db.getCollectionNames()
```

![Image](https://github.com/user-attachments/assets/379985d9-2a1c-4619-ac8e-a71a63e22a3d)

## Operations:

Q:1. **Batch Create with minimum 100 records in MongoDb (create batch).**

Query:

```bash
db.my_collection.insertMany(
[
  { "name": "John", "age": 28, "city": "New York", "hobby": "Cycling", "favoriteColor": "Blue" },
  { "name": "Alice", "age": 25, "city": "Los Angeles", "hobby": "Reading", "favoriteColor": "Green" },
  { "name": "Bob", "age": 30, "city": "Chicago", "hobby": "Cooking", "favoriteColor": "Red" },
  { "name": "Charlie", "age": 35, "city": "San Francisco", "hobby": "Photography", "favoriteColor": "Yellow" },
  { "name": "David", "age": 40, "city": "Miami", "hobby": "Fishing", "favoriteColor": "Orange" },
  { "name": "Emma", "age": 22, "city": "Boston", "hobby": "Yoga", "favoriteColor": "Purple" },
  { "name": "Frank", "age": 50, "city": "Seattle", "hobby": "Hiking", "favoriteColor": "Brown" },
  { "name": "Grace", "age": 31, "city": "Dallas", "hobby": "Painting", "favoriteColor": "Pink" },
  { "name": "Hannah", "age": 29, "city": "Austin", "hobby": "Swimming", "favoriteColor": "Blue" },
  { "name": "Ivy", "age": 45, "city": "San Diego", "hobby": "Gardening", "favoriteColor": "Green" },
  { "name": "Jack", "age": 38, "city": "Atlanta", "hobby": "Football", "favoriteColor": "Red" },
  { "name": "Kenny", "age": 60, "city": "Seattle", "hobby": "Fishing", "favoriteColor": "Black" },
  { "name": "Lily", "age": 27, "city": "Denver", "hobby": "Cycling", "favoriteColor": "White" },
  { "name": "Megan", "age": 33, "city": "Washington D.C.", "hobby": "Running", "favoriteColor": "Yellow" },
  { "name": "Nina", "age": 24, "city": "Phoenix", "hobby": "Dancing", "favoriteColor": "Purple" },
  { "name": "Olivia", "age": 41, "city": "Miami", "hobby": "Yoga", "favoriteColor": "Pink" },
  { "name": "Paul", "age": 36, "city": "Chicago", "hobby": "Cooking", "favoriteColor": "Orange" },
  { "name": "Quincy", "age": 30, "city": "Los Angeles", "hobby": "Photography", "favoriteColor": "Blue" },
  { "name": "Rachel", "age": 37, "city": "Houston", "hobby": "Traveling", "favoriteColor": "Red" },
  { "name": "Steve", "age": 47, "city": "San Francisco", "hobby": "Cycling", "favoriteColor": "Green" },
  { "name": "Tina", "age": 28, "city": "New York", "hobby": "Hiking", "favoriteColor": "Yellow" },
  { "name": "Ursula", "age": 32, "city": "Boston", "hobby": "Yoga", "favoriteColor": "Purple" },
  { "name": "Victor", "age": 50, "city": "Dallas", "hobby": "Fishing", "favoriteColor": "Orange" },
  { "name": "Wendy", "age": 22, "city": "Austin", "hobby": "Reading", "favoriteColor": "Blue" },
  { "name": "Xander", "age": 40, "city": "Seattle", "hobby": "Traveling", "favoriteColor": "Black" },
  { "name": "Yara", "age": 26, "city": "San Diego", "hobby": "Painting", "favoriteColor": "Pink" },
  { "name": "Zach", "age": 30, "city": "Phoenix", "hobby": "Cycling", "favoriteColor": "Green" },
  { "name": "Aiden", "age": 27, "city": "New York", "hobby": "Swimming", "favoriteColor": "Yellow" },
  { "name": "Bella", "age": 33, "city": "Washington D.C.", "hobby": "Running", "favoriteColor": "Purple" },
  { "name": "Cody", "age": 42, "city": "Dallas", "hobby": "Football", "favoriteColor": "Red" },
  { "name": "Diana", "age": 29, "city": "Miami", "hobby": "Cooking", "favoriteColor": "Blue" },
  { "name": "Eli", "age": 36, "city": "San Francisco", "hobby": "Photography", "favoriteColor": "Green" },
  { "name": "Fiona", "age": 50, "city": "Seattle", "hobby": "Fishing", "favoriteColor": "Black" },
  { "name": "Gavin", "age": 34, "city": "Los Angeles", "hobby": "Traveling", "favoriteColor": "Yellow" },
  { "name": "Holly", "age": 27, "city": "Chicago", "hobby": "Cycling", "favoriteColor": "Pink" },
  { "name": "Isaac", "age": 41, "city": "Boston", "hobby": "Yoga", "favoriteColor": "Purple" },
  { "name": "Jasmine", "age": 26, "city": "Atlanta", "hobby": "Painting", "favoriteColor": "Orange" },
  { "name": "Kyle", "age": 34, "city": "Houston", "hobby": "Football", "favoriteColor": "Red" },
  { "name": "Lena", "age": 31, "city": "San Diego", "hobby": "Hiking", "favoriteColor": "Green" },
  { "name": "Mark", "age": 45, "city": "Phoenix", "hobby": "Swimming", "favoriteColor": "Blue" },
  { "name": "Nadia", "age": 38, "city": "Dallas", "hobby": "Dancing", "favoriteColor": "Yellow" },
  { "name": "Owen", "age": 32, "city": "Seattle", "hobby": "Photography", "favoriteColor": "Purple" },
  { "name": "Penny", "age": 29, "city": "San Francisco", "hobby": "Cooking", "favoriteColor": "Orange" },
  { "name": "Quinn", "age": 33, "city": "Los Angeles", "hobby": "Cycling", "favoriteColor": "Blue" },
  { "name": "Reed", "age": 40, "city": "Chicago", "hobby": "Traveling", "favoriteColor": "Green" },
  { "name": "Sophia", "age": 25, "city": "Miami", "hobby": "Yoga", "favoriteColor": "Purple" },
  { "name": "Tony", "age": 37, "city": "San Diego", "hobby": "Running", "favoriteColor": "Yellow" },
  { "name": "Ursula", "age": 45, "city": "Washington D.C.", "hobby": "Painting", "favoriteColor": "Pink" },
  { "name": "Vera", "age": 29, "city": "New York", "hobby": "Photography", "favoriteColor": "Blue" },
  { "name": "Will", "age": 41, "city": "Phoenix", "hobby": "Fishing", "favoriteColor": "Red" },
  { "name": "Xander", "age": 32, "city": "Seattle", "hobby": "Hiking", "favoriteColor": "Green" },
  { "name": "Yasmine", "age": 30, "city": "Los Angeles", "hobby": "Cooking", "favoriteColor": "Orange" },
  { "name": "Zane", "age": 37, "city": "Houston", "hobby": "Cycling", "favoriteColor": "Yellow" },
  { "name": "Amelia", "age": 33, "city": "San Francisco", "hobby": "Yoga", "favoriteColor": "Purple" },
  { "name": "Brian", "age": 48, "city": "Dallas", "hobby": "Fishing", "favoriteColor": "Blue" },
  { "name": "Clara", "age": 24, "city": "New York", "hobby": "Swimming", "favoriteColor": "Green" },
  { "name": "David", "age": 50, "city": "San Francisco", "hobby": "Photography", "favoriteColor": "Red" },
  { "name": "Eleanor", "age": 39, "city": "Chicago", "hobby": "Traveling", "favoriteColor": "Black" },
  { "name": "Felix", "age": 34, "city": "Los Angeles", "hobby": "Cooking", "favoriteColor": "Yellow" },
  { "name": "Grace", "age": 29, "city": "San Francisco", "hobby": "Cycling", "favoriteColor": "Blue" },
  { "name": "Henry", "age": 52, "city": "San Diego", "hobby": "Fishing", "favoriteColor": "Green" },
  { "name": "Isla", "age": 36, "city": "Seattle", "hobby": "Photography", "favoriteColor": "Purple" },
  { "name": "Jack", "age": 25, "city": "Dallas", "hobby": "Football", "favoriteColor": "Red" },
  { "name": "Kate", "age": 44, "city": "Miami", "hobby": "Running", "favoriteColor": "Yellow" },
  { "name": "Leo", "age": 31, "city": "Washington D.C.", "hobby": "Swimming", "favoriteColor": "Blue" },
  { "name": "Maya", "age": 22, "city": "Austin", "hobby": "Dancing", "favoriteColor": "Green" },
  { "name": "Nolan", "age": 47, "city": "Chicago", "hobby": "Hiking", "favoriteColor": "Orange" },
  { "name": "Olga", "age": 40, "city": "Houston", "hobby": "Photography", "favoriteColor": "Purple" },
  { "name": "Piper", "age": 38, "city": "Los Angeles", "hobby": "Cycling", "favoriteColor": "Blue" },
  { "name": "Quinn", "age": 29, "city": "Seattle", "hobby": "Painting", "favoriteColor": "Pink" },
  { "name": "Riley", "age": 41, "city": "San Diego", "hobby": "Cooking", "favoriteColor": "Red" },
  { "name": "Sam", "age": 50, "city": "Phoenix", "hobby": "Football", "favoriteColor": "Yellow" },
  { "name": "Tess", "age": 35, "city": "San Francisco", "hobby": "Running", "favoriteColor": "Green" },
  { "name": "Uma", "age": 28, "city": "Washington D.C.", "hobby": "Swimming", "favoriteColor": "Blue" },
  { "name": "Vince", "age": 38, "city": "New York", "hobby": "Traveling", "favoriteColor": "Purple" },
  { "name": "Wes", "age": 26, "city": "Miami", "hobby": "Dancing", "favoriteColor": "Orange" },
  { "name": "Xander", "age": 42, "city": "Phoenix", "hobby": "Photography", "favoriteColor": "Yellow" },
  { "name": "Yara", "age": 31, "city": "Dallas", "hobby": "Cycling", "favoriteColor": "Red" },
  { "name": "Zoe", "age": 33, "city": "San Diego", "hobby": "Yoga", "favoriteColor": "Green" },
  { "name": "Alex", "age": 29, "city": "New York", "hobby": "Reading", "favoriteColor": "Blue" },
  { "name": "Beth", "age": 34, "city": "Houston", "hobby": "Hiking", "favoriteColor": "Yellow" },
  { "name": "Chloe", "age": 25, "city": "Los Angeles", "hobby": "Painting", "favoriteColor": "Red" },
  { "name": "Derek", "age": 39, "city": "Seattle", "hobby": "Football", "favoriteColor": "Purple" },
  { "name": "Eva", "age": 30, "city": "San Diego", "hobby": "Cooking", "favoriteColor": "Green" },
  { "name": "Fred", "age": 32, "city": "Phoenix", "hobby": "Running", "favoriteColor": "Yellow" },
  { "name": "George", "age": 45, "city": "Chicago", "hobby": "Fishing", "favoriteColor": "Blue" },
  { "name": "Hilda", "age": 36, "city": "Washington D.C.", "hobby": "Swimming", "favoriteColor": "Red" },
  { "name": "Ingrid", "age": 50, "city": "San Francisco", "hobby": "Photography", "favoriteColor": "Green" },
  { "name": "Jackie", "age": 41, "city": "Dallas", "hobby": "Dancing", "favoriteColor": "Orange" },
  { "name": "Kyle", "age": 29, "city": "Miami", "hobby": "Cycling", "favoriteColor": "Yellow" },
  { "name": "Lena", "age": 38, "city": "San Diego", "hobby": "Traveling", "favoriteColor": "Pink" },
  { "name": "Mason", "age": 33, "city": "Houston", "hobby": "Yoga", "favoriteColor": "Purple" },
  { "name": "Nina", "age": 31, "city": "Chicago", "hobby": "Cooking", "favoriteColor": "Red" },
  { "name": "Oscar", "age": 28, "city": "Seattle", "hobby": "Running", "favoriteColor": "Green" },
  { "name": "Paige", "age": 36, "city": "New York", "hobby": "Swimming", "favoriteColor": "Blue" },
  { "name": "Quinn", "age": 42, "city": "Dallas", "hobby": "Photography", "favoriteColor": "Purple" },
  { "name": "Rita", "age": 37, "city": "Los Angeles", "hobby": "Hiking", "favoriteColor": "Orange" },
  { "name": "Stan", "age": 30, "city": "San Francisco", "hobby": "Cycling", "favoriteColor": "Green" },
  { "name": "Tom", "age": 44, "city": "Miami", "hobby": "Traveling", "favoriteColor": "Yellow" },
  { "name": "Ursula", "age": 29, "city": "Austin", "hobby": "Painting", "favoriteColor": "Pink" },
  { "name": "Vanessa", "age": 33, "city": "Phoenix", "hobby": "Swimming", "favoriteColor": "Red" },
  { "name": "Walter", "age": 41, "city": "Houston", "hobby": "Fishing", "favoriteColor": "Blue" },
  { "name": "Xander", "age": 39, "city": "Seattle", "hobby": "Running", "favoriteColor": "Orange" },
  { "name": "Yasmin", "age": 38, "city": "San Francisco", "hobby": "Cycling", "favoriteColor": "Yellow" },
  { "name": "Zane", "age": 40, "city": "Los Angeles", "hobby": "Traveling", "favoriteColor": "Purple" }
]
);
```
Result:

![Image](https://github.com/user-attachments/assets/00da5f73-9fa8-4f55-b988-67da1b6c9b5c)


Q:2. **Batch Update with minimum 100 records  in MongoDB (update batch).**

Query:

```bash
db.my_collection.updateMany(
  { city: "New York" },
  { $set: { city: "NYC" } }
);
```
Result:

![Image](https://github.com/user-attachments/assets/0c106fff-60cc-43ff-b566-135161df84a9)


3. **Perform indexing on particular 3 fields in MongoDB.**

Query:

```bash
db.my_collection.createIndex({ name: 1, age: 1, city: 1});
```

Result:

![Image](https://github.com/user-attachments/assets/530d1e49-e3e7-4c41-8ed8-afab4bafe4c7)


4. **Find duplicates using aggregation in MongoDB**

Query:

```bash
db.my_collection.aggregate([
  { $group: { _id: "$name", count: { $sum: 1 } } },
  { $match: { count: { $gt: 1 } } }, 
  { $project: { _id: 0, name: "$_id", count: 1 } }, 
]);
```

Result:

![Image](https://github.com/user-attachments/assets/86495e08-0d1c-4063-97d0-c053f10ac8e8)
