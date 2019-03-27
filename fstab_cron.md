## FSTAB







## CRONTAB:

- Cada hora en punto ejecutamos la sincronización horaria y mandamos la salida a /dev/null/
~~~
* * * * * root ntpdate -u hora.roa.es > /dev/null/
~~~

- Programar un trabajo (A) para ejecutarse en el minuto 30 de cada hora de cada día.
~~~
30 * * * * root (A) >  /etc/trabajos
~~~

- Programar un trabajo (B) para ejecutarse cada día a las 20:30h.
~~~
30 20 * * * root (B) >  /etc/trabajos
~~~

- Programar un trabajo (C) para ejecutarse de lunes a viernes a las 20:30h.
~~~
30 20 * * 1,2,3,4,5 root (C) >  /etc/trabajos
~~~

- Programar un trabajo (D) para ejecutarse los martes y los jueves a las 20:30h.
~~~
30 20 * * 2,4 root (D) >  /etc/trabajos
~~~

- Programar un trabajo (E) para ejecutarse los días 10 y 20 de todos los meses a las 20:30h.
~~~
30 20 10,20 * * root (E) >  /etc/trabajos
~~~

- Programar un trabajo (F) para ejecutarse cada 15 minutos.
~~~
15 * * * * root (F) >  /etc/trabajos
~~~

- Programar un trabajo (G) para ejecutarse cada día a las 00:00h.
~~~
00 0 * * * root (G) >  /etc/trabajos
~~~

- Programar un trabajo (H) para ejecutarse cada primer día de mes a las 00:00h.
~~~
00 0 1 * * root (H) >  /etc/trabajos
~~~
