# promisequel
simple mysql promise wrapper package

install :

```
npm i promisequel
```


usage example :


```JavaScript
const promisequel = require('promisequel')

const config = {
    host: process.env.DATABASE_HOST,
    user: process.env.DATABASE_USER,
    password: process.env.DATABASE_PASSWORD,
    database: process.env.DATABASE_NAME
}

const db = new promisequel(config)

db.query('select * from example where id = ?', 1)
    .then(result => {
        console.log(result)
    }).catch(err => {
        console.log(err)
    })
```
