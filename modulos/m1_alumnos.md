# Proyecto Final: Sistema Integral de Control Escolar 

## Módulo 1: Alumnos (Equipo 1)

## Tabla de Contenido

1. I. Introducción y Resumen del Módulo
2. II. Contexto del Módulo
   - 2.1. Problemas que se pretenden resolver
   - 2.2. Oportunidades que se buscan aprovechar
3. III. Objetivos y Alcance
   - 3.1. Objetivo General
   - 3.2. Objetivos Específicos
   - 3.3. Límites del Módulo (Dentro del alcance)
   - 3.4. Exclusiones (Fuera del alcance)
4. IV. Requerimientos del Módulo
   - 4.1. Requerimientos Funcionales (RF)
   - 4.2. Requerimientos No Funcionales (RNF)
5. V. Actores del Módulo
6. VI. Modelado del Sistema (Diagramas UML)
   - 6.1. Diagrama de Contexto del Módulo
   - 6.2. Diagrama de Casos de Uso
   - 6.3. Diagrama de Clases
   - 6.4. Diagrama de Componentes
   - 6.5. Diagramas de Secuencia
   - 6.6. Diagrama de Estados
7. VII. Interfaz de Usuario (Wireframes / Mockups)
8. VIII. Autenticación, Autorización y Permisos del Módulo
9. IX. Glosario, Abreviaturas y Nomenclaturas
10. X. Referencias Bibliográficas

## I. Introducción y Resumen del Módulo

El **Módulo de Alumnos** comprende la interfaz de usuario y la lógica de negocio del Sistema Integral de Control Escolar  orientadas al uso directo por parte del estudiante. Este módulo centraliza las herramientas académicas y administrativas esenciales para el alumno, permitiéndole consultar su rendimiento escolar en tiempo real, autogestionar su información personal, dar seguimiento a sus trámites de reinscripción y descargar documentos oficiales (como constancias de estudio) sin necesidad de acudir presencialmente a las oficinas administrativas.

## II. Contexto del Módulo

### 2.1. Problemas que se pretenden resolver

* **Trámites presenciales lentos:** Largas filas y tiempos de espera en ventanilla para solicitar constancias de estudio o verificar el estatus de reinscripción.
* **Falta de acceso inmediato a información académica:** Dificultad para consultar horarios actualizados, boletas parciales e historial académico desde dispositivos móviles.
* **Desactualización de datos de contacto:** Registros de domicilio, teléfonos y correos alternos obsoletos por falta de un portal de autogestión.
* **Incertidumbre en trámites administrativos:** Desconocimiento del alumno sobre si su reinscripción fue aprobada, rechazada o presenta observaciones.

### 2.2. Oportunidades que se buscan aprovechar

* **Autoservicio estudiantil 24/7:** Disponibilidad continua de consultas y descargas desde cualquier ubicación y dispositivo.
* **Automatización documental:** Emisión instantánea de constancias oficiales en formato PDF con validación digital.
* **Mejora en la experiencia del estudiante (UX):** Interfaz moderna, responsiva e intuitiva que reduce la carga operativa del personal de servicios escolares.

## III. Objetivos y Alcance

### 3.1. Objetivo General

Proporcionar a los alumnos un punto de acceso unificado, intuitivo y seguro para autogestionar su perfil, consultar su información académica en tiempo real y realizar trámites administrativos institucionales.

### 3.2. Objetivos Específicos

* Permitir la autenticación segura y la actualización de datos personales y contacto del alumno.
* Facilitar la consulta en tiempo real de calificaciones del periodo, historial académico, horarios de clase y materias inscritas.
* Automatizar la generación y descarga inmediata de documentos oficiales en formato PDF, como la constancia de estudios.
* Agilizar el seguimiento y consulta del estado de los trámites de reinscripción.

### 3.3. Límites del Módulo (Dentro del alcance)

* **Autenticación y gestión de perfil:** Inicio de sesión con matrícula y contraseña, cambio de contraseña y edición de datos personales/contacto.
* **Consultas académicas:** Visualización de calificaciones parciales y finales, historial académico completo, horario semanal de clases y lista de materias inscritas en el ciclo vigente.
* **Trámites y seguimiento:** Consulta del estatus del proceso de reinscripción.
* **Descarga de documentos:** Generación y descarga directa de constancias de estudio oficiales en formato PDF.

### 3.4. Exclusiones (Fuera del alcance)

* **Captura o modificación de calificaciones:** Función exclusiva del Módulo de Profesores.
* **Validación y aprobación manual de expedientes:** Función administrativa gestionada en el Módulo de Inscripciones.
* **Configuración de grupos, aulas y catálogo de asignaturas:** Función del Módulo de Asignaturas/Materias.
* **Procesamiento de pagos bancarios en línea:** El módulo consulta estatus administrativos, pero no funciona como pasarela de pago.

## IV. Requerimientos del Módulo
### 4.1. Requerimientos Funcionales (RF)
* **RF-01 (Iniciar sesión):** El sistema permitirá al alumno autenticarse mediante su matrícula institucional y contraseña.
* **RF-02 (Actualizar datos personales):** El alumno podrá visualizar y actualizar su teléfono, correo electrónico alterno y domicilio actual.
* **RF-03 (Consultar calificaciones):** El sistema mostrará las calificaciones parciales y finales obtenidas en las materias del ciclo escolar vigente.
* **RF-04 (Consultar historial académico):** El alumno podrá consultar su historial completo de asignaturas cursadas, calificaciones finales, créditos acumulados y promedio general.
* **RF-07 (Consultar horario):** El sistema permitirá visualizar la distribución de clases asignadas por día, hora, aula y docente para el ciclo vigente.
* **RF-08 (Consultar materias inscritas):** El alumno podrá verificar la lista detallada de asignaturas asignadas en su carga académica actual.
* **RF-09 (Descargar constancia de estudios):** El sistema generará y descargará un documento PDF oficial que certifique la condición académica activa del alumno.
* **RF-10 (Cambiar contraseña):** El alumno podrá actualizar su clave de acceso previa validación de su contraseña actual.
* **RF-11 (Consultar estado de reinscripción):** El alumno podrá verificar el estatus actual de su trámite de reinscripción (*En proceso, Aprobado, Rechazado* o *Con observaciones*).

### 4.2. Requerimientos No Funcionales (RNF)

* **RNF-01 (Autenticación):** El sistema debe requerir credenciales válidas y vigentes para permitir el acceso al módulo.
* **RNF-02 (Cifrado de contraseñas):** Las contraseñas almacenadas deben protegerse mediante algoritmos de hash criptográfico seguros (ej. *bcrypt* o *Argon2*).
* **RNF-03 (Sesiones expiradas):** La sesión del alumno se cerrará automáticamente tras 15 minutos de inactividad para proteger su privacidad.
* **RNF-04 (Tiempo de respuesta):** Las peticiones de consulta académica deben responder en un tiempo menor a 5 segundos en condiciones normales de tráfico.
* **RNF-05 (Generación de PDF):** La generación y descarga de la constancia de estudios en formato PDF no debe tomar más de 3 segundos.
* **RNF-06 (Disponibilidad):** El módulo debe mantener una disponibilidad mínima del 99% durante los periodos críticos de reinscripción y cierre de semestre.
* **RNF-07 (Diseño responsivo):** La interfaz debe adaptarse correctamente a dispositivos móviles, tabletas y computadoras de escritorio.
* **RNF-08 (Accesibilidad):** Los elementos visuales deben cumplir con un contraste adecuado y navegación clara para facilitar su uso.
---

## V. Actores del Módulo

| Actor | Tipo | Descripción y Funciones en el Módulo |
| :--- | :--- | :--- |
| **Alumno** | Primario | Usuario principal del módulo. Inicia sesión, actualiza sus datos de contacto, cambia su contraseña, consulta calificaciones, historial, horarios y materias inscritas, revisa el estado de su reinscripción y descarga constancias en PDF. |
| **Motor de Documentos PDF** | Secundario (Sistema) | Componente automatizado encargado de validar la vigencia del estudiante y compilar la constancia oficial con sello y folio digital. |
| **Base de Datos Institucional** | Secundario (Sistema) | Repositorio central que provee los registros académicos, cargas horarias y estatus administrativos en modo de lectura/escritura controlada. |
---

## VI. Modelado del Sistema (Diagramas UML)

### 6.1. Diagrama de Contexto del Módulo

![Diagrama de Contexto](resources/imgs/Diagra_de_Contexto_Alumno.png)
```plantuml

@startuml
!theme plain
skinparam rectangleStyle uml2
actor "Alumno" as Alumno
rectangle "Módulo de Alumnos (SIGE)" as ModAlumnos
database "Base de Datos Académica" as DB
cloud "Servicio Generador de PDF" as PDF
cloud "Servicio de Autenticación (JWT)" as Auth
Alumno --> ModAlumnos : Consulta notas, horario,\nactualiza perfil, descarga constancia
ModAlumnos <--> Auth : Valida credenciales y sesión
ModAlumnos <--> DB : Consulta carga académica,\nhistorial y actualiza contacto
ModAlumnos <--> PDF : Solicita y recibe\nconstancia oficial en PDF
@enduml
```

### 6.2. Diagrama de Casos de Uso

![Diagrama de Casos de Uso](resources/imgs/Caso_de_usos_Alumno.png)
```plantuml

@startuml
left to right direction
actor "Alumno" as A
rectangle "Módulo de Alumnos" {
    usecase "Iniciar sesión" as UC1
    usecase "Editar datos generales" as UC2
    usecase "Iniciar reinscripción" as UC3
    usecase "Consultar datos personales" as UC4
    usecase "Consultar calificaciones" as UC5
    usecase "Consultar historial académico" as UC6
    usecase "Consultar horario" as UC7
    usecase "Consultar materias inscritas" as UC8
    usecase "Descargar constancia de estudios" as UC9
    usecase "Cambiar contraseña" as UC10
    usecase "Consultar estado de reinscripción" as UC11

}

A --> UC1
A --> UC2
A --> UC3
A --> UC4
A --> UC5
A --> UC6
A --> UC7
A --> UC8
A --> UC9
A --> UC10
A --> UC11
UC02 ..> UC01 : <<include>>
UC03 ..> UC01 : <<include>>
UC04 ..> UC01 : <<include>>
UC07 ..> UC01 : <<include>>
UC08 ..> UC01 : <<include>>
UC09 ..> UC01 : <<include>>
UC10 ..> UC01 : <<include>>
UC11 ..> UC01 : <<include>>
@enduml

```

### 6.3. Diagrama de Clases

![Diagrama de Clases](resources/imgs/Diagrama_de_Clases_Alumno.png)
```plantuml
@startuml
skinparam classAttributeIconSize 0
class Alumno {
  - matricula: String
  - nombre: String
  - apellidos: String
  - correoInstitucional: String
  - correoAlterno: String
  - telefono: String
  - domicilio: String
  - semestreActual: int
  - promedioGeneral: float
  - estatusAcademico: String
  - passwordHash: String
  + iniciarSesion(matricula: String, pass: String): Boolean
  + actualizarDatosContacto(tel: String, correo: String, dir: String): Boolean
  + cambiarPassword(actual: String, nueva: String): Boolean

}

class CargaAcademica {
  - idCarga: int
  - cicloEscolar: String
  - totalCreditos: int
  + obtenerMateriasInscritas(): List<InscripcionMateria>
}

class InscripcionMateria {
  - idInscripcion: int
  - claveMateria: String
  - nombreMateria: String
  - grupo: String
  - docente: String
  - calificacionParcial1: float
  - calificacionParcial2: float
  - calificacionFinal: float
  - acreditada: Boolean
}

class HorarioClase {
  - idHorario: int
  - diaSemana: String
  - horaInicio: Time
  - horaFin: Time
  - aula: String
}

class HistorialAcademico {
  - idHistorial: int
  - creditosAprobados: int
  - creditosTotalesPlan: int
  - porcentajeAvance: float
  + consultarKardex(): List<InscripcionMateria>
}

class ConstanciaEstudios {
  - folioUnico: String
  - fechaEmision: DateTime
  - cadenaDigital: String
  + generarPDF(alumno: Alumno): File
}

class TramiteReinscripcion {
  - idTramite: int
  - cicloDestino: String
  - fechaSolicitud: Date
  - estatus: EstadoReinscripcion
  - observaciones: String
  + consultarEstado(): EstadoReinscripcion

}

enum EstadoReinscripcion {
  EN_PROCESO
  APROBADO
  RECHAZADO
  CON_OBSERVACIONES
}

Alumno "1" --> "1" HistorialAcademico : posee
Alumno "1" --> "*" CargaAcademica : tiene
CargaAcademica "1" *-- "*" InscripcionMateria : contiene
InscripcionMateria "1" *-- "*" HorarioClase : se imparte en
Alumno "1" --> "*" ConstanciaEstudios : genera
Alumno "1" --> "*" TramiteReinscripcion : consulta
TramiteReinscripcion --> EstadoReinscripcion
@enduml
```
### 6.4. Diagrama de Componentes
![Diagrama de Componentes](resources/imgs/Diagrama_de_Componentes_Alumno.png)

```plantuml
@startuml
package "Frontend - Portal Web Alumnos" {
  [Vista Login y Perfil]
  [Vista Consultas Académicas]
  [Vista Trámites y Constancias]
  [Cliente HTTP / Gestor de Sesión]
}

package "Backend - Microservicio / Módulo Alumnos" {
  [Controlador REST Alumnos]
  [Servicio de Perfil y Seguridad]
  [Servicio de Consulta Académica]
  [Servicio de Constancias PDF]
  [Servicio de Seguimiento Reinscripción]
}

database "Infraestructura y Datos" {
  [Base de Datos Relacional]
  [Librería Generadora PDF (iText/Puppeteer)]
}

[Vista Login y Perfil] --> [Cliente HTTP / Gestor de Sesión]
[Vista Consultas Académicas] --> [Cliente HTTP / Gestor de Sesión]
[Vista Trámites y Constancias] --> [Cliente HTTP / Gestor de Sesión]
[Cliente HTTP / Gestor de Sesión] --> [Controlador REST Alumnos] : HTTPS / JSON (JWT)
[Controlador REST Alumnos] --> [Servicio de Perfil y Seguridad]
[Controlador REST Alumnos] --> [Servicio de Consulta Académica]
[Controlador REST Alumnos] --> [Servicio de Constancias PDF]
[Controlador REST Alumnos] --> [Servicio de Seguimiento Reinscripción]
[Servicio de Perfil y Seguridad] --> [Base de Datos Relacional]
[Servicio de Consulta Académica] --> [Base de Datos Relacional]
[Servicio de Seguimiento Reinscripción] --> [Base de Datos Relacional]
[Servicio de Constancias PDF] --> [Base de Datos Relacional]
[Servicio de Constancias PDF] --> [Librería Generadora PDF (iText/Puppeteer)]
@enduml

```
### 6.5. Diagramas de Secuencia

![Diagrama de Secuencias A](resources/imgs/Diagrama_de_SecuenciasA_Alumno.png)
#### A. Secuencia: Descargar Constancia de Estudios (UC09)
```plantuml
@startuml
actor Alumno
participant "UI Portal Alumno" as UI
participant "Controlador Alumnos" as Ctrl
participant "Servicio Constancias" as Svc
participant "Base de Datos" as DB
participant "Motor PDF" as PDF
Alumno -> UI : Selecciona "Descargar Constancia de Estudios"
UI -> Ctrl : GET /api/v1/alumnos/{matricula}/constancia (Token JWT)
Ctrl -> Svc : solicitarConstancia(matricula)
Svc -> DB : obtenerDatosYEstadoAlumno(matricula)
DB --> Svc : DatosAlumno (estatus = "ACTIVO")
alt Alumno con estatus ACTIVO
  Svc -> PDF : compilarPlantillaPDF(DatosAlumno, folio, selloDigital)
  PDF --> Svc : byte[] archivoPDF
  Svc --> Ctrl : archivoPDF
  Ctrl --> UI : 200 OK (Content-Type: application/pdf)
  UI --> Alumno : Inicia descarga automática del PDF
else Alumno INACTIVO o con restricción administrativa
  Svc --> Ctrl : ErrorValidacion("Alumno no elegible para constancia")
  Ctrl --> UI : 403 Forbidden
  UI --> Alumno : Muestra notificación con motivo de restricción
end
@enduml

```
![Diagrama de Secuencias B](resources/imgs/Diagrama_de_SecuenciasB_Alumno.png)
#### B. Secuencia: Cambiar Contraseña (UC10)

```plantuml
@startuml
actor Alumno
participant "UI Perfil Alumno" as UI
participant "Controlador Alumnos" as Ctrl
participant "Servicio Seguridad" as Sec
participant "Base de Datos" as DB
Alumno -> UI : Ingresa contraseña actual y nueva contraseña
UI -> Ctrl : PUT /api/v1/alumnos/{matricula}/password
Ctrl -> Sec : cambiarPassword(matricula, passActual, passNueva)
Sec -> DB : obtenerHashActual(matricula)
DB --> Sec : hashAlmacenado
Sec -> Sec : verificarHash(passActual, hashAlmacenado)
alt Contraseña actual válida y nueva cumple políticas
  Sec -> Sec : generarNuevoHash(passNueva)
  Sec -> DB : actualizarPasswordHash(matricula, nuevoHash)
  DB --> Sec : Confirmación actualización
  Sec --> Ctrl : Operación exitosa
  Ctrl --> UI : 200 OK
  UI --> Alumno : Muestra mensaje "Contraseña actualizada"
else Contraseña actual incorrecta
  Sec --> Ctrl : ErrorAutenticacion("Contraseña actual incorrecta")
  Ctrl --> UI : 401 Unauthorized
  UI --> Alumno : Muestra alerta de error
end

@enduml

```
![Diagrama de Secuencias C](resources/imgs/Diagrama_de_SecuenciasC_Alumno.png)
#### C. Diagrama de Secuencia C
```plantuml
@startuml
actor Alumno
participant "UI Académica" as UI
participant "Controlador Académico" as Ctrl
participant "Base de Datos" as DB
Alumno -> UI : Selecciona opción (Calificaciones / Historial / Horario / Materias)
UI -> Ctrl : GET /api/alumnos/{consulta} (UC5, UC6, UC7 o UC8)
Ctrl -> DB : Consultar registros académicos del alumno
DB --> Ctrl : Lista de resultados
Ctrl --> UI : 200 OK (Datos solicitados)
UI --> Alumno : Renderiza información correspondiente
@enduml
```
![Diagrama de Secuencias D](resources/imgs/Diagrama_de_SecuenciasD_Alumno.png)
#### D. Diagrama de Secuencia D
```plantuml
@startuml
actor Alumno
participant "UI Constancias" as UI
participant "Controlador Constancias" as Ctrl
participant "Base de Datos" as DB
participant "Generador PDF" as PDF

Alumno -> UI : Clic en "Descargar constancia de estudios"
UI -> Ctrl : GET /api/alumnos/constancia
Ctrl -> DB : Verificar estatus vigente del alumno
alt Alumno activo
  DB --> Ctrl : Estatus activo
  Ctrl -> PDF : Generar PDF con folio y datos
  PDF --> Ctrl : Archivo PDF
  Ctrl --> UI : 200 OK (application/pdf)
  UI --> Alumno : Descarga constancia en PDF
else Alumno no vigente / bloqueado
  DB --> Ctrl : Restricción activa
  Ctrl --> UI : 403 Forbidden
  UI --> Alumno : Muestra motivo de restricción
end
@enduml
```
![Diagrama de Secuencias E](resources/imgs/Diagrama_de_SecuenciasE_Alumno.png)
#### E. Diagrama de Secuencia E
```plantuml
@startuml
actor Alumno
participant "UI Reinscripción" as UI
participant "Controlador Reinscripción" as Ctrl
participant "Base de Datos" as DB

== UC3: Iniciar reinscripción ==
Alumno -> UI : Clic en "Iniciar reinscripción"
UI -> Ctrl : POST /api/alumnos/reinscripcion
Ctrl -> DB : Validar elegibilidad y crear trámite ("En proceso")
DB --> Ctrl : Trámite creado
Ctrl --> UI : 201 Created
UI --> Alumno : Muestra confirmación de inicio

== UC11: Consultar estado de reinscripción ==
Alumno -> UI : Clic en "Consultar estado de reinscripción"
UI -> Ctrl : GET /api/alumnos/reinscripcion/estado
Ctrl -> DB : Obtener trámite actual
DB --> Ctrl : Estado (En proceso / Aprobado / Rechazado / Con observaciones)
Ctrl --> UI : 200 OK
UI --> Alumno : Muestra estado y observaciones
@enduml
```
### 6.6. Diagrama de Estados (Trámite de Reinscripción - UC11)

![Diagrama de Estados](resources/imgs/Diagrama_de_estados_Alumno.png)

```plantuml

@startuml
[*] --> SinSolicitud
SinSolicitud --> EnProceso : Alumno registra solicitud\nde reinscripción
EnProceso --> ConObservaciones : Servicios escolares detecta\ndocumentación o requisito pendiente
ConObservaciones --> EnProceso : Alumno subsana\nobservaciones
EnProceso --> Aprobado : Validación administrativa\nsatisfactoria
EnProceso --> Rechazado : Incumplimiento de reglamento\no vencimiento de plazo
Aprobado --> [*] : Carga académica activada
Rechazado --> [*] : Trámite cerrado

@enduml

```
## VII. Interfaz de Usuario (Wireframes / Mockups)

El diseño visual del Módulo de Alumnos sigue principios de usabilidad centrados en el estudiante, priorizando la claridad, consistencia y accesibilidad. A continuación se presentan los wireframes de las principales pantallas del módulo:
1. **Pantalla de Inicio de Sesión:** Formulario minimalista con validación en tiempo real de matrícula institucional, campo de contraseña con opción de visibilidad y enlace de recuperación.
2. **Dashboard Principal del Alumno:**
   * **Barra lateral / Menú superior:** Acceso directo a *Inicio, Mi Perfil, Horario, Calificaciones, Historial Académico, Reinscripción* y *Constancias*.
   * **Tarjetas resumen (KPIs):** Promedio general acumulado, créditos aprobados vs. totales, semestre actual y estatus de reinscripción vigente.
3. **Vista de Horario Semanal:** Tabla matricial estructurada por días de la semana (Lunes a Sábado) y bloques horarios, diferenciando cada materia por color e indicando clave, grupo, aula y docente.
4. **Vista de Boleta e Historial:** Tabla filtrable por periodo escolar con desglose de evaluaciones parciales, calificación final y estado (*Acreditada / No acreditada*).
5. **Sección de Trámites y Descargas:** Indicador visual de progreso (*Stepper*) para el estado de reinscripción (`En proceso` → `Aprobado`) y botón de descarga directa en un clic para la constancia oficial en PDF.

## VIII. Autenticación, Autorización y Permisos del Módulo

El acceso al Módulo de Alumnos está protegido mediante autenticación basada en **JSON Web Tokens (JWT)** con expiración automática tras 15 minutos de inactividad (`RNF-03`).

### Matriz de Permisos del Módulo de Alumnos

| Funcionalidad / Recurso | Alumno (Propietario) | Otros Roles (Profesor / Coord. / Admin) |
| :--- | :---: | :---: |
| **Iniciar sesión y gestionar sesión propia** | Permitido | N/A (Usan sus respectivos módulos) |
| **Ver y editar datos de contacto propios** | Lectura / Escritura | Sin acceso directo en este módulo |
| **Cambiar contraseña propia** | Ejecución | Sin acceso |
| **Consultar calificaciones e historial** | Solo Lectura (Propios) | Sin acceso en esta vista |
| **Consultar horario y materias inscritas** | Solo Lectura (Propios) | Sin acceso en esta vista |
| **Consultar estado de reinscripción** | Solo Lectura (Propio) | Sin acceso en esta vista |
| **Descargar constancia de estudios (PDF)** | Ejecución (Propia) | Sin acceso en esta vista |

## IX. Glosario, Abreviaturas y Nomenclaturas

### Abreviaturas

* **API:** *Application Programming Interface* (Interfaz de Programación de Aplicaciones).
* **HTTPS:** *Hypertext Transfer Protocol Secure* (Protocolo Seguro de Transferencia de Hipertexto).
* **JSON:** *JavaScript Object Notation* (Notación de Objetos de JavaScript).
* **JWT:** *JSON Web Token* (Token Web JSON para autenticación).
* **KPI:** *Key Performance Indicator* (Indicador Clave de Rendimiento).
* **PDF:** *Portable Document Format* (Formato de Documento Portable).
* **RF:** Requerimiento Funcional.
* **RNF:** Requerimiento No Funcional.
* **SIGE:** Sistema Integral de Gestión Escolar.
* **UC:** *Use Case* (Caso de Uso).
* **UI:** *User Interface* (Interfaz de Usuario).
* **UML:** *Unified Modeling Language* (Lenguaje Unificado de Modelado).
* **UX:** *User Experience* (Experiencia de Usuario).

### Nomenclaturas

* **Requerimientos Funcionales:** `RF-XX` (ej. `RF-09` para Descargar constancia de estudios).
* **Requerimientos No Funcionales:** `RNF-XX` (ej. `RNF-03` para Sesiones expiradas).
* **Casos de Uso:** `UC-XX` (ej. `UC09` para Descargar constancia de estudios).
* **Rutas de Recursos Gráficos:** `resources/imgs/m1_[nombre_diagrama].png`.


## X. Referencias Bibliográficas
* Booch, G., Rumbaugh, J., & Jacobson, I. (2006). *El Lenguaje Unificado de Modelado: Guía del Usuario* (2.ª ed.). Addison-Wesley.
* Pressman, R. S., & Maxim, B. R. (2021). *Ingeniería del Software: Un enfoque práctico* (9.ª ed.). McGraw-Hill Education.
* Sommerville, I. (2011). *Ingeniería de Software* (9.ª ed.). Pearson Educación.
* Object Management Group (OMG). (2017). *OMG Unified Modeling Language (OMG UML), Version 2.5.1*. https://www.omg.org/spec/UML/
* PlantUML Documentation. (2025). *PlantUML Language Reference Guide*. https://plantuml.com/
