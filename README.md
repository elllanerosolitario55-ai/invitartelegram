# 📱 Telegram Mass Inviter

Herramienta web para gestionar invitaciones masivas a grupos de Telegram. Desplegable en Netlify.

![Telegram Inviter](https://img.shields.io/badge/Telegram-Inviter-blue?style=for-the-badge&logo=telegram)
![Netlify Ready](https://img.shields.io/badge/Netlify-Ready-00C7B7?style=for-the-badge&logo=netlify)

## ✨ Características

- 🎯 **Configuración del Grupo**: Define nombre, enlace de invitación y descripción
- 📝 **Plantillas Personalizables**: Usa variables como `{nombre}`, `{grupo}` y `{enlace}`
- 📤 **Importación CSV**: Carga contactos desde archivos CSV/TXT
- 📱 **Envío por WhatsApp**: Abre conversaciones listas para enviar
- 📊 **Estadísticas**: Seguimiento de enviados, pendientes y fallidos
- 💾 **Persistencia Local**: Los datos se guardan automáticamente
- 🎨 **Interfaz Moderna**: Diseño dark mode con animaciones

## 🚀 Despliegue en Netlify

### Opción 1: Deploy Directo (Drag & Drop)

1. Ve a [netlify.com](https://www.netlify.com/) e inicia sesión
2. En el dashboard, arrastra la carpeta `telegram-inviter` al área de deploy
3. ¡Listo! Tu app estará disponible en una URL de Netlify

### Opción 2: Desde GitHub

1. Sube este proyecto a un repositorio de GitHub
2. En Netlify, haz clic en "New site from Git"
3. Conecta tu repositorio de GitHub
4. Configura:
   - **Build command**: (dejar vacío)
   - **Publish directory**: `.`
5. Haz clic en "Deploy site"

### Opción 3: Netlify CLI

```bash
# Instalar Netlify CLI
npm install -g netlify-cli

# Login en Netlify
netlify login

# Deploy del proyecto
cd telegram-inviter
netlify deploy --prod
```

## 📋 Formato del CSV

El archivo CSV debe tener el siguiente formato:

```csv
nombre,telefono
Juan García,+34612345678
María López,+34698765432
Pedro Sánchez,+1234567890
```

**Notas:**
- El teléfono debe incluir el código de país (+34, +1, etc.)
- La primera línea puede ser el encabezado (se detecta automáticamente)
- Separadores soportados: coma (,), punto y coma (;), tabulador

## 📱 Variables Disponibles

| Variable | Descripción |
|----------|-------------|
| `{nombre}` | Nombre del contacto |
| `{grupo}` | Nombre del grupo configurado |
| `{enlace}` | Enlace de invitación del grupo |

## 💡 Ejemplo de Mensaje

```
¡Hola {nombre}! 👋

Te invito a unirte a nuestro grupo de Telegram "{grupo}".

👉 {enlace}

¡Te esperamos!
```

## ⚠️ Consideraciones

- **WhatsApp Web**: Debes tener WhatsApp Web abierto en tu navegador
- **Límites**: WhatsApp puede limitar el número de mensajes enviados
- **Privacidad**: Los contactos se almacenan localmente en tu navegador
- **Consentimiento**: Asegúrate de tener permiso para contactar a las personas

## 🛠️ Tecnologías

- HTML5
- CSS3 (Custom Properties, Flexbox, Grid)
- JavaScript (ES6+)
- LocalStorage para persistencia
- WhatsApp Web API
- Telegram Share API

## 📄 Licencia

Este proyecto es de uso libre para fines personales y comerciales.

---

Desarrollado con 💙 para la comunidad
