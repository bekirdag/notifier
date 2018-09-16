# DemocracyOS API Notifier

API Notifications with agenda and nodemailer

## Configuration
- Install dependencies

```sh
$ npm install
```

- Set environment variables

```
MONGO_URL='mongodb://<my-mongo-url>/<database-name>'
ORGANIZATION_EMAIL=your-organization@mail.com
ORGANIZATION_NAME='My Organization'
NODEMAILER_HOST=your.host.com
NODEMAILER_PASS=yourservicemailpass
NODEMAILER_USER=yourservice@mail.com
```

## ¡Run server, run!

```sh
$ npm run dev
```

Server will run on port 3000.
At the moment, try make a POST request to 

```
/api/sendemail
```

with this body structure

```javascript
{
	"type":"the-type",
	"info": {
		"to":"the-email-to@notify.com",
		"document": {
			"comment":"The original comment",
			"title":"The document title",
			"author":"The document author"
		}
	}
}
```

Currently there are three types of notifications: "comment-resolved", "comment-liked", "document-edited"