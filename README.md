# api-rest-CV
# 🔐 API REST - Autenticación JWT, Roles y Permisos

![Node.js](https://img.shields.io/badge/Node.js-Backend-green)
![Express](https://img.shields.io/badge/Express.js-Framework-black)
![JWT](https://img.shields.io/badge/JWT-Authentication-blue)
![bcrypt](https://img.shields.io/badge/bcrypt-Security-orange)
![Swagger](https://img.shields.io/badge/Swagger-Documentation-brightgreen)
![Postman](https://img.shields.io/badge/Postman-Testing-ff6c37)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📚 Tabla de Contenidos

- [Descripción](#-descripción)
- [Objetivo](#-objetivo)
- [Características](#-características)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Arquitectura](#-arquitectura)
- [Instalación](#-instalación)
- [Variables de Entorno](#-variables-de-entorno)
- [Autenticación](#-autenticación)
- [Roles y Permisos](#-roles-y-permisos)
- [Endpoints](#-endpoints)
- [Documentación Swagger](#-documentación-swagger)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Seguridad Implementada](#-seguridad-implementada)
- [Pruebas](#-pruebas)
- [Casos de Uso](#-casos-de-uso)
- [Autor](#-autor)

---

## 📖 Descripción

Esta aplicación es una **API REST profesional desarrollada con Node.js y Express**, diseñada para gestionar el registro, autenticación y autorización de usuarios mediante **JSON Web Tokens (JWT)**.

La solución implementa buenas prácticas de desarrollo backend, incluyendo cifrado seguro de contraseñas, control de acceso basado en roles y permisos, validación de datos, manejo centralizado de errores y documentación automática mediante Swagger.

Está orientada a proyectos que requieran una arquitectura segura, escalable y mantenible para la gestión de usuarios y recursos protegidos.

---

## 🎯 Objetivo

Desarrollar una API REST segura y robusta que permita:

- Registrar nuevos usuarios.
- Autenticar usuarios mediante JWT.
- Proteger contraseñas utilizando bcrypt.
- Gestionar acceso basado en roles y permisos.
- Proteger rutas privadas mediante middleware.
- Realizar operaciones CRUD sobre recursos.
- Documentar la API de forma interactiva con Swagger UI.

---

## 🚀 Características

- ✅ Registro de usuarios
- ✅ Inicio de sesión seguro
- ✅ Autenticación basada en JWT
- ✅ Contraseñas encriptadas con bcrypt
- ✅ Middleware de autenticación
- ✅ Middleware de autorización por roles
- ✅ CRUD completo
- ✅ Validación de datos
- ✅ Manejo centralizado de errores
- ✅ Documentación automática con Swagger
- ✅ Colección de pruebas en Postman

---

## 🛠 Tecnologías Utilizadas

| Tecnología | Uso |
|------------|------|
| Node.js | Entorno de ejecución |
| Express.js | Framework Backend |
| JWT | Autenticación |
| bcrypt | Encriptación de contraseñas |
| Swagger UI | Documentación interactiva |
| Postman | Pruebas de la API |
| GitHub | Control de versiones |

---

## 🏗 Arquitectura

```text
Cliente
   │
   ▼
Express Server
   │
   ├── Middleware JWT
   │
   ├── Middleware Roles
   │
   ├── Controladores
   │
   ├── Servicios
   │
   └── Base de Datos
```

La aplicación sigue una arquitectura por capas para facilitar el mantenimiento, escalabilidad y separación de responsabilidades.

---

## ⚙ Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/usuario/repositorio.git
```

### 2. Acceder al directorio

```bash
cd repositorio
```

### 3. Instalar dependencias

```bash
npm install
```

### 4. Ejecutar la aplicación

```bash
npm run dev
```

---

## 🔑 Variables de Entorno

Crear un archivo `.env` en la raíz del proyecto:

```env
PORT=3000

JWT_SECRET=tu_clave_super_secreta

DATABASE_URL=tu_base_de_datos
```

---

## 🔐 Autenticación

La autenticación se realiza mediante **JSON Web Tokens (JWT)**.

Una vez que el usuario inicia sesión correctamente, el servidor genera un token que deberá enviarse en las peticiones protegidas utilizando el encabezado:

```http
Authorization: Bearer eyJhbGciOiJIUzI1NiIsIn...
```

---

## 👥 Roles y Permisos

La API implementa un sistema de autorización basado en roles para controlar el acceso a los recursos.

| Rol | Permisos |
|------|-----------|
| Admin | Crear, consultar, actualizar y eliminar |
| Usuario | Consultar información |

Los permisos son validados mediante middleware antes de permitir el acceso a rutas protegidas.

---

## 📌 Endpoints

### Autenticación

| Método | Endpoint | Descripción |
|----------|------------|-------------|
| POST | `/register` | Registrar usuario |
| POST | `/login` | Iniciar sesión |

### Usuarios

| Método | Endpoint | Descripción |
|----------|------------|-------------|
| GET | `/users` | Obtener todos los usuarios |
| GET | `/users/:id` | Obtener un usuario |
| POST | `/users` | Crear usuario |
| PUT | `/users/:id` | Actualizar usuario |
| DELETE | `/users/:id` | Eliminar usuario |

---

## 📄 Documentación Swagger

La documentación interactiva se encuentra disponible en:

```text
http://localhost:3000/api-docs
```

Desde Swagger UI podrás:

- Probar todos los endpoints.
- Autenticarte mediante JWT.
- Consultar modelos y esquemas.
- Visualizar respuestas y códigos HTTP.
- Explorar la documentación completa de la API.

---

## 📁 Estructura del Proyecto

```text
src
│
├── controllers/
├── routes/
├── middlewares/
├── services/
├── models/
├── config/
├── docs/
├── utils/
└── app.js
```

---

## 🔒 Seguridad Implementada

La API incorpora múltiples mecanismos de seguridad:

- Contraseñas cifradas con bcrypt.
- Autenticación mediante JWT.
- Middleware de autenticación.
- Middleware de autorización por roles.
- Validación de datos de entrada.
- Manejo centralizado de errores.
- Protección de rutas privadas.

---

## 🧪 Pruebas

La aplicación puede probarse utilizando:

- Swagger UI
- Postman

También se incluye una colección de Postman para facilitar las pruebas de todos los endpoints.

---

## 📌 Casos de Uso

- ✔ Registro de usuarios.
- ✔ Inicio de sesión.
- ✔ Validación de identidad mediante JWT.
- ✔ Consulta de registros.
- ✔ Creación de registros.
- ✔ Actualización de registros.
- ✔ Eliminación de registros.
- ✔ Acceso protegido a recursos.
- ✔ Control de permisos según el rol del usuario.

---

## 📖 Documentación

Toda la documentación de la API se encuentra disponible mediante Swagger:

```text
/api-docs
```

Además, las pruebas pueden realizarse mediante la colección incluida para Postman.

---

## 👨‍💻 Autor

Desarrollado como proyecto académico enfocado en el desarrollo Backend con Node.js y Express.

Este proyecto implementa autenticación JWT, cifrado de contraseñas con bcrypt, control de acceso basado en roles y permisos, documentación automática y buenas prácticas de arquitectura REST para la construcción de APIs seguras y escalables.

---

⭐ Si este proyecto te resulta útil, considera darle una estrella en GitHub.
