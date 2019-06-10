<a href="https://www.npmjs.com/package/@awesomeeng/awesome-cli">![npm](https://img.shields.io/npm/v/@awesomeeng/awesome-cli.svg "npm Details")</a>
<a href="./LICENSE">![GitHub](https://img.shields.io/github/license/awesomeeng/awesome-cli.svg "License Details")</a>
<a href="http://npm-stats.com/~packages/@awesomeeng/awesome-cli">![npm](https://img.shields.io/npm/dt/@awesomeeng/awesome-cli.svg "npm download stats")</a>
<a href="https://github.com/awesomeeng/awesome-cli/graphs/contributors">![GitHub contributors](https://img.shields.io/github/contributors-anon/awesomeeng/awesome-cli.svg "Github Contributors")</a>
<a href="https://github.com/awesomeeng/awesome-cli/commits/master">![GitHub last commit](https://img.shields.io/github/last-commit/awesomeeng/awesome-cli.svg "Github Commit Log")</a>
<br/><a href="https://nodejs.org/en/">![node](https://img.shields.io/node/v/@awesomeeng/awesome-cli.svg "NodeJS")</a>
<a href="https://github.com/awesomeeng/awesome-cli/issues">![GitHub issues](https://img.shields.io/github/issues/awesomeeng/awesome-cli.svg "Github Issues")</a>
<a href="https://snyk.io/vuln/search?type=npm&q=@awesomeeng/awesome-cli">![Snyk Vulnerabilities for GitHub Repo](https://img.shields.io/snyk/vulnerabilities/github/awesomeeng/awesome-cli.svg "Synk Vulnerabilities Database")</a>
<a href="https://www.npmjs.com/package/@awesomeeng/awesome-cli">![David](https://img.shields.io/david/awesomeeng/awesome-cli.svg)</a>

# AwesomeCLI

AwesomeCLI is a simple framework for building enterprise Command Line Interface (CLI) tools. It supports standard or command based CLI interaction, global and local switches/options, and useful utilities to speed your tool development time.  It's all your cLI needs in one.

## Features

# AwesomeStack

AwesomeStack is an application stack for building enterprise nodejs applications.  It provides a set of libraries for delivering stable, secure, and performant applications in a fast and reliable manner.

AwesomeStack includes...

 - **[AwesomeServer](https://github.com/awesomeeng/awesome-server)** - A HTTP/HTTPS/HTTP2 API Server focused on implementing API endpoints.

 - **[AwesomeLog](https://github.com/awesomeeng/awesome-log)** - Performant Logging for your application needs.

 - **[AwesomeConfig](https://github.com/awesomeeng/awesome-config)** - Powerful configuration for your application.

 - **[AwesomeCLI](https://github.com/awesomeeng/awesome-cli)** - Rapidly implement Command Line Interfaces (CLI) for your application.

All AwesomeStack libraries and AwesomeStack itself is completely free and open source (MIT license) and has zero external dependencies. This means you can have confidence in your stack and not spend time worrying about licensing and code changing out from under you. Additionally, AwesomeStack and This means consistency of code throughout the product, safer code, and better support for you and your product. are maintained by The Awesome Engineering Company ensuring you a single point of contact and responsibility and unified support for your entire application.

You can learn more about AwesomeStack here: https://github.com/awesomeeng/awesome-stack

## Usage

You use AwesomeStack by installing it via npm and then requiring the module you need for what you are doing:

```shell
npm install @awesomeeng/awesome-stack
```

```javascript
let Log = require("@awesomeeng/awesome-log");
Log.start();

let config = require("@awesomeeng/awesome-config");
config().init();
config().add({
	http: {
		hostname: "localhost",
		port: 4000
	}
});
config().start();

let server = require("@awesomeeng/awesome-server");
server.addHTTPServer(config.http);
server.route("*","*",(path,request,response)=>{
	Log.access("Request "+request.method+" "+request.path+" from "+request.origin+".");
});
server.route("get","/test",(path,request,response)=>{
	return response.writeText("Hello world!");
});
```

## Not Using AwesomeStack

You can use AwesomeStack libraries (AwesomeServer, AwesomeLog, AwesomeConfig, AwesomeCLI) independantly from AwesomeStack, as needed. However, using AwesomeStack together provides you a more unified system with less points of failure and a single source of "truth". Its up to you.

## The Awesome Engineering Company

AwesomeServer is written and maintained by The Awesome Engineering Company. We belive in building clean, configurable, creative software for engineers and architects and customers.

To learn more about The Awesome Engineering Company and our suite of products, visit us on the web at https://awesomeeng.com.

## Support and Help

This product is maintained and supported by The Awesome Engineering Company.  For support please [file an issue](./issues) or contact us via our Webiste at [https://awesomeeng.com](https://awesomeeng.com).  We will do our best to respond to you in a timely fashion.

## License

AwesomeServer is released under the MIT License. Please read the  [LICENSE](./LICENSE) file for details.
