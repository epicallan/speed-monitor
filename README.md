![Screenshot](https://raw.githubusercontent.com/jacted/speed-monitor/master/example/screenshot1.png)

More screenshots in ```examples/```

## Introduction

- Website performance reports for slack
- Captures performance stats using ```performance.timing``` 
- Messages will be posted to default channel (config.slack.channel) or the channel where the message came from, including users.
- Discuss on [Hacker News](https://news.ycombinator.com/item?id=12438895)
- This is NOT a NodeJS package.

## Stack

> - NodeJS
> - MongoDB (Get one free at mlab.com)

## Getting started

1. Clone repository

2. Use npm to install dependencies:

	```
	npm install
	```

3. Add slack bot ```https://my.slack.com/services/new/bot```

4. Edit app/config.example.js and rename to app/config.js

5. Insert script tags at the bottom of your website right before ```</body>```

	```
	<script type="text/javascript">
		var speedmonitorUxMonitorBeaconUrl = 'http://localhost:8080/log';
	</script>
	<script type="text/javascript" src="http://localhost:8080/speedmonitor.js" defer></script>
	```

6. Invite bot to #general (or the one set in the config)

7. Run ```node index.js``` (or use something like pm2)

## Commands
- ```speed help``` shows explanations
- ```speed report``` shows report
- ```speed report full``` shows extended report

## ToDo

- [ ] Multiple domain support
- [ ] Clean up code
- [ ] Multiple database options
- [ ] Add more commands
- [X] Better README.md

## License
The MIT License (MIT)

Copyright (c) 2016 Jacob (Jacted)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.