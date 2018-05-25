rebar_auto_plugin
=====

A rebar3 plugin for auto running compile on source file change reloading modules in the shell.

Prerequisite
-----
On Linux you need to install inotify-tools.


Use
---

Add the plugin only to your user local rebar config in `~/.config/rebar3/rebar.config`:

    {plugins, [rebar3_auto]}.

If you add it to your project rebar.config, it will get unloaded each time compilation occurs, thus breaking it.

Then run
```
    $ rebar3 compile
```

Then just call your plugin directly in an existing application:


```
$ rebar3 auto
===> Verifying dependencies...
...
Erlang/OTP 20 [erts-9.3] [source] [64-bit] [smp:8:8] [ds:8:8:10] [async-threads:0] [hipe] [kernel-poll:false] [dtrace]

Eshell V9.3  (abort with ^G)
1> ===> The rebar3 shell is a development tool; to deploy applications in production, consider using releases (http://www.rebar3.org/docs/releases)
...
```
