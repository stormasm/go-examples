
In Golang one can not set an ENVIRONMENT variable in a parent process.

You can only set an ENVIRONMENT variable for the currently running process
that this particular go process is running inside...

Therefore to set an ENVIRONMENT variable system wide or in the parent
process one must write out a file with a name like .influxenv

And then come along and source that file with the environment variable in it
just like you would other files with environment variables in it like .profile

So you must source the file that gets written out.  My standard way
of sourcing files is to run an alias called **sp**

#### TO build the binary

```
go build -o exportenv *.go
```
