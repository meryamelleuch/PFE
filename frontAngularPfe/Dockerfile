
FROM node:12.20

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./
ENV PATH /app/node_modules/.bin:$PATH

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production
RUN npm install -g @angular/cli@9.1.15


# Bundle app source
COPY . .
#EXPOSE 1323
#CMD [ "ng", "build"]
CMD ng serve --host 0.0.0.0
EXPOSE 4200


