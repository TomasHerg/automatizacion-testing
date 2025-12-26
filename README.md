# Testing Automation Portfolio

Portfolio de proyectos de automatización de pruebas con diferentes frameworks y herramientas de testing.

---

## 📋 Proyectos Incluidos

1. [Postman - API Testing](#1-postman---api-testing)
2. [Cypress - E2E Testing](#2-cypress---e2e-testing)
3. [Playwright - E2E Testing](#3-playwright---e2e-testing)
4. [Cucumber - BDD Testing](#4-cucumber---bdd-testing)

---

## 1. Postman - API Testing

Suite completa de pruebas automatizadas para API REST con flujo de autenticación y operaciones CRUD.

### 🚀 Ejecutar

**Opción 1: Postman (recomendado)**
1. Abrir Postman
2. Importar `tarea5.postman_collection.json`
3. Importar `tarea5.postman_environment.json`
4. Seleccionar environment "Laboratorio"
5. Click en "Run collection"

**Opción 2: Newman (CLI)**
```bash
npm install -g newman
newman run tarea5.postman_collection.json -e tarea5.postman_environment.json
```

### 🧪 Tests Incluidos
- Autenticación con token Bearer
- CRUD completo de órdenes (Create, Read, Update, Delete)
- Validación de status codes y respuestas JSON
- Generación automática de datos de prueba
- 9 endpoints testeados con scripts automatizados

---

## 2. Cypress - E2E Testing

Suite de pruebas end-to-end con Cypress para validación de flujo de autenticación.

### 🚀 Ejecutar

```bash
cd tarea_cypress

# Instalar dependencias (solo primera vez)
npm install

# Abrir Cypress en modo interactivo
npx cypress open

# Ejecutar tests en modo headless
npx cypress run
```

### 🧪 Tests Incluidos
- 6 escenarios de login con fixtures para datos de prueba
- Validación de headers y elementos del DOM
- Login exitoso y fallido con diferentes combinaciones
- Verificación de mensajes de error específicos

### ⚠️ Nota
Proyecto funcional que cumple con los requisitos de la materia. Contiene validaciones de headers repetidas en cada test que podrían extraerse a funciones helper, pero no se refactorizó por tiempos de entrega ajustados.

---

## 3. Playwright - E2E Testing

Suite de pruebas end-to-end para validación de flujo de autenticación con 9 escenarios.

### 🚀 Ejecutar

```bash
cd tarea_8_playwright

# Instalar dependencias (solo primera vez)
npm install
npx playwright install

# Ejecutar tests
npx playwright test

# Ver reporte
npx playwright show-report
```

### 🧪 Tests Incluidos
- Login exitoso y fallido con diferentes combinaciones
- Validación de credenciales válidas/inválidas
- Verificación de campos vacíos
- Comprobación de mensajes de error

### ⚠️ Nota
Proyecto funcional que cumple con los requisitos de la materia. Contiene código repetido identificado (uso de `beforeEach`, constantes compartidas) que no se refactorizó por tiempos de entrega ajustados.

---

## 4. Cucumber - BDD Testing

Suite de pruebas automatizadas con metodología BDD (Behavior Driven Development) usando Cucumber + Playwright.

### 🚀 Ejecutar

```bash
cd tarea_9_cucumber

# Instalar dependencias (solo primera vez)
npm install

# Ejecutar tests
npm test
```

### 🧪 Tests Incluidos
- 6 escenarios de login escritos en Gherkin (Given-When-Then)
- Validación de credenciales y campos vacíos
- Verificación de mensajes de error en el DOM

### ⚠️ Nota
Proyecto funcional que cumple con los requisitos de la materia. Contiene step definitions duplicados que podrían consolidarse en funciones genéricas reutilizables, pero no se refactorizó por tiempos de entrega ajustados.

---

## 🛠️ Tecnologías Utilizadas

| Proyecto | Tecnologías | Framework |
|----------|-------------|-----------|
| Postman | JavaScript, REST API | Postman/Newman |
| Cypress | JavaScript, Node.js | Cypress |
| Playwright | JavaScript, Node.js | Playwright Test |
| Cucumber | JavaScript, Gherkin, Playwright | Cucumber.js |

---

## 📝 Notas

- Proyectos desarrollados para el curso de Verificación y Validación de Software
- Los proyectos Cypress, Playwright y Cucumber priorizaron funcionalidad dentro de plazos académicos sobre optimización de código
- Cada proyecto es independiente y puede ejecutarse por separado
- **Importante:** Todos los tests fueron realizados sobre endpoints de la página del departamento de computación de la Universidad Nacional del Sur con la debida autorización del docente a cargo de la materia Verificación y Validación de Software

