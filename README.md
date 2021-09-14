[checkmark]: https://raw.githubusercontent.com/mozgbrasil/mozgbrasil.github.io/master/assets/images/logos/logo_32_32.png "MOZG"

![valid XHTML][checkmark]

# mongo-labs

## Contribuição

Caso queira contribuir para melhoria da documentação de um Fork no repositório e envie um pull request ou edite no github

## Requerimentos

- https://www.docker.com/
- https://code.visualstudio.com/
- https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack

## Executando local

```
git clone ☝️

cd <directory>

code --new-window .
```

## -

### mongodb - local

```
telnet 172.18.0.2 27017 # mongodb

docker network connect mongodb_devcontainer_default <container>
```

### mongodb - DevContainer

```

#npm view mongodb
#yarn info mongodb

mongo "mongodb://172.18.0.2:27017/roadcam"

mongo "mongodb://172.18.0.2:27017/local" --username dbUser

mongo "mongodb+srv://localhost:27017/<dbname>" --username dbUser

mongo --version

mongo <<EOF
show databases
EOF

mongo <<EOF
show databases
use local
show collections
db.startup_log.find()
db.startup_log.findOne()
db.startup_log.find().count()
EOF

https://www.striphtml.com/

mongo <<EOF
show databases
use roadcam
show collections
EOF

mongoimport \
--uri 'mongodb://172.18.0.2:27017/roadcam' \
--collection='cameras' \
--file='cameras-mongodb.json'

mongo <<EOF
show databases
use roadcam
show databases
db.cameras.insertOne( { x: "Feature"  } )
show collections
EOF

mongo <<EOF
show databases
use myNewDB
db.myNewCollection1.insertOne( { x: 1 } )
db.myNewCollection2.insertOne( { x: 1 } )
db.myNewCollection3.createIndex( { y: 1 } )
show collections
EOF

mongo <<EOF
show databases
use roadcam
db.dropDatabase()
show databases
EOF


nano /home/marcio/dados/acid-workflow/node-labs/views/tests/findup/scope/users.json

mongoimport --db findup --collection users_0209_153801 --type json --file  ./views/tests/findup/scope/users.json


$ mongo

👇️

db.getName()
show databases

👇️

show databases
use microsoft_typescript_node
db.getName()
show collections

db.createCollection('helloworlds');

var file = cat('./views/tests/findup/scope/users.json')
var o = JSON.parse(file)
db.patients.insert(o.results)
db.patients.find().count()
show collections

👇️

function printSchema(obj, indent) {
  for (var key in obj) {
    print(indent, key, typeof obj[key]) ;
    if (typeof obj[key] == "object") {
      printSchema(obj[key], indent + "\t")
    }
  }
};

var schemaObj = db.patients.findOne();
printSchema(schemaObj,"");

👇️

db.collection_users_findup.drop()
show collections

👇️

use findup
db.getName()
db.dropDatabase()
show databases

👇️
 


👇️


👇️


```
