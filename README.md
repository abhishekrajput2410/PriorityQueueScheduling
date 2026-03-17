# Priority Queue System with Real-Time Monitoring

A distributed priority-based job processing system built with Node.js, Redis (BullMQ), MongoDB, and React.

## Features

- Priority-based job processing
- Redis-backed queue using BullMQ
- Worker auto scaling
- Dead Letter Queue for failed jobs
- SLA monitoring
- Real-time dashboard monitoring
- Load simulator for stress testing

## Tech Stack

Backend
- Node.js
- Express
- BullMQ
- Redis
- MongoDB
- Socket.io

Frontend
- React
- Chart.js
- WebSockets

## How to Run PriorityQueue Srtucture 

 Redis --> cd "C:\Program Files\Redis"  --> .\redis-cli.exe
 
 MongoDB --> C:\Program Files\MongoDB\Server\8.2\bin --> .\mongod.exe
 
 Backend Server --> cd backend --> node src/server.js
 
 AI-Service --> cd ai-server --> python train.py
 
 Worker --> cd backend --> node src/worker/worker.js
 
 Scaler --> cd backend --> node src/worker/scaler.js
 
 DLQ --> cd backend --> npm run dlq
 
 Frontend --> cd dashboard/frontend --> npm run dev
 
 Load Simulator --> cd load-test --> node loadSimulator.js

To Remone all previous requests from Mongodb and redis run in diff terminals

C:\Users\YourName> mongosh
test> use priorityQueue
priorityQueue> db.requests.deleteMany({})

C:\Users\YourName> redis-cli
127.0.0.1:6379> FLUSHALL

