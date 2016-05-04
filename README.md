# docker-node
A base docker contaner for Node JS applications

## Node Version

This docker container currently installs the version of Node used throughout UKTI applications, Node 5.11.0 with NPM 3

## Folder layout
By default the docker build process will copy the current folders contents to /app

## Install and RUN
At this time the Dockerfile only installs node but does not auto start an app, or install npm packages. Typically you
will combine this Dockerfile with your own and add that reuqire code to start your application.

```
FROM ukti/node

ENV PORT = 80
ENV NODE_ENV = production

RUN NODE_ENV=production npm install

CMD ["npm run start"]

EXPOSE 80
```
