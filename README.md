# PROYECTO-ELECTIVA-1

# 🚗 ParKol — Sistema de Gestión de Parqueadero

**ParKol** es una aplicación web para la gestión y administración de un **parqueadero público con capacidad de 50 vehículos**.

El sistema permite controlar las entradas y salidas de vehículos, administrar los cupos disponibles, realizar reservas, calcular automáticamente el valor a pagar según el tiempo de permanencia, registrar pagos y consultar el historial de vehículos.

El proyecto busca facilitar la administración del parqueadero, reducir el manejo manual de la información y ofrecer una forma más organizada de controlar los espacios disponibles.

---

## 🎯 Objetivo del proyecto

Desarrollar un sistema que permita **automatizar la gestión de un parqueadero público**, facilitando el registro de vehículos, el control de cupos, las reservas y el cálculo de los pagos.

---

## 🚘 Funcionalidades principales

* 🚗 Registro de entrada de vehículos.
* 🔤 Registro de placa.
* 🚙 Selección del tipo de vehículo:

  * 🚗 Carro
  * 🏍️ Moto
* 🅿️ Visualización de cupos disponibles.
* 📅 Reserva de cupos.
* 🚪 Registro de salida.
* ⏱️ Cálculo automático del tiempo de permanencia.
* 💰 Cálculo automático del valor a pagar.
* 💳 Registro de pagos.
* 📋 Historial de vehículos.
* 👨‍💼 Panel de administrador.
* ⚙️ Administración de tarifas.

---

## 🅿️ Capacidad del parqueadero

ParKol tendrá una capacidad inicial de **50 cupos**.

Para evitar mostrar 50 botones individualmente, los espacios podrán organizarse por **zonas**, facilitando la visualización y administración del parqueadero.

```text
              PARKOL
        Estado del parqueadero

┌─────────────────────────────────┐
│ ZONA A — CARROS                 │
│ 🟢 🟢 🔴 🟢 🟢 🟢 🟢 🟢 🟢 🟢   │
│ 01 02 03 04 05 06 07 08 09 10  │
└─────────────────────────────────┘

┌─────────────────────────────────┐
│ ZONA B — CARROS                 │
│ 🟢 🔴 🟢 🟢 🟢 🟢 🟢 🟢 🟢 🟢   │
│ 11 12 13 14 15 16 17 18 19 20  │
└─────────────────────────────────┘

┌─────────────────────────────────┐
│ ZONA C — MOTOS                  │
│ 🟢 🟢 🟢 🔴 🟢 🟢 🟢 🟢 🟢 🟢   │
│ 21 22 23 24 25 26 27 28 29 30  │
└─────────────────────────────────┘

🟢 Disponible
🔴 Ocupado
🟡 Reservado
```

---

## 🚪 Registro de salida

Cuando un vehículo salga del parqueadero, ParKol calculará automáticamente el tiempo de permanencia y el valor correspondiente.

**Ejemplo:**

```text
Placa: ABC123
Entrada: 2:15 PM
Salida: 5:40 PM
Tiempo: 3 h 25 min
Total: $12.000

[ REGISTRAR PAGO ]
```

Una vez registrado el pago, el cupo volverá a estar disponible automáticamente.

---

## 💰 Cálculo de tarifas

El valor a pagar será calculado automáticamente teniendo en cuenta:

* Tipo de vehículo.
* Tiempo de permanencia.
* Tarifa configurada.

Las tarifas podrán ser modificadas desde el **panel de administrador**.

---

## 📋 Historial de vehículos

ParKol almacenará los registros de los vehículos que hayan utilizado el parqueadero.

| Placa  | Tipo     | Entrada | Salida   | Tiempo   |   Total | Estado |
| ------ | -------- | ------- | -------- | -------- | ------: | ------ |
| ABC123 | 🚗 Carro | 2:15 PM | 5:40 PM  | 3h 25min | $12.000 | Pagado |
| XYZ789 | 🏍️ Moto | 8:10 AM | 10:30 AM | 2h 20min |  $6.000 | Pagado |

---

## 👨‍💼 Panel de administrador

El administrador podrá:

* Consultar el estado de los 50 cupos.
* Registrar entradas y salidas.
* Administrar reservas.
* Registrar pagos.
* Consultar el historial.
* Configurar tarifas.
* Consultar estadísticas del parqueadero.
* Gestionar la información de los vehículos.

---

## 🔄 Flujo principal

```text
              INICIO
                 │
                 ▼
       Registrar vehículo
                 │
                 ▼
        Ingresar placa
                 │
                 ▼
    Seleccionar carro o moto
                 │
                 ▼
      Verificar disponibilidad
                 │
          ┌──────┴──────┐
          │             │
     Disponible      Sin cupos
          │             │
          ▼             ▼
    Asignar cupo     Mostrar aviso
          │
          ▼
   Registrar entrada
          │
          ▼
   Vehículo permanece
          │
          ▼
    Registrar salida
          │
          ▼
 Calcular tiempo y tarifa
          │
          ▼
    Registrar pago
          │
          ▼
    Liberar cupo
          │
          ▼
          FIN
```

---

## 🛠️ Tecnologías

La implementación de ParKol podrá utilizar:

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend

* Node.js
* Express.js

### Base de datos

* MySQL

### Control de versiones

* Git
* GitHub

---

## 📁 Estructura del proyecto

```text
ParKol/
│
├── frontend/
│   ├── index.html
│   ├── css/
│   │   └── styles.css
│   └── js/
│       └── app.js
│
├── backend/
│   ├── server.js
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   └── config/
│
├── database/
│   └── parkol.sql
│
├── README.md
└── package.json
```

---

## 📌 Estado del proyecto

🚧 **En desarrollo**

ParKol es un proyecto de desarrollo académico que irá incorporando nuevas funcionalidades a medida que avance su construcción.

---

## 📄 Licencia

Este proyecto ha sido desarrollado con fines **académicos y educativos**.

---

## 👨‍💻 Autor

**Tu nombre aquí**

Proyecto académico — **ParKol**

---

⭐ **ParKol — Una forma sencilla de administrar tu parqueadero.**
