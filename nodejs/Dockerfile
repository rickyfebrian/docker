FROM node:16

WORKDIR /app/
COPY . /app/

RUN npm i
EXPOSE 3000

HEALTHCHECK --interval=5s --timeout=30s --start-period=5s --retries=3 CMD curl --fail http://localhost:3000 || exit 1

CMD [ "npm", "run", "start" ]
