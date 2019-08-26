# thrift-hbase-laravel

## Install
    
    composer require honvid/thrift-hbase-laravel

Changes to `config/app.php`
    
    'providers' => [
        ...
        Honvid\Providers\ThriftServiceProvider::class    
    ],
    'aliases' => [
        ...
        'Thrift' => Honvid\Facades\Thrift::class
    ]

Run Command to add Config file (config/thrift.php),  Change the Host and Port to the Thrift using Config file.

    php artisan vendor:publish --provider="Honvid\Providers\ThriftServiceProvider"

    
Uses Example 
    
    use Honvid\Facades\Thrift;
    
    ...
    
    
    Thrift::getValue('table1', 'column_Family', 'Key/Row Identifier', [<Column indexes to be returned, empty for all>]]);
