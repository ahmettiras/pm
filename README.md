# Project Management Tool

## Information

PM tool is designed to be a basic project management tool. It's only contains most essential parts of project management such as managing users and their roles on created projects, assigning tasks and tracking the overall progress.

Since most of the good PM alternatives were written in Ruby and Java, we started to develop one with PHP to enable ease of maintenance for PHP developers.

Built on [Scabbia Framework 1.5](https://github.com/larukedi/Scabbia-Framework).


## Installation

**Step 1:**

On Terminal or Command Prompt:
``` bash
git clone https://github.com/larukedi/pm pm
```

Alternatively [PM](https://github.com/larukedi/pm/archive/master.zip) package can be downloaded directly.

**Step 2:**

``` bash
cd pm
cd htdocs
php scabbia update
```

**Step 3:**
Make `uploads`, `application/writable` and `application/locale` directories writable.

``` bash
chmod 0777 -R uploads
chmod 0777 -R application/writable
chmod 0777 -R application/locale
```

**Step 4:**
Import an mysql dump file depending on your language choice.
For english data: `db/en/R00_base.sql`
For turkish data: `db/tr/R00_base.sql`

**Step 5:**
Open `application/config/datasources.json` file to update the database configuration parameters.

a sample mysql database configuration:
```json
{
    "datasourceList": [
        {
            "id":           "dbconn",
            "interface":    "pdo",
            "persistent":   true,
            "overrideCase": "natural",
            "pdoString":    "mysql:host=localhost;dbname=pm",
            "username":     "root",
            "password":     "123456",
            "initCommand":  "SET NAMES utf8",
            "errors":       "exception"
        }
    ]
}
```


## Requirements
* PHP 5.3.3+ (http://www.php.net/)
* Composer Dependency Manager** (http://getcomposer.org/)
* Scabbia Framework** (http://larukedi.github.com/Scabbia-Framework/)

** Will be auto-installed during composer execution


## License
See [license.txt](license.txt)


## Contributing
It is publicly open for any contribution. Bugfixes, new features and extra modules are welcome.

* Fork the repo, push your changes to your fork, and submit a pull request.
* If something does not work, please report it using GitHub issues.
