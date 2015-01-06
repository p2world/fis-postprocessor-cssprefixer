# fis-postprocessor-cssprefixer

a postprocessor for fis to autoprefixer css with [postcss/autoprefixer](https://github.com/postcss/autoprefixer)

1. install fis-postprocessor-cssprefixer
```bash
npm install -g fis-postprocessor-cssprefixer
```
2. modify fis-conf.js
```javascript
fis.config.set('modules.postprocessor.css', 'cssprefixer');
```
3. set the browsers option of `postcss/autoprefixer`
```javascript
fis.config.merge({
    settings : {
        postprocessor : {
          cssprefixer : {
              // detail config (https://github.com/postcss/autoprefixer#browsers)
              "browsers": ['FireFox > 1','Chrome > 1',"ie >= 8"]
            }
        }
    }
});
```
4. fis release
`fis release`
