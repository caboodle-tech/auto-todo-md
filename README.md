# Auto To-Do MD (ATM)
A fast and convenient way to automatically build a project to-do list from developers comments. As your developers work on your project make sure they add to-do items like so:

> // TODO: Comment safe for most types of files.
>
> \<!-- // TODO: Comment you'll have to do for HTML files. --\>

The word `TODO` does not have to be capitalized but it must always have `//` before it and `:` after it.

After you run ATM on your project these comments will be replaced with ATM formatted to-do comments that have a unique ID assigned to each item. This ID is the magic that makes ATM so useful, especially for a remote team! If your team uses a version control system such as git you can use these ID's as the prefix to branch names.  Take a look at ATM's [TO-DO List](TODO.md) for an example.

# Installation
Auto To-Do MD (ATM) has been designed to run from a single file; currently we support only Command Line Interfaces (CLIs) but we plan to add support for server side integration later. Copy the appropriate `todo.xxx` file from your programming languages directory into your project.

If you would like to run ATM without having to configure anything make sure to place the `todo.xxx` file inside the `/bin` directory at your projects root. If your project doesn't have a `/bin` directory you will either need to add one OR place the `todo.xxx` file inside any directory that is one directory deep from your projects root.

**EXAMPLE:** For this repository we actually use `/php/todo.php` instead of a `/bin/todo.php` like a traditional PHP project would.

# Configuration
You can customize ATM to fit your needs by altering the variables at the top of your chosen `todo.xxx` file. If your using PHP for example you would change the following variables:

```php
$path_to_project = ...;
$header_message = ...;
$file_types = array( ... );
$end_lines = array( ... );
```

# Usage
In a command line / shell / terminal navigate to the directory where you put your `todo.xxx` file and run it. In a PHP project for example, after navigating to the correct directory, you would run this command: `php -f todo.php`

**EXAMPLE:** For this project we actually navigate into the `/php` directory and run: `php -f todo.php`
