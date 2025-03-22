#FROM node:20
#IC-1
FROM node:20.18.3-alpine3.21
#on top of IC -1 instruction 2 is executed and save this as layer 2 image. ic-1 is deleted
RUN addgroup -S expense && adduser -S expense -G expense && \
# create ic-2 on top of ic-2 instruction 3 is executed ans save as layer 3. ic-2 is deleted.
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
USER expense
CMD ["node", "index.js"]