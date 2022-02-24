# CSS-SCSS-Dependencies-scripts

## Step:1 

> npm init

### Add to package.json 👇

```
{
"scripts": {
    "compile1:sass": "node-sass sass/main.scss css/style.css",
    "watch:sass": "nodemon -e scss -x \"npm run compile:sass\"",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },
  
  "devDependencies": {
    "autoprefixer": "^10.4.2",
    "concat": "^1.0.3",
    "node-sass": "^7.0.1",
    "nodemon": "^2.0.15",
    "npm-run-all": "^4.1.5",
    "postcss-cli": "^9.1.0"
  }
 }
   
```
## Step:2
### Run in CLI

> > npm install / npm i

<hr>

