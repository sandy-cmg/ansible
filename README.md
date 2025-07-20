# ansible
Se usara ansible como herramienta de automatización para algunos servicios básico que usan las entidades hoy en día, principalmente las de cuba. Poco a poco se actualizarán a medida que se incorporen más de ellos. Aclarar que todos los sistemas operativos para el despliegue están sobre Debian12, La guía de automatización para el caso objeto de estudio será: 
-	Creación de un usuario para el despliegue de los playbooks en los servidores remotos.
-	Configuración de fail2ban para la prevención de ataques remoto, inicialmente para los servicios de ssh y correo.
-	Despliegue de servidores proxy (Padres e Hijos) con funcionalidad de Round Robin.
-	Actualización de sistemas operativos.
De forma general los proxy trabajan en la combinación padres/hijos, los hijos usan Round Robin para las peticiones a sus padres, se usó un solo role, aunque hay miles de forma de hacer esta tarea, decidí hacerlo de esta vía, en la definición de las variables se especifica claramente de donde es cada una y a través de las condiciones en el fichero de configuración igual se aclara.
