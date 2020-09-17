## SIMPLE WMS DOCKERIZE


Simple to run
  1. git clone git@github.com:subhandp/simple-wms-dockerize.git
  2. cd simple-wms-dockerize
  3.  edit and adjust the .env.example file with your data after that change the file name to .env
  3. type and run
  ```bash
  $ docker-compose up --force-recreate
  ```
  4. if run successfull will appear Listened on port 3000, but we dont have yet any data 
  5. We will migrate the database
  6. first go to the shell be-wms container

```bash
  $ docker-compose exec be-wms/bin/sh
  ```
 ```bash
   $ yarn sequelize-cli db:migrate
  ```

```bash
  $ yarn sequelize-cli db:seed:all
  ```

7. opened up http://localhost:3000 on the browser browser.
8. execution API with Postman or other tools

Thank You


