## My fork of ruby-rsync
There's only one new method and one attr_reader, so you can better work with Rsync as server.
Now its possible to get hash of module - description pairs on given Rsync server, or access raw output data.

e.g.:
```ruby
test = Rsync.run("rsync://zabbix.ernet", "")
=> #<Rsync::Result:0x000000017c1838 @exitcode=0, @raw="zabbix         \tzabbix config directory\netc            \tmain config directory\n">
test.list_modules
=> {"zabbix"=>"zabbix config directory", "etc"=>"main config directory"}
```

[Original repository](https://github.com/jbussdieker/ruby-rsync)
