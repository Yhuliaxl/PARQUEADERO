# 🚗 Sistema de Gestión Integral de Parqueadero

> 🅿️ Sistema web para la **gestión integral de un parqueadero**, diseñado para centralizar las operaciones, servicios, clientes, vehículos, pagos, mensualidades, pertenencias, gastos y reportes administrativos.

---

## 📌 Descripción del proyecto

El proyecto consiste en desarrollar un sistema web para la gestión integral de un parqueadero, orientado a centralizar y facilitar el control de las operaciones realizadas diariamente en el establecimiento. La aplicación permitirá administrar la información relacionada con vehículos, clientes, servicios, pagos, mensualidades, pertenencias almacenadas y movimientos económicos del negocio.

El sistema será desarrollado utilizando **Python con Django** para el backend, encargado de la lógica de negocio, procesamiento de información, autenticación y comunicación con la base de datos. Para el frontend se utilizará **HeroUI**, con el objetivo de proporcionar una interfaz moderna, organizada y sencilla de utilizar para el personal encargado de la operación y administración del parqueadero.

La aplicación permitirá gestionar tanto los servicios convencionales de parqueadero como los servicios mediante mensualidad. Además, contará con un sistema configurable de tarifas que permitirá al propietario establecer la forma en que se cobra el tiempo de permanencia, adaptándose a las necesidades específicas del establecimiento.

El sistema también tendrá un componente administrativo que permitirá al propietario consultar el comportamiento económico y operativo del parqueadero mediante reportes y gráficos. Estos podrán mostrar información de la actividad diaria y realizar una trazabilidad de los resultados obtenidos, incluyendo los ingresos generados y los gastos registrados durante cada jornada.

Como complemento, el sistema podrá incorporar servicios adicionales según las necesidades del establecimiento, como el almacenamiento temporal de cascos, maletas, tulas u otras pertenencias de los clientes. Estos elementos podrán ser registrados y asociados al servicio correspondiente para mantener un control sobre los objetos almacenados.

El propósito del proyecto es proporcionar una herramienta centralizada que permita mejorar la organización, control y seguimiento de las operaciones del parqueadero, reduciendo procesos manuales y facilitando al propietario la consulta de información operativa y financiera para la administración del negocio.

---

# ⚙️ Requerimientos funcionales

## 👥 RF01 — Gestión de clientes

El sistema debe permitir registrar, consultar, modificar y administrar la información básica de los clientes que utilizan los servicios del parqueadero.

---

## 🚗 RF02 — Gestión de vehículos

El sistema debe permitir registrar los vehículos asociados a los clientes, incluyendo su placa y tipo de vehículo.

Debe ser posible consultar el historial relacionado con cada vehículo.

---

## 🟢 RF03 — Registro de ingreso

El sistema debe permitir registrar el ingreso de un vehículo y generar la información necesaria para identificar el servicio.

El registro deberá almacenar la fecha y hora de ingreso.

---

## 📅 RF04 — Control de mensualidades

El sistema debe identificar automáticamente si un vehículo cuenta con una mensualidad vigente.

Cuando la mensualidad esté activa, el sistema deberá informar al empleado que el vehículo tiene una mensualidad vigente y no deberá permitir registrar un nuevo servicio de parqueadero convencional.

---

## ⏰ RF05 — Vencimiento de mensualidad

Cuando finalice el período de una mensualidad, el sistema deberá cambiar su estado a vencida y notificar al usuario encargado.

El sistema deberá mostrar el período correspondiente de la mensualidad.

---

## 🔄 RF06 — Renovación de mensualidad

El sistema debe permitir registrar la renovación de una mensualidad, generando un nuevo período de vigencia y conservando el historial de los períodos anteriores.

---

## ⚠️ RF07 — Control de mensualidades pendientes

Después del vencimiento, el sistema deberá realizar seguimiento a las mensualidades que todavía no hayan sido renovadas.

El sistema deberá permitir controlar el período establecido para que el cliente pueda realizar la renovación.

---

## 🗑️ RF08 — Eliminación automática de mensualidad

Si una mensualidad permanece sin renovación durante **10 días después de su vencimiento**, el sistema deberá cambiarla automáticamente a un estado inactivo o eliminado.

El sistema deberá generar una notificación informando al usuario encargado.

---

## 🎫 RF09 — Generación de ticket

El sistema debe permitir generar un ticket para los servicios de parqueadero.

El ticket deberá contener la información necesaria para identificar el vehículo, el servicio y la fecha y hora correspondiente.

---

## 🖨️ RF10 — Impresión de ticket

El sistema debe permitir imprimir el ticket generado.

En el caso de una mensualidad vencida, deberá permitir al empleado decidir si desea continuar con la generación e impresión del ticket o cancelar la operación.

---

## 🚪 RF11 — Registro de salida

El sistema debe permitir registrar la salida de un vehículo utilizando el identificador correspondiente del servicio.

Debe registrar la fecha y hora de salida.

---

## 💰 RF12 — Cálculo automático del servicio

El sistema deberá calcular automáticamente el valor a pagar teniendo en cuenta el tiempo de permanencia y las tarifas configuradas.

---

## 💵 RF13 — Configuración de tarifas

El administrador podrá configurar las tarifas del parqueadero de acuerdo con las necesidades del establecimiento.

El sistema deberá permitir definir diferentes reglas de cobro, por ejemplo:

* ⏱️ Cobro por hora.
* 🕐 Cobro por fracción.
* 🕧 Cobro por media hora.
* ⏳ Cobro después de determinados minutos.

---

## ⏱️ RF14 — Configuración de fracciones de tiempo

El propietario podrá establecer desde qué cantidad de minutos se debe cobrar una determinada fracción.

Por ejemplo, podrá configurar que:

* **Hasta 10 minutos** → determinada tarifa.
* **Después de 10 minutos** → media hora.
* **Después de 15 minutos** → hora completa.

Los valores y condiciones deberán ser configurables y no estar establecidos de manera fija en el sistema.

---

## 🏷️ RF15 — Tarifas diferenciadas

El sistema deberá permitir configurar diferentes tarifas dependiendo del tipo de vehículo o servicio.

Por ejemplo:

* 🏍️ Moto.
* 🚗 Automóvil.
* 🚙 Otros tipos definidos por el administrador.

---

## 💳 RF16 — Registro de pagos

El sistema deberá permitir registrar los pagos realizados por los clientes y asociarlos con el servicio correspondiente.

---

## 💵 RF17 — Métodos de pago

El sistema podrá registrar el método mediante el cual se realizó el pago, según las opciones configuradas por el administrador.

---

## 🪖 RF18 — Gestión de cascos

El sistema deberá permitir registrar el almacenamiento de cascos cuando el parqueadero ofrezca este servicio.

Se deberá poder asociar el casco con el cliente, vehículo o servicio correspondiente para facilitar su identificación y entrega.

---

## 🧳 RF19 — Control de pertenencias

El sistema deberá permitir registrar otros objetos entregados para almacenamiento, como:

* 🧳 Maletas.
* 🎒 Tulas.
* 👜 Bolsos.
* 📦 Otros objetos definidos por el establecimiento.

Cada elemento deberá quedar asociado al servicio o cliente correspondiente.

---

## 🏪 RF20 — Gestión de almacén

El sistema podrá contar con un módulo de almacenamiento para controlar los objetos que se encuentren temporalmente bajo custodia del parqueadero.

El administrador podrá activar o desactivar este servicio según las necesidades del establecimiento.

---

## 📦 RF21 — Entrega de pertenencias

El sistema deberá permitir registrar la entrega de los objetos almacenados y actualizar su estado para evitar que aparezcan como pendientes.

---

## 💸 RF22 — Registro de gastos

El administrador, como propietario del establecimiento, deberá contar con un apartado para registrar los gastos realizados durante el día.

Cada gasto podrá incluir:

* 📝 Concepto.
* 💰 Valor.
* 📅 Fecha.
* 📌 Observación, si es necesaria.

---

## 📈 RF23 — Control de ingresos diarios

El sistema deberá calcular el total de ingresos generados durante una jornada.

---

## 💸 RF24 — Control de gastos diarios

El sistema deberá calcular el total de gastos registrados durante una jornada.

---

## 📊 RF25 — Resultado diario

El sistema deberá permitir visualizar el resultado económico del día diferenciando:

### 💰 Total de ingresos sin gastos

**y**

### 💵 Total de ingresos después de gastos.

Por ejemplo:

> 💰 **Ingresos:** $500.000
> 💸 **Gastos:** $80.000
> 📊 **Resultado:** $420.000

---

## 📄 RF26 — Reporte diario

El administrador podrá generar un reporte correspondiente a una fecha determinada.

El reporte deberá incluir información como:

* 🚗 Total de servicios.
* 💰 Total de ingresos.
* 💸 Total de gastos.
* 📊 Resultado después de gastos.
* 💳 Pagos.
* 📅 Mensualidades.
* 📋 Información relevante de la operación.

---

## 🕒 RF27 — Trazabilidad diaria

El sistema deberá conservar información histórica de las jornadas anteriores para permitir realizar una trazabilidad de la actividad del parqueadero.

El administrador podrá consultar cómo fueron los resultados de días anteriores y comparar la información registrada.

---

## 📊 RF28 — Gráficas administrativas

El sistema deberá presentar gráficamente información relevante del funcionamiento del parqueadero.

Las gráficas podrán representar:

* 📈 Ingresos por día.
* 📉 Gastos por día.
* 💰 Resultado diario.
* 🚗 Cantidad de vehículos atendidos.
* 📅 Comportamiento de las mensualidades.
* 📊 Otros indicadores definidos para la administración.

---

## 🗂️ RF29 — Consulta histórica

El administrador podrá consultar información de períodos anteriores, permitiendo analizar el comportamiento económico y operativo del establecimiento.

---

## 👤 RF30 — Gestión de usuarios

El sistema deberá permitir administrar los usuarios que tendrán acceso a la plataforma.

Se podrán establecer diferentes roles, principalmente:

* 👑 **Administrador/Propietario**
* 👨‍💼 **Empleado**

---

## 🔐 RF31 — Control de permisos

El sistema deberá controlar qué funciones puede utilizar cada tipo de usuario.

El administrador tendrá acceso a las funciones administrativas y económicas, mientras que el empleado tendrá acceso únicamente a las operaciones necesarias para prestar el servicio.

---

## 🔑 RF32 — Inicio de sesión

Los usuarios deberán autenticarse mediante credenciales para acceder al sistema.

---

## 🔔 RF33 — Notificaciones

El sistema deberá generar notificaciones sobre eventos importantes, como:

* ⚠️ Mensualidades vencidas.
* ⏰ Mensualidades próximas a eliminarse.
* 🗑️ Mensualidades eliminadas.
* 📋 Servicios pendientes.
* 🔔 Otros eventos configurados por el administrador.

---

# 🛠️ Requerimientos no funcionales

## 🐍 RNF01 — Tecnología

El backend deberá desarrollarse utilizando **Python y Django**.

---

## 🎨 RNF02 — Interfaz

El frontend deberá desarrollarse utilizando **HeroUI**, proporcionando una interfaz moderna, clara y adaptable.

---

## 🔐 RNF03 — Seguridad

El sistema deberá proteger la información mediante autenticación y control de permisos según el rol del usuario.

---

## 🗄️ RNF04 — Integridad de datos

El sistema deberá garantizar que la información registrada sea consistente y evitar registros duplicados o inconsistentes.

---

## 🖥️ RNF05 — Usabilidad

La aplicación deberá ser sencilla de utilizar para empleados y administradores, reduciendo la cantidad de pasos necesarios para realizar las operaciones frecuentes.

---

## ⚡ RNF06 — Rendimiento

Las operaciones habituales, como registrar un ingreso, consultar una placa o generar un ticket, deberán ejecutarse en un tiempo adecuado para no afectar la atención de los clientes.

---

## 🟢 RNF07 — Disponibilidad

El sistema deberá estar disponible durante el horario de funcionamiento del parqueadero.

---

## 📈 RNF08 — Escalabilidad

La estructura del sistema deberá permitir agregar posteriormente nuevos tipos de servicios, tarifas, vehículos, usuarios o funcionalidades sin tener que reconstruir completamente la aplicación.

---

## 💾 RNF09 — Respaldo

La información almacenada deberá contar con mecanismos de respaldo para evitar la pérdida de información histórica.

---

## 🕵️ RNF10 — Trazabilidad

Las operaciones importantes deberán conservar información suficiente para identificar cuándo se realizaron y qué usuario las realizó.

---

# 🧩 Módulos principales del sistema

Con todos los requerimientos que hemos definido, el proyecto podría quedar dividido en estos módulos:

| #      | Módulo                         |
| ------ | ------------------------------ |
| 1️⃣    | 📊 **Dashboard**               |
| 2️⃣    | 🚗 **Ingresos y salidas**      |
| 3️⃣    | 🎫 **Tickets**                 |
| 4️⃣    | 👥 **Clientes**                |
| 5️⃣    | 🚘 **Vehículos**               |
| 6️⃣    | 📅 **Mensualidades**           |
| 7️⃣    | 💳 **Pagos**                   |
| 8️⃣    | 💰 **Tarifas**                 |
| 9️⃣    | 🧳 **Almacén / pertenencias**  |
| 🔟     | 💸 **Gastos**                  |
| 1️⃣1️⃣ | 📄 **Reportes**                |
| 1️⃣2️⃣ | 📊 **Gráficas y estadísticas** |
| 1️⃣3️⃣ | 👤 **Usuarios y permisos**     |
| 1️⃣4️⃣ | ⚙️ **Configuración**           |

---

# 🏁 Conclusión

Así el proyecto queda planteado como un **sistema completo de administración de parqueadero**, no simplemente como un programa para registrar entradas y salidas.

El sistema contempla la gestión operativa, financiera y administrativa del establecimiento, incluyendo:

* 🚗 Control de vehículos.
* 👥 Gestión de clientes.
* 🎫 Tickets.
* 📅 Mensualidades.
* 💳 Pagos.
* 💰 Tarifas configurables.
* 🧳 Almacenamiento de pertenencias.
* 💸 Control de gastos.
* 📊 Ingresos y resultados diarios.
* 📄 Reportes.
* 📈 Gráficas y estadísticas.
* 👤 Usuarios y permisos.
* 🔔 Notificaciones.
* 🕒 Trazabilidad histórica.

---

## 🚀 Tecnologías

* 🐍 **Python**
* 🌐 **Django**
* 🎨 **HeroUI**
* 🗄️ **Base de datos**
* 🔐 **Sistema de autenticación y permisos**

---

> 💡 **Objetivo:** proporcionar una herramienta centralizada que permita mejorar la organización, control y seguimiento de las operaciones del parqueadero, reduciendo procesos manuales y facilitando la administración del negocio.
