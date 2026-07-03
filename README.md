
# Actividad Práctica – Instalación de n8n y Primer Workflow "Hola Mundo"

## Integrante

- Jessica Urrego

---

# Método de instalación utilizado

Instalación local utilizando Node.js, npm y nvm-windows.

---

# Requisitos previos

- Windows 11 (o la versión que tengas)
- Node.js 24.16.0
- npm 11.13.0
- nvm-windows 1.2.2
- Conexión a Internet

---

# Proceso de instalación

## 1. Instalación de nvm-windows

Se instaló nvm-windows para administrar diferentes versiones de Node.js.

## 2. Instalación de Node.js

Se instaló la versión:

```bash
nvm install 24.16.0
```

Se activó con:

```bash
nvm use 24.16.0
```

Verificación:

```bash
node -v
```

Resultado:

```text
v24.16.0
```

Verificación de npm:

```bash
npm -v
```

Resultado:

```text
11.13.0
```

## 3. Instalación de n8n

Se ejecutó:

```bash
npm install -g n8n
```

Para iniciar n8n:

```bash
n8n start
```

El editor quedó disponible en:

```text
http://localhost:5678
```

---

# Problemas encontrados

Durante la instalación apareció el siguiente error:

```text
ECONNRESET
```

La instalación se interrumpía debido a un problema de red y además se estaba utilizando Node.js 26, el cual presentó incompatibilidades con n8n.

## Solución

- Se instaló nvm-windows.
- Se cambió a Node.js 24.16.0.
- Se ejecutó nuevamente la instalación de n8n.
- La instalación finalizó correctamente.

---

# Workflow "Hola Mundo"

## Objetivo

Crear un flujo sencillo para comprobar que n8n funciona correctamente.

## Nodos utilizados

### Manual Trigger

Inicia manualmente la ejecución del workflow.

### Set

Se creó un campo llamado:

| Campo | Valor |
|--------|-------|
| mensaje | Hola Mundo desde n8n |

El flujo quedó:

```
Manual Trigger
      ↓
      Set
```

Después de ejecutar el flujo, el nodo Set mostró el mensaje:

```
Hola Mundo desde n8n
```

---

# Evidencias

Agregar las siguientes capturas:

- Instalación de Node.js
- Instalación de n8n
- Dashboard de n8n
- Workflow creado
- Ejecución exitosa
- Resultado del nodo Set
<p>
  <img src="img/errorConnectividad.png.png" width="700">
</p>

---

# Explicación de los nodos

## Manual Trigger

Permite iniciar el flujo manualmente desde el editor de n8n.

## Set

Permite crear variables o modificar datos dentro del flujo. En este caso se creó el mensaje "Hola Mundo desde n8n".

---

# Reflexión Técnica

## 1. ¿Qué fue lo más difícil de la instalación?

Lo más difícil fue solucionar los errores durante la instalación de n8n. Inicialmente se presentó un error de conexión (ECONNRESET) y posteriormente fue necesario cambiar la versión de Node.js utilizando nvm para lograr una instalación compatible.

## 2. ¿Qué ventajas tiene n8n?

- Es gratuito y de código abierto.
- Permite automatizar tareas sin necesidad de programar mucho.
- Tiene una gran cantidad de integraciones.
- Es fácil crear flujos visuales.

## 3. ¿Qué diferencia encontraron entre Docker y la instalación local?

La instalación local es más sencilla para aprender y realizar pruebas. Docker facilita la portabilidad y el despliegue en otros equipos o servidores, además de mantener un entorno aislado.

## 4. ¿Para qué casos reales usarían automatización?

- Envío automático de correos.
- Integración entre aplicaciones.
- Generación de reportes.
- Notificaciones automáticas.
- Procesamiento de formularios.

## 5. ¿Qué les gustaría automatizar en el futuro?

Me gustaría automatizar la recepción de información desde formularios, el envío de correos automáticos y procesos que integren herramientas de inteligencia artificial con aplicaciones como Google Sheets y WhatsApp.

---

# Conclusión

Se realizó correctamente la instalación local de n8n utilizando Node.js y npm. Después de solucionar los problemas de compatibilidad con la versión de Node.js, fue posible ejecutar el primer workflow "Hola Mundo", comprobando el funcionamiento de la plataforma y comprendiendo los conceptos básicos de automatización.