# Print In Tables

If you're making a terminal-based application with Ruby, you'll likely want to include a "help" command listing all of the functions your app can perform.
Normally, this results in a list with awkward formating being printed to the console.
A solution? [pretty_table](https://github.com/jwulff/pretty_table).

This is a gem that will allow you to easily print large amounts of data in nicely formated tables. Interested? Here's how it works:

First, establish the required gem and setup your headers for your table.
```ruby
require "pretty_table"

headers = ['Header 1', 'Header 2']
```

Then, enter your data with the entries for different headers separated by commas.
```ruby
data = [
  ["this is under the first header", "this is under the second"],
  ["this is also under the first", "this is also under the second"]
]
```

Finally, print your new table.
```ruby
puts PrettyTable.new(data, headers).to_s
```

And you should get something like this:
```bash
           Header 1            |           Header 2
-------------------------------+------------------------------
this is under the first header | this is under the second
this is also under the first   | this is also under the second
```
