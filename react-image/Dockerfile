# pull official base image
FROM node:lts-alpine3.10

# set working directory
WORKDIR /app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH
ENV DOMAIN_SERVER=http://nodeback

# install app dependencies
COPY package.json ./
#COPY package-lock.json ./
RUN npm install --silent
RUN npm install node-sass --silent
RUN npm install react-scripts@3.3.0 -g --silent

# add app
COPY . ./

# start app
CMD ["npm", "start"]