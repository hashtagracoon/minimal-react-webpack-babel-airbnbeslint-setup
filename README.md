# eslint config - airbnb versus create-reat-app
I need to compare how [eslint](http://eslint.org) configuration in [create-react-app](https://github.com/facebookincubator/create-react-app/tree/master/packages/eslint-config-react-app) is different with [airbnb one](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb/rules).

To play with airbnb's eslint, I combine this great [tutorial](https://robinwieruch.de/react-eslint-webpack-babel/) from [@rwieruch](https://github.com/rwieruch) and his [minimum react setup repo](https://github.com/rwieruch/minimal-react-webpack-babel-setup)

## Some notes
- airbnb's eslint is more opinionated than [creat-react-app's one](https://github.com/facebookincubator/create-react-app/blob/master/packages/eslint-config-react-app/index.js#L10). 
- Airbnb's will be good for team which need [enforce code style and code conventions](https://github.com/facebookincubator/create-react-app/issues/205) and find out that it closes to what they need.
- Creat-react-app is less opinionated so it's easier for new developer.

## My custom eslint rule
I have some custom rules on top of airbnb one:

- Enable jsx in js file.
- No comma at the end of file. I used to add `;` until I dicover the code style without it from http://redux.js.org/ . My personal opinion is `;` make code looks more busy without adding value.

```json
{
  "extends": "airbnb",
  "rules": {
    "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx"] }],
    "semi": [2, "never"],
  }
}
```

# minimal-react-webpack-babel-setup

* `git clone git@github.com:rwieruch/minimal-react-webpack-babel-setup.git`
* cd minimal-react-webpack-babel-setup
* npm install
* npm start

Read more: [Minimal Setup Tutorial](https://www.robinwieruch.de/minimal-react-webpack-babel-setup/)