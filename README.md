# kordle-svr

## Background
This is the server that keeps track of the wordle2 results via HTTP ReST calls.

The server can be run locally or in Google's Cloud Run.  There is some configuration related to Google's App Engine, but that approach did not work well with the H2 in memory database.

## How-to

To run locally:
```
./gradlew bootRun
```

To deploy/run in Cloud Run:
```
gcloud run deploy
```

To see the data, navigate to:
```
http(s)://{host}:{port}/h2-console
```

Then find the "data can be found at jdbc:....." line in the logs and use that in the H2 Console.

## References
https://www.bezkoder.com/spring-boot-jpa-h2-example/
