# telltime
Cli tool for interacting with Daypack-lib components

## Examples

#### Get exact time after some duration from now

```
$ telltime from-now "1 hour"
Now                   : 2020-09-03 15:53:29
Duration (original)   : 1 hour
Duration (normalized) : 1 hours 0 mins 0 secs
Now + duration        : 2020-09-03 16:53:29
```

```
$ telltime from-now "1.5 hour"
Now                   : 2020-09-03 15:54:24
Duration (original)   : 1.5 hour
Duration (normalized) : 1 hours 30 mins 0 secs
Now + duration        : 2020-09-03 17:24:24
```

```
$ telltime from-now "1.5 days 2.7 hours 0.5 minutes"
Now                   : 2020-09-03 15:55:43
Duration (original)   : 1.5 days 2.7 hours 0.5 minutes
Duration (normalized) : 1 days 14 hours 42 mins 30 secs
Now + duration        : 2020-09-05 06:38:13
```

## Possible uses

- For scripts to check if time is within time slots specified by time expression
- Looking up the exact date for sentences we often use, e.g. "thu 9am to 12pm"
- Do some operations over time slots, set operators such as `&&` (intersect), `||` (union) are available

## Online demo

- The engine that evaluates the time expression can be accessed via this online [demo](https://daypack-dev.github.io/time-expr-demo/)
- Note that the online demo may be more limiting than `telltime` itself, due to memory space restriction of JS being run in a browser
  - In other words, if `telltime` might still return something useful even if the demo failed for a particular input
