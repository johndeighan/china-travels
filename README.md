China Travels
=============

Building:

```bash
$ cd ~
$ hugo new site china-travels
$ cd china-travels
$ npm init
$ git init
$ git branch -M main
$ git submodule add https://github.com/janraasch/hugo-bearblog.git themes/hugo-bearblog
```

Change `package.json` to:

```json
{
	"name": "<GitHub username>/china-travels",
	"version": "1.0.0",
	"type": "module",
	"description": "Document China travels",
	"scripts": {
		"test": "echo \"Error: no test specified\" && exit 1",
		"serve": "hugo serve",
		"start": "npm run serve"
	},
	"keywords": [
		"hugo"
	],
	"author": "<your name>",
	"license": "MIT"
}
```

Change `hugo.toml` to:

```toml
baseURL = 'https://<GitHub username>.github.io/'
languageCode = 'en-us'
title = '<your title>'
theme = 'hugo-bearblog'
```

Create a new top level page:

```bash
$ hugo new about.md
```

Create a blog post:

```bash
$ hugo new blog/intro.md
```

Edit the file content/posts/intro.md to introduce yourself

Test out the web site locally with:

```bash
$ hugo
```

Download images from my cell phone
----------------------------------

Connect computer to cell phone with USB cable.
USE THE WHITE CABLE!!!
On cell phone:
	go to Settings
	Click on "Search settings"
	Enter 'usb'
	Click on "USB Preferences"
	Select "File transfer

The phone will show up on your computer as an external drive
Browser to DCIM/Camera to view photos

Move desired photos to folder `assets`

Add an image
------------

```markdown
{{< figure src="/ice_cream.jpg" width="200" >}}
```

```bash
$ npm install @jdeighan/llutils
```

Create file `.gitignore`:

```text
logs/
node_modules/
typings/
*.tsbuildinfo
.npm

# dotenv environment variables file
.env
.env.test

test/temp*.*
```

Create file `.npmrc`:

```text
engine-strict=true
loglevel=silent
```

