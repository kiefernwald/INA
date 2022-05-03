# Kiefernwald INA

A headless CMS based on [Cockpit](https://cockpit.loc/).

### Requirements

* PHP >= 7.3
* PDO + SQLite (or MongoDB)
* GD extension
* mod_rewrite, mod_versions enabled (on apache)

make also sure that <code>$_SERVER['DOCUMENT_ROOT']</code> exists and is set correctly.


### Installation

1. Download Cockpit and put the cockpit folder in the root of your web project
2. Run `composer install`
3. Make sure that the __/cockpit/storage__ folder and all its subfolders are writable
4. Go to __/cockpit/install__ via Browser
5. You're ready to use Cockpit :-)


### Build (Only if you modify JS components)

You need [nodejs](https://nodejs.org/) installed on your system.

First run `npm install` to install development dependencies

1. Run `npm run build` - For one-time build of styles and components
2. Run `npm run watch` - For continuous build every time styles or components change


### Dockerized Development

You need docker installed on your system: https://www.docker.com.

1. Run `npm run docker-init` to build the initial image.
2. Run `npm run docker` to start an Apache environment suited for Cockpit on port 8080 (this folder mapped to /var/www/html).

## License

Licensed under the MIT license.

See [LICENSE](LICENSE) for more information.
