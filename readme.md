#Maintenance mode for Yii framework.

##Install
Copy extension to your folder path/to/extensions.
Add to config/main.php:

    'preload' => array('log', 'maintenanceMode'),
    ...
    'components' => array(
            'maintenanceMode' => array(
                'class' => 'ext.MaintenanceMode.MaintenanceMode',
            ),
            ...
    ),

##Options

    'maintenanceMode' => array(
        'class' => 'ext.MaintenanceMode.MaintenanceMode',
        'enabledMode' => true,
        'message' => 'Hello!',
        // or
        //'capUrl' => 'site/contact',
        // allowed users
        'users' => array('admin', ),
        // allowed roles
        'roles' => array('Administrator', ),
        // allowed IP
        'ips' => array('123.456.789.000', ),        
        // allowed urls
        'urls' => array('/site/login', '/login', ),        
    ),

