# receipt-less-backend

## Docker set up:

Set up mongo:

    docker run --name mongo -d mongo

Run this inside the backend folder:

    docker build -t receipt-less-backend:1 .

Run the backed container

    docker run -p 8000:8000 -d --name backend --link mongo:mongo receipt-less:1

(Optional) Run Mongo Express to see inside DB

    docker run --link mongo:mongo -p 8081:8081 mongo-express