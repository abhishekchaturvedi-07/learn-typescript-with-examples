# learn-typescript-with-examples
Typescript
mkdir learn-typescript
cd learn-typescript
npm init
npm i -D typescript

// to create tsconfig.json npx tsc  --init

//make this option true
"esModuleInterop": true, 
Earlier we use to import like “import * as React from ‘react’” but when we enable this option we can use it like “import React from ‘react” enable "outDir": "./" ("outDir": "dist",), | "jsx": "preserve",  | "jsx": "react" (for react),  
Add this “"include": ["src/**/*"]“ - to include all the files in this folder
npx tsc - compile it : you will notice a Dist folder

Open package.json and add build script :
"scripts": {
    "build": "tsc"
  },

Run in watch mode :  npx tsc -w
It till watch all the changes inside the src folder which we add in include inside tscofig file

Install nodemon for watch the file without restart the build  npm i -D nodemon

To run the watcher and nodemon at at time, you can install:
npm i -D concurrently

Then run both the process at a time :
npx concurrently "tsc -w" "nodemon -w dist -q dist/index.js"
To check the sequence
npx concurrently -n COMPILE,NODEMON yello,blue "tsc -w" "nodemon -w dist -q dist/index.js"

Enjoy TS




