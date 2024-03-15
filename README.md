# Typescript-Project-Setup
How to setup your typescript project 

1. npm init -y

2. npm install typescript --save-dev

3. npm install @types/node --save-dev

4. npx tsc --init --rootDir src --outDir build \
--esModuleInterop --resolveJsonModule --lib es6 \
--module commonjs --allowJs true --noImplicitAny true

5. npm install ts-node
6. npm install typescript @types/node ts-node express passport passport-local passport-jwt bcryptjs jsonwebtoken pg @types/express @types/passport @types/passport-local @types/passport-jwt

7. put below in package.json in script
   ```
   "test": "echo \"Error: no test specified\" && exit 1",
    "start": "tsc && node dist/index.js",
    "dev": "nodemon dist/index.js",
    "copy-files": "copyfiles --up 1 src/resources/locales/* ./dist/",
    "build": "rm -rf ./dist/ && tsc -p .",
    "watch": "nodemon -e ts -w ./src -x npm run watch:serve",
    "watch:serve": "ts-node src/index.ts",
    "postbuild": "npm run copy-files"

    ```
8. npm i copyfiles
9. make src folder and put index.ts file
10. put basic code 
    ```mport express from 'express'

    const app = express()

    app.listen(7000,()=>{
    return console.log("server is running on port 7000")
    })```
11. npm run build
12. npm run watch
