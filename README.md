# documentacionApache
Entregable 2
Apache server fue craedo en 1995 por la compañia Apache Software Foundation. Hoy en dia el servidor de apache es uno de los mas usados, ya que lo usa el 46% de las páginas web en todo el mundo.

## Index


## Instalar Apache

Para empezar debemos debemos introducir el siguiente comando
~~~
sudo apt install apache2
~~~
Una vez creado comprobamos el estado
~~~
sudo systemctl status apache2
~~~
![status ](status.png)

Aqui podemos ver el directorio donde se guarda todo.

Para dar permisos ("www-data" esto es el grupo)("ubuntu" y esto es el usuario).
~~~
sudo usermod -a -G www-data ubuntu
~~~
despues de esto tenemos que reiniciar, es decir exit y despues volvemos a poner el ssh.
para saber en los grupos que estas en ubuntu
~~~
groups
~~~
para que la web se vea

para poner el puerto 
~~~
sudo nano /etc/apache2/sites-available/taller.conf
~~~
y a continuacion
~~~
<VirtualHost *:80>
  DocumentRoot /var/www/html/taller
</VirtualHost>
~~~
para poder vcerla tenemos que poner el siguiente comando
~~~
sudo a2ensite taller
~~~
para desabilitar una pagina
~~~
sudo a2dissite 000-default
~~~

