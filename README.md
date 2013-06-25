# how to use

Setup application.

```
bundle install
rackup
```

Post markdown data.

```
echo "# title\n\ncontent" | curl http://localhost:9292 -i --data-binary @-
```

You'll get a response like below.

```
HTTP/1.1 200 OK
X-Frame-Options: SAMEORIGIN
X-Xss-Protection: 1; mode=block
X-Content-Type-Options: nosniff
Content-Type: text/html;charset=utf-8
Content-Length: 31
Server: WEBrick/1.3.1 (Ruby/2.0.0/2013-05-14)
Date: Tue, 25 Jun 2013 00:08:15 GMT
Connection: Keep-Alive

<h1>title</h1>

<p>content</p>
```

For production.

```
heroku create {app_name_you_want}
git push heroku master
```
