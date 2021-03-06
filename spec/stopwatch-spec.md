# Unit Spec : `Stopwatch`

## `advanceTheClock`

```markdown
1.  If the stopwatch is running,
  a.  it calls `updateTimeValues`.
  b.  it sets a timeout to call itself in 10 milliseconds.
2.  If the stopwatch is not running,
  a.  it does nothing.
```

## `updateTimeValues`

```markdown
1.  It increases the number of milliseconds by ten.
2.  If the number of milliseconds reaches 1000,
  a.  it resets the number of milliseconds to zero.
  b.  it increments the number of seconds.
3.  If the number of seconds reaches 60,
  a.  it resets the number of seconds to zero.
  b.  it increments the number of minutes.
4.  It updates the browser (via `Display`) after adjusting all
    time values.
```

## `reset`

```markdown
1.  It resets the counts of minutes, seconds, and milliseconds to zero.
2.  It resets the list of laps to be empty.
```

## `start`

```markdown
1.  If the stopwatch is not running,
  a. it sets the state of the stopwatch to 'running'.
  b. it calls `advanceTheClock` in order to start the ticking of the clock.
2.  If the stopwatch is running,
  a. it does nothing.
```

## `stop`

```markdown
1.  If the stopwatch is running,
  a. it sets the state of the stopwatch to 'not running'.
2.  If the stopwatch is not running,
  a. it does nothing.
```

## `lap`

```markdown
1.  If the stopwatch is running,
  a. it adds a record of the current values of minutes (`mins`), seconds (`secs`), and milliseconds(`millisecs`) to the list of laps.
2.  If the stopwatch is not running,
  a. it does nothing.
```
