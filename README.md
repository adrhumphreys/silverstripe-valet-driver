# Silverstripe Valet Driver

To install create a copy of the driver in ~./valet

You need to specify fastcgi_buffers, and fastcgi_buffer_size in valet.conf.
/usr/local/etc/nginx/valet/valet.conf

```
location ~ \.php$ {
  # added params:
  fastcgi_buffers 16 16k;
  fastcgi_buffer_size 32k;
}
```

Be sure to do a "valet restart" once you've added those parameters to put them into effect.
