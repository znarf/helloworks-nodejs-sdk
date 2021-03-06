# HelloWorks Node.js SDK

> A Node.js SDK for easily creating and managing [HelloWorks][external_helloworks] workflow instances.

[![Npm version][badge_npm-version]][external_npm]
[![Travis][badge_travis]][external_travis]
[![David][badge_david]][external_david]

<br/>

## Usage

Start by installing the HelloWorks SDK from [npm](https://npmjs.com).

```bash
npm install helloworks-sdk
```

In your backend app, require the `helloworks-sdk` library and instantiate a new client with your API key ID and secret.

```js
const HelloWorks = require('helloworks-sdk');

const client = new HelloWorks({
  apiKeyId,
  apiKeySecret,
});
```

Use the client to easily make HelloWorks API requests without the overhead of handling responses and managing JWT authorization.

```js
client.workflowInstances.getInstance({
  instanceId,
}).then((instanceObj) => {
  // ...
});
```

More examples and documentation can be found in the [API Documentation][wiki_api-documentation] Wiki page.

**Note:** It should go without saying that this library must **never be used on the client side** of your application. The HelloWorks Node.js SDK relies on sensitive API keys and by using it on the public-facing frontend codebase you will risk dangerously exposing your API key secret, which will make you vulnerable to impersonation attacks.


## Resources

* [API Documentation][wiki_api-documentation]
* [Changelog][changelog]

<br/>
<br/>
<hr/>

&copy; 2019 [HelloSign][external_hellosign]. All rights reserved.






[changelog]: https://github.com/hellosign/helloworks-nodejs-sdk/blob/master/CHANGELOG.md

[badge_npm-version]: https://img.shields.io/npm/v/helloworks-sdk.svg
[badge_david]: https://img.shields.io/david/hellosign/helloworks-nodejs-sdk.svg
[badge_travis]: https://img.shields.io/travis/hellosign/helloworks-nodejs-sdk/master.svg

[wiki_api-documentation]: https://github.com/hellosign/helloworks-nodejs-sdk/wiki/API-Documentation

[external_david]: https://david-dm.org/hellosign/helloworks-nodejs-sdk
[external_demo]: https://app.hellosign.com/api/embeddedTest
[external_hellosign]: https://hellosign.com
[external_helloworks]: https://hellosign.com
[external_npm]: https://npmjs.org/package/helloworks-sdk
[external_travis]: https://travis-ci.org/hellosign/helloworks-nodejs-sdk?branch=master
