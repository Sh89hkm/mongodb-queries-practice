# MongoDB Queries Practice

The objectives of this assignment are:

1. Practicing MongoDB queries on a local database
2. Learning to query MongoDB collections directly before implementing the same in CRUD APIs

## Setup

### Prepare Local Database using Docker

With Docker, setting up your local database becomes straightforward and ensures a consistent environment across different setups. Follow these steps to prepare your local MongoDB database:

1. **Start MongoDB Container**: First, start the MongoDB container by running:

   ```
   npm run start
   ```

2. **Verify Container Running**: To ensure that the MongoDB container is running correctly and to check your container name, use the following command:

   ```
   npm run verify
   ```

3. **Copy Restaurant Data to Container**: Now, copy the `restaurants.json` data file to your running MongoDB container. Replace `<path to your restaurant.json file>` with the actual path to your `restaurants.json` file, and `your_container_name` with the name of your MongoDB container:

   ```
   npm run copy-data
   ```

4. **Import Data into MongoDB**: Import the restaurant data into the MongoDB database by executing:

   ```
   npm run import-data
   ```

5. **Access MongoDB Shell**: To interact with your MongoDB instance, access the shell using:

   ```
   npm run shell
   ```

6. **Switch to Practice Database**: Inside the MongoDB shell, switch to the `practice` database:

   ```
   use practice
   ```

7. **Verify Data Import**: Confirm that the data import was successful by fetching the first document from the `restaurants` collection:

   ```
   db.restaurants.findOne()
   ```

   If you see the details of the first restaurant, your setup is complete and successful.

8. **Exit MongoDB Shell**: To exit the Mongo shell, simply type `exit`.

Now your MongoDB environment is set up inside a Docker container, and you're ready to start querying your local `practice` database.

9. **Delete volume and reset**: if things got missy and you want to start from scratch, you can use the follwing command and restart from step 1

`npm run reset`

## Practice Time

Let's perform some queries on our restaurants collection now. In this assignment repo, you will find another markdown file called `QUERIES.md`. In this file, we have listed many practice queries for you. Go through the questions one by one and try to execute the queries on your Mongo shell.

You can keep the MongoDB documentation open on your browser to help you with the queries.

As you finish executing your queries, paste the solutions in the provided space inside markdown code blocks syntax below each query statement.

## Submission

Once you're ready to submit the assignment, follow these steps on your terminal:

1. Stage your changes to the `QUERIES.md` file to be committed: `git add QUERIES.md`
2. Commit your final changes: `git commit -m "solve assignment"`
3. Push your commit to the main branch of your assignment repo: `git push origin main`

After your changes are pushed, return to this assignment on Canvas for the final step of submission.

## Conclusion

Now that we have practiced performing queries on a MongoDB database, we are ready for module 3 where we will learn to build a CRUD API using Express.js and a MongoDB ODM.
