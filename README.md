Ports and Services
Not everything is as straightforward as the idealistic world of Docker would have you believe. The "one process per container" doesn't really work for us in the real world so we've gone with "one logical service per container" instead.

We use Supervisord to bootstrap the following services in our Nginx PHP-FPM web mode container:

Service	Description	Port/Socket
Nginx	Web server	0.0.0.0:80
PHP-FPM	PHP running as a pool of workers	/run/php.sock

Liecense: ccweb