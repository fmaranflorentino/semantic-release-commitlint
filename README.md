- `npm install --save-dev @commitlint/config-conventional @commitlint/cli`

create `commitlint.config.js` file on your project root folder

```js
module.exports = {
  extends: ["@commitlint/config-conventional"],
};
```

- `npm install --save-dev commitizen`

- `npm install --save-dev husky`

In your `package.json` add the following objects

```json
 "config": {
    "commitizen": {
      "path": "cz-conventional-changelog"
    }
  },
 "husky": {
   "hooks": {
     "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
   }
 }
```

You can also add `git-cz` on your scripts object

```json
"scripts": {
  "commit": "git-cz"
}
```
