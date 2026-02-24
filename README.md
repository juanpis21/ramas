# ADSO-3063267 - NestJS Multi-Environment API

Proyecto NestJS configurado para múltiples entornos con PostgreSQL, TypeORM y documentación Swagger.

## 🚀 Características

- **NestJS Framework** - Backend API robusto y escalable
- **TypeORM** - ORM para PostgreSQL
- **Multi-entorno** - Configuración para desarrollo, staging y producción
- **Swagger** - Documentación automática de API
- **Validación** - Class-validator y class-transformer
- **Docker** - Contenerización para todos los entornos
- **Testing** - Unit tests y e2e tests configurados

## 📋 Requisitos Previos

- Node.js 18+
- PostgreSQL 14+
- Docker (opcional)
- Git

## 🛠️ Instalación

```bash
# Clonar el repositorio
git clone <repository-url>
cd ramas

# Cambiar a rama de desarrollo
git checkout develop

# Instalar dependencias
npm install
```

## 🔧 Configuración de Entornos

El proyecto está configurado para múltiples entornos:

### Entornos Disponibles

- **develop**: Desarrollo local (puerto 3000)
- **staging**: Pre-producción (puerto 3001)  
- **master**: Producción (puerto 3002)

### Variables de Entorno

Copia y configura los archivos de entorno según necesites:

```bash
# Desarrollo
cp .develop.env .env

# Staging
cp .staging.env .env

# Producción
cp .production.env .env
```

## 🏃‍♂️ Ejecución

### Desarrollo

```bash
# Modo desarrollo con hot-reload
npm run start:dev

# Modo debug
npm run start:debug
```

### Producción

```bash
# Construir aplicación
npm run build

# Iniciar producción
npm run start:prod
```

### Staging

```bash
npm run start:stg
```

## 🐳 Docker

### Desarrollo

```bash
docker-compose up
```

### Staging

```bash
docker-compose -f docker-compose.stg.yml up
```

### Producción

```bash
docker-compose -f docker-compose.prod.yml up
```

## 📚 Documentación API

Una vez iniciada la aplicación, accede a la documentación Swagger:

- **Desarrollo**: http://localhost:3000/api
- **Staging**: http://localhost:3001/api
- **Producción**: http://localhost:3002/api

## 🧪 Testing

```bash
# Ejecutar todos los tests
npm test

# Tests en modo watch
npm run test:watch

# Coverage
npm run test:cov

# Tests e2e
npm run test:e2e
```

## 📁 Estructura del Proyecto

```
src/
├── app.controller.ts          # Controlador principal
├── app.module.ts              # Módulo raíz
├── app.service.ts             # Servicio principal
├── config.ts                  # Configuración de la aplicación
├── database/                  # Configuración de base de datos
├── enviroments.ts             # Variables de entorno
├── main.ts                    # Punto de entrada
└── users/                     # Módulo de usuarios
    ├── entities/              # Entidades TypeORM
    ├── controllers/           # Controladores
    ├── services/              # Servicios
    └── dto/                   # Data Transfer Objects
```

## 🔍 Scripts Disponibles

- `npm run build` - Compila TypeScript
- `npm run format` - Formatea código con Prettier
- `npm run start` - Inicia aplicación
- `npm run start:dev` - Desarrollo con watch
- `npm run start:debug` - Modo debug
- `npm run start:prod` - Producción
- `npm run lint` - Linting con ESLint
- `npm run test` - Ejecuta tests unitarios
- `npm run test:e2e` - Tests end-to-end
- `npm run test:cov` - Coverage de tests

## 🚀 Despliegue

### Desarrollo

1. Asegúrate de estar en la rama `develop`
2. Configura las variables de entorno
3. Ejecuta `npm run start:dev`

### Staging

1. Cambia a la rama `staging`
2. Usa `docker-compose.stg.yml` o `npm run start:stg`

### Producción

1. Cambia a la rama `master`
2. Usa `docker-compose.prod.yml` o `npm run start:prod`

## 🤝 Contribución

1. Crea una feature branch desde `develop`
2. Realiza tus cambios
3. Ejecuta los tests: `npm test`
4. Commitea tus cambios
5. Push a la rama
6. Crea un Pull Request

## 📝 Licencia

UNLICENSED

## 👥 Autor

**monic305** - Desarrollo inicial

---

Para más información sobre NestJS, visita [https://nestjs.com](https://nestjs.com)
