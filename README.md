# Go Gin Example [![rcard](https://goreportcard.com/badge/github.com/shinydev1992/Golang-Gin-RESTful-APIs)](https://goreportcard.com/report/github.com/shinydev1992/Golang-Gin-RESTful-APIs) [![GoDoc](http://img.shields.io/badge/go-documentation-blue.svg?style=flat-square)](https://godoc.org/github.com/shinydev1992/Golang-Gin-RESTful-APIs) [![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/shinydev1992/Golang-Gin-RESTful-APIs/master/LICENSE)

An example of gin contains many useful features

[简体中文](https://github.com/shinydev1992/Golang-Gin-RESTful-APIs/blob/master/README_ZH.md)

## Installation
```
$ go get github.com/shinydev1992/Golang-Gin-RESTful-APIs
```

## How to run

### Required

- Mysql
- Redis

### Ready

Create a **blog database** and import [SQL](https://github.com/shinydev1992/Golang-Gin-RESTful-APIs/blob/master/docs/sql/blog.sql)

### Conf

You should modify `conf/app.ini`

```
[database]
Type = mysql
User = root
Password =
Host = 127.0.0.1:3306
Name = blog
TablePrefix = blog_

[redis]
Host = 127.0.0.1:6379
Password =
MaxIdle = 30
MaxActive = 30
IdleTimeout = 200
...
```

### Run
```
$ cd $GOPATH/src/Golang-Gin-RESTful-APIs

$ go run main.go 
```

Project information and existing API

```
[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /auth                     --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/routers/api.GetAuth (3 handlers)
[GIN-debug] GET    /swagger/*any             --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/vendor/github.com/swaggo/gin-swagger.WrapHandler.func1 (3 handlers)
[GIN-debug] GET    /api/v1/tags              --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.GetTags (4 handlers)
[GIN-debug] POST   /api/v1/tags              --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.AddTag (4 handlers)
[GIN-debug] PUT    /api/v1/tags/:id          --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.EditTag (4 handlers)
[GIN-debug] DELETE /api/v1/tags/:id          --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.DeleteTag (4 handlers)
[GIN-debug] GET    /api/v1/articles          --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.GetArticles (4 handlers)
[GIN-debug] GET    /api/v1/articles/:id      --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.GetArticle (4 handlers)
[GIN-debug] POST   /api/v1/articles          --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.AddArticle (4 handlers)
[GIN-debug] PUT    /api/v1/articles/:id      --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.EditArticle (4 handlers)
[GIN-debug] DELETE /api/v1/articles/:id      --> github.com/shinydev1992/Golang-Gin-RESTful-APIs/api/v1.DeleteArticle (4 handlers)

Listening port is 8000
Actual pid is 4393
```
Swagger doc

![image](https://i.imgur.com/bVRLTP4.jpg)

## Features

- RESTful API
- Gorm
- Swagger
- logging
- Jwt-go
- Gin
- Graceful restart or stop (fvbock/endless)
- App configurable
- Cron
- Redis
