# Setup NPM webserver for programming

## Initialize
First time setup in the folder containing the html files and execute. Fill out the props and be sure that the "entry point" points the the first HTML page you want displayed. Typically index.html.

```
npm init
```

This will create the **package.json** file. This file is the roadmap to launching an npm application. More on this later.

## Install lite-server

Next we need to install lite-server; to do this we execute the following command.
```
npm install lite-server --save-dev
```
This will pull in the respective tools for the server into a new directory called "**node_modules**". It will also create a file called "package-lock.json".



## Audit Fix?? (optional) 
There may be some issues with the npm and you might get prompted to fix them by running this command.
```
npm audit fix
```
  
## Edit package.json file
Review in your favorite text editor the package.json file to ensure the server configuration is correct paying special attention to the rows in BLUE. These are critical to a successful npm server launch.
```
{
	"name": "interactivity-with-javascript",
	"version": "1.0.0",
	"description": "Coursera Work -- Interactivity with JavaScript",
	"main": "index.html",
	"scripts": {
		"start": "npm run lite",
		"lite": "lite-server",
		"test": "echo \"Error: no test specified\" && exit 1"
	},
	"repository": {
		"type": "git",
		"url": "git+[https://github.com/salmancuso/interactivity-with-JavaScript.git](https://github.com/salmancuso/interactivity-with-JavaScript.git)"
	},
	"author": "Sal Mancuso",
	"license": "ISC",
	"bugs": {
		"url": "[URL/TO/GIT/REPO](URL/TO/GIT/REPO)"
	},
	"homepage": "[URL/TO/GIT/REPO#readme](URL/TO/GIT/REPO#readme)",
	"dependencies": {},
	"devDependencies": {
		"lite-server": "^2.4.0"
	}
}
```
  

  

If you have made it this far, then it is time to **launch the server** by typing. Once the server starts with no errors it will launch your preferred browser and load the site.
```
npm start
```
    

## **Trouble shooting** the npm server. 
Sometimes it gags and the easiest way is to start fresh.

**Step 1:**
```
npm cache clean --force
```

**Step 2::**
```
delete node_modules folder
```
  

**Step 3::**
```
npm install
```


**Step 4: :** Repeat steps above for normal setup.
