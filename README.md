<h2>Motivation</h2>
Solve the limitations of the regular node + typescript setup <a href='https://github.com/NathanKr/node-typescript-setup-tsconfig'>here</a>. Thus we have good setup for node using typescript via ts-node (adding express is trivial)


<h2>Installation</h2>
<ul>
<li>

```
npm i
```
</li>
<li>
This is actually limitation, local install is not working of the box    

```
npm i -g ts-node
```
</li>
<li>
create tsconfig.json :

```
tsc --init
```
</li>
<li>
tweak tsconfig.json :

```
"target": "ES2020",
"outDir": "./dist", 
 "rootDir": "./src",
 "sourceMap": true,

```
</li>
<li>
add scripts in package.json

```
    "start": "node ./dist/index.js",
    "dev": "nodemon ./src/index.ts",
    "build": "tsc -p ."
```

</li>

</ul>

<h2>Usage</h2>
The following will compile the typescript code and run using nodemon.
The out dir is not created !!!! and is not need

```
npm run dev
```

create a build version using

```
npm run build
```

run production version using

```
npm run start
```


<h2>Benefits of using ts-node</h2>
Notice the limitation of using just tsc <a href='https://github.com/NathanKr/node-typescript-setup-tsconfig'>here</a>
<ul>
<li>Development is easy. No need for one terminal for copiling using tsc and one terminal for running. Here npm run dev will run ts-node which compiles ts files and execute nodemon</li>
<li>A dist version is not created when nodemon is used thus no problem with searching</li>
<li>The other two limitations remains</li>
</ul>



<h2>Open issue</h2>
<ul>
<li>what is the purpose of tsc -p</li>
</ul>
