# publik_altenatif
Laravel 7 - Folder publik alternatif untuk shared hosting

The point of this Gist is to help setting up Laravel on a shared hosting setup, where you'd might need to have your `./public` folder in another structure due to the hosting setup, but still keep the application itself out of the document root/public html folder.

The directory structure presented below is just an example, showing the document root/public html folder next to the Laravel application. The configurations displayed in the files below matches this structure.

Additionally, the changes in `server.php` allows for you to have the same directory structure when working locally with `artisan serve` (if you are using this).

I've added `//` comments in the files below on the lines where I changed any references and I've marked, in the tree structure below, where you find the files you need to update.

```
shared_hosting/ <- Your root directory (not document root/public html folder).
├── laravel/
│   ├── README.md
│   ├── app/
│   │   └──Providers/
│   │       └── AppServiceProvider.php <- Change this file
│   ├── artisan
│   ├── bootstrap/
│   ├── composer.json
│   ├── composer.lock
│   ├── config/
│   ├── database/
│   ├── package.json
│   ├── phpunit.xml
│   ├── resources/
│   ├── routes/
│   ├── server.php <- Change this file
│   ├── storage/
│   ├── tests/
│   ├── vendor/
│   └── webpack.mix.js
└── public_html/
    ├── favicon.ico
    ├── index.php <- Change this file
    ├── robots.txt
    └── web.config
