####An exercise in taking a terribly insecure blog (original reademe below) and making it better!

My New Blog!

I've got a lot to say, and now I have a place to say it!!!!!

Read all my amazing posts!!!!! You can load them into the app with: `rake load_blog:load_shit`

Since I know you want to read them all, I designed my page to show EVERYTHING on the front page of the site!!!!!

I know it is a little slow (but totes worth it!!!!)... _Do you know how I can make it faster?_

XSS:
```
http://localhost:3000/posts?utf8=%E2%9C%93&search=archive&status=foo=%22bar%22%3E%3Cscript%3Ealert%28%22p0wned!!!%22%29%3C/script%3E%3Cp%20data-foo
```

SQL Injection:

```
foo%'); INSERT INTO posts (id,title,body,created_at,updated_at) VALUES (99,'hacked','hacked alright','2013-07-18','2013-07-18'); SELECT "posts".* FROM 