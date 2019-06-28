# Go GraphQL Demo

This project is a playground to try out GraphQL with Go using [graphql-go/graphql](https://github.com/graphql-go/graphql)

Inspired by [The Polyglot Developer](https://www.thepolyglotdeveloper.com/2018/05/getting-started-graphql-golang/)


```
$ curl -g 'http://localhost:8080/graphql?query={songs(album:"ts-fearless"){album,title,duration}}'

{
    "data": {
        "songs": [{
            "album": "ts-fearless",
            "duration": "4:01",
            "title": "Fearless"
        }, {
            "album": "ts-fearless",
            "duration": "4:54",
            "title": "Fifteen"
        }]
    }
}
```

```
curl -g 'http://localhost:8080/graphql?query=mutation+_{createSong(id:"7",album:"ts-fearless",title:"Breathe",duration:"4:23"){title,duration}}'

{
  "data": {
    "createSong": {
      "duration": "4:23",
      "title": "Breathe"
    }
  }
}
```