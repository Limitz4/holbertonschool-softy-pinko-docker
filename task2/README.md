# Task 2 - Frontend + Backend

## Backend (Flask API)
Build: docker build -t softy-pinko-backend:task2 ./back-end
Run: docker run -d -p 5252:5252 --name backend softy-pinko-backend:task2
Test: curl http://localhost:5252/api/hello

## Frontend (Nginx)
Build: docker build -t softy-pinko-frontend:task2 ./front-end
Run: docker run -d -p 9000:9000 --name frontend softy-pinko-frontend:task2
Open: http://localhost:9000

## Cleanup
docker stop backend frontend
docker rm backend frontend
docker rmi softy-pinko-backend:task2 softy-pinko-frontend:task2
