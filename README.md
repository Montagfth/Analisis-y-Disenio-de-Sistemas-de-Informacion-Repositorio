# Analisis & Diseño de Sistemas de Informacion | Proyecto Final
###### Programador(es): Montañez Fabrizio - Quispe Angelo - Chipana Milenka - Flores Gabriel
Sistema de gestión de servicios para TESLA Motors Inc. desarrollado como proyecto final del curso.   
  
## Arquitectura del Sistema  
### Arquitectura en Capas  
- **Capa de Presentación**: Swing UI con panels administrativos e informativos  
- **Capa de Controlador**: MVC controllers (parcialmente implementado)  
- **Capa de Lógica de Negocio**: Gestión de sesiones y validaciones  
- **Capa de Acceso a Datos**: DAOs para MySQL y MongoDB  
- **Capa de Persistencia**: Base de datos relacional y documental  
  
### Stack Tecnológico  
| Tecnología | Versión | Propósito |  
|------------|---------|----------|  
| Java | 23 | Lenguaje principal |  
| MySQL | 8.0.33 | Base de datos relacional |  
| MongoDB | 3.11.0-beta4 | Base de datos documental |  
| Maven | - | Gestión de dependencias |  
| Swing | - | Interfaz de escritorio |  
| FlatLaf | 3.6 | Look & Feel moderno |  
  
## Servicios del Sistema  
### Servicio 1: Venta de Autos (ReservaServUno)  
- Gestión de reservas y ventas de vehículos TESLA  
- Control de inventario y estados de reserva  
  
### Servicio 2: Venta de Autopartes (ReservaServDos)    
- Solicitudes de autopartes con verificación de stock  
- Seguimiento de fulfillment de pedidos  
  
### Servicio 3: Mantenimiento (ReservaServTres)  
- Citas de mantenimiento para vehículos TESLA y de otras marcas  
- Asignación de técnicos y captura condicional de datos  
  
## Estructura de Base de Datos  
### MySQL: `basededatosiiproyecto`  
- **cliente**: Información de clientes  
- **administrador**: Usuarios administrativos  
- **empleado**: Técnicos y personal  
- **auto**: Catálogo de vehículos  
- **autopartes**: Inventario de repuestos  
- **reservaservuno**: Reservas de venta de autos  
- **reservaservdos**: Solicitudes de autopartes  
- **reservaservtres**: Citas de mantenimiento  
  
### MongoDB: `dbproyectobasededatosii`  
- **pruebacomentario**: Feedback y calificaciones de clientes  
  
## Roles de Usuario  
- **Cliente**: Navegar inventario, crear reservas, enviar feedback  
- **Administrador**: Acceso completo al panel administrativo, operaciones CRUD  
- **Empleado**: Asignado a tareas de mantenimiento, acceso limitado  
  
## Instalación y Configuración  
### Prerrequisitos  
- Java 23 o superior  
- MySQL 8.0+  
- MongoDB 4.4+  
- Maven 3.6+  
  
### Configuración de Base de Datos  
1. Crear base de datos MySQL: `BaseDeDatosIIProyecto`  
2. Ejecutar script SQL para crear tablas  
3. Configurar conexión en `Database.java`  
4. Crear base de datos MongoDB: `dbproyectobasededatosii`  
  
### Ejecución  
`bash`

### Estructura & Paqueteria

```
src/main/java/  
├── Administrative/  
│   └── panelAdministrator.java  
├── Controller/  
│   └── ClienteControlador.java  
├── Database/  
│   ├── Database.java  
│   ├── DatabaseNOSQL.java  
│   └── Sesion.java  
├── DatabaseModels/  
│   ├── Cliente.java  
│   ├── Empleado.java  
│   ├── Auto.java  
│   └── [Otros modelos]  
├── InformativePanels/  
│   ├── Informativo01.java  
│   ├── Informativo02.java  
│   ├── Informativo03.java  
│   └── Informativo04.java  
├── Comentarios/  
│   └── DialogComentarios.java  
└── Services/  
    ├── panelService1.java  
    ├── panelService2.java  
    └── panelService3.java
```

### Características Destacadas
- Arquitectura poliglota con MySQL y MongoDB
- Gestión de sesiones con roles diferenciados
- Captura condicional de datos según tipo de vehículo
- Sistema de feedback con calificación por estrellas
- Interfaz moderna con FlatLaf

### Estado del Proyecto
✅ Base de datos implementada y probada
✅ Capa de presentación funcional
✅ Conectividad con bases de datos
⏳ Controladores MVC por implementar
⏳ Tests unitarios pendientes


