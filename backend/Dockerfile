FROM node:22

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

COPY wait-for-it.sh ./
RUN chmod +x wait-for-it.sh

CMD ["./wait-for-it.sh", "mongo:27017", "--", "npm", "run", "start:dev"]
