# Leaf-JS
Leaf-JS is the JavaScript API for the Leaf blockchain

# Documentation

- [Install](https://github.com/LeafterMedia/leaf-js/tree/master/doc#install)
- [Browser](https://github.com/LeafterMedia/leaf-js/tree/master/doc#browser)
- [Config](https://github.com/LeafterMedia/leaf-js/tree/master/doc#config)
- [Database API](https://github.com/LeafterMedia/leaf-js/tree/master/doc#api)
    - [Subscriptions](https://github.com/LeafterMedia/leaf-js/tree/master/doc#subscriptions)
    - [Tags](https://github.com/LeafterMedia/leaf-js/tree/master/doc#tags)
    - [Blocks and transactions](https://github.com/LeafterMedia/leaf-js/tree/master/doc#blocks-and-transactions)
    - [Globals](https://github.com/LeafterMedia/leaf-js/tree/master/doc#globals)
    - [Keys](https://github.com/LeafterMedia/leaf-js/tree/master/doc#keys)
    - [Accounts](https://github.com/LeafterMedia/leaf-js/tree/master/doc#accounts)
    - [Market](https://github.com/LeafterMedia/leaf-js/tree/master/doc#market)
    - [Authority / validation](https://github.com/LeafterMedia/leaf-js/tree/master/doc#authority--validation)
    - [Votes](https://github.com/LeafterMedia/leaf-js/tree/master/doc#votes)
    - [Content](https://github.com/LeafterMedia/leaf-js/tree/master/doc#content)
    - [Witnesses](https://github.com/LeafterMedia/leaf-js/tree/master/doc#witnesses)
- [Login API](https://github.com/LeafterMedia/leaf-js/tree/master/doc#login)
- [Follow API](https://github.com/LeafterMedia/leaf-js/tree/master/doc#follow-api)
- [Broadcast API](https://github.com/LeafterMedia/leaf-js/tree/master/doc#broadcast-api)
- [Broadcast](https://github.com/LeafterMedia/leaf-js/tree/master/doc#broadcast)
- [Auth](https://github.com/LeafterMedia/leaf-js/tree/master/doc#auth)


Here is full documentation:
https://github.com/LeafterMedia/leaf-js/tree/master/doc



## Install
```
$ npm install @leafter/leaf-js
```

## Examples
### Broadcast Vote
```js
var leaf = require('leaf');

var wif = leaf.auth.toWif(username, password, 'posting');
leaf.broadcast.vote(wif, voter, author, permlink, weight, function(err, result) {
	console.log(err, result);
});
```

### Get Accounts
```js
leaf.api.getAccounts(['ned', 'dan'], function(err, result) {
	console.log(err, result);
});
```

### Get State
```js
leaf.api.getState('/trends/funny', function(err, result) {
	console.log(err, result);
});
```

### Reputation Formatter
```js
var reputation = leaf.formatter.reputation(user.reputation);
console.log(reputation);
```

## Contributions
Patches are welcome! Contributors are listed in the package.json file. Please run the tests before opening a pull request and make sure that you are passing all of them. If you would like to contribute, but don't know what to work on, check the issues list.

## Issues
When you find issues, please report them!

## License
MIT
