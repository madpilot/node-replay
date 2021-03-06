## Version 1.3.1 2012-03-15

Accept replay documents with nothing but method and path.


## Version 1.3.0 2012-03-15

Fix status code being string instead of integer.

Fix handling of fixtures with empty body.


## Version 1.2.3 2012-01-16

Support (or don't fail on) Web Sockets.

Fix non-working `Replay.localhost`.


## Version 1.2.2 2011-12-27

There may be hosts you don't care to record/replay: it doesn't matter if requests to these hosts succeed or not, and you
don't care to manage their recorded file.  You can just add those to the ignore list:

    Replay.ignore "www.google-analytics.com", "airbrake.io"

The `allow`, `ignore` and `localhost` methods now accept multiple arguments. 


## Version 1.2.1 2011-12-27

Bug fix to DNS hack.


## Version 1.2.0 2011-12-27

You can tell **node-replay** what hosts to treat as "localhost".  Requests to these hosts will be routed to 127.0.0.1,
without capturing or replay.  This is particularly useful if you're making request to a test server and want to use the
same URL as production.

For example:

    Replay.localhost "www.example.com"

Likewise, you can tell **node-reply** to allow network access to specific hosts.  These requests can still be recorded
and replayed, but will otherwise pass through to the specified host:

    Replay.allow "logger.example.com"


## Version 1.1.1 2011-12-06

Only store specific request headers (e.g. `Accept` but not `User-Agent`).


## Version 1.1.0 2011-12-05

Recorded response now starts with <method> <path>.
    
Examples:
    GET /weather?c=94606
    POST /posts


## Version 1.0.1 2011-12-05

Fix pathname and support matching request headers.


## Version 1.0.0 2011-12-02

First, almost does something interesting, check in.
