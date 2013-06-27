Final: Question 8

Supposed we executed the following Java code. How many animals will be inserted into the "animals" collection?
public class Question8 {



        public static void main(String[] args) throws IOException {
            MongoClient c =  new MongoClient(new MongoClientURI("mongodb://localhost"));
            DB db = c.getDB("test");
            DBCollection animals = db.getCollection("animals");


            BasicDBObject animal = new BasicDBObject("animal", "monkey");

            animals.insert(animal);
            animal.removeField("animal");
            animal.append("animal", "cat");
            animals.insert(animal);
            animal.removeField("animal");
            animal.append("animal", "lion");
            animals.insert(animal);

        }

}



A: 0

B: 1

C: 2

D: 3