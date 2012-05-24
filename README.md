# li3_gelf
lithium Graylog2 Logger

Config:

```
use lithium\analysis\Logger;

Logger::config(array(
    'gelf' => array(
    	'adapter' => 'li3_gelf\extensions\adapter\logger\Gelf',     	
    	'host' => '33.33.33.200',   
    	'defaults' => array(
    		'key' => 'value'    		
    	)
    )
));
```

Usage:
```
Logger::write('alert', 'Short Message', array('full_message' => 'It is a log', 'facility' => 'room1', 'additional' => array('one' => 'two'))); 

additional takes an array

$_levels = array(
	'debug' 	=> 0,
	'info'  	=> 1,
	'warn'  	=> 2,
	'error' 	=> 3,
	'fatal' 	=> 4,
	'unknown' 	=> 5
);
```

Todo: Refactor, Docs, Test
