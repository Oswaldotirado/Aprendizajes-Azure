# Migracion a Azure

La primera tarea que se debe plantear para migrar a Azure es elaborar un plan para presetnarlo al equipo directivo con el fin de obtener respaldo y aprobacion

# Pasos que se deben de seguir para la migracion

## Evaluacion
Se tiene que hacer una evaluacion completa del entorno. Identificar que servidores, aplicaciones y servicios "pasaremos" a Azure

### Opciones de migracion

- Rehospedaje: Vuelve a crear infraestructura existente en Azure<br>
- Refactorizacion; Tralada los servicios que se ejecutan en maquinas virtuales a servicios de plataforma como Paas. Esto mejora la agilidad de la version y mantiene los costos a raya <br>
- Rediseño: Puede que se tiene que rediseñar a alguinos sistemas para que se pueda emigrar, estos rediseños pueden aprovechar los servicios de la nube, haciendo asi nuevos metodoscomo microservicios <br>
- Sustitucion: Evaluar opciones de software como servicio para remplazar las aplicaciones existentes

## Calculo de ahorro de costos
Es una parte del plan para migrar a Azure, el ahorro de costos es un importante tema a recalcar ya que el tralado a la nube ofrece un ahorrode costos con respecto a la 
ejecucion de una infraestructura local propia

## Identificacion de herraamientas
Existen varias herramientas disponibles para ayudar a planear las fases de la migracion,
puede que una migracion solo necesite usar una o dos herramientas:
- Azure Migrate
- Service Map
- Calculadora de TCO de Azure
- Azure Database Migration Service
- Herramienta de migracion de datos
- Azure Cost Management
- Azure Advisr
- Azure Monitor
- Azure Sentinel

## Azure Migrate
Es un servicio gratuito proporcionado por Microsfot que detecta, evalua y migra sistemas locales a Azure. El servicio que facilita los calculos de tamaño basados
en el rendimiento de las maquinas que se van a migrar, y la estimulacion del costo corriente de la ejecucion de estas maquinas en Azure.

## Replicacion de maquinas virtuales
Azure Migrate replica simultaneamente hasta 100 maquinas virtuales. Si necesita mas capacidad es recomendable crear varios lotes, el tiempo que se tardara
depende del numero y tamaño de las maquinas virtuales

#### Prueba de maquina virtual migrada
Una vez que se hayan replicado todas las maquinas vrituales, se pueden probar antes de migrarlas para comprobar que todo funcione

## Pasos Posteriores a la migracion
Una vez completada la migracion, se revisa la configuracion de seguridad de la maquina virtual.<br>
Se implementa el Azure Disk Encryption para proteger los discos de posibles robos de datos y accesos no autorizados

## Migracion sin xonexion y migracion en linea
El servicio de migracion facilita ods maneras distintas de migrar bases de datos de SQL server:
- Sin conexion: Requiere apagar el servidor al inicial la migracion
- Mediante migracion en linea: Sincronizacion continua de los datos 

## Destinos 
Se pueden migrar a varios destinos diferentes en Azure: <br>
- Unica instancia en SQL database (*es las mas rapida y economica*)
- Instancia administrada SQL database
- SQL server en Azure Virtual Machine (*garantiza una compatibilidad del 100% con el Motod de base de datos de SQL SERVER*)
- Azure Database for MySQL
- Azure Database for PostgresSQL
- Azure Cosmos DB

