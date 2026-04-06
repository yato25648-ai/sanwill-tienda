# 📱 INSTRUCCIONES: DESPLEGAR SANWILL EN VERCEL

## ¿QUÉ ES VERCEL?
Vercel es una plataforma de hosting que permite alojar sitios web de forma **gratuita y automática**. Tu tienda estará disponible en línea 24/7.

---

## 📋 REQUISITOS PREVIOS

Necesitarás:
- ✅ Una cuenta de **GitHub** (gratuita)
- ✅ Una cuenta de **Vercel** (gratuita, vinculada a GitHub)
- ✅ El código del proyecto en tu computadora

---

## 🚀 PASO A PASO: DESPLEGAR EN VERCEL

### PASO 1: CREAR CUENTA EN GITHUB (si no la tienes)

1. Ve a **https://github.com**
2. Haz clic en **"Sign up"** (Registrarse)
3. Completa tu información:
   - **Email**: Tu correo electrónico
   - **Password**: Una contraseña segura
   - **Username**: Tu nombre de usuario (ej: sanwill-tienda)
4. Haz clic en **"Create account"**
5. Confirma tu correo electrónico

**Ya tienes cuenta en GitHub ✅**

---

### PASO 2: CREAR UN NUEVO REPOSITORIO EN GITHUB

1. Inicia sesión en **https://github.com**
2. Haz clic en el **"+"** en la esquina superior derecha
3. Selecciona **"New repository"** (Nuevo repositorio)
4. Completa los datos:
   - **Repository name**: `sanwill-tienda`
   - **Description**: "Tienda en línea de bebidas SANWILL"
   - **Public**: Selecciona esta opción (para que Vercel pueda acceder)
   - **Add a README file**: No marques esta opción
   - **Add .gitignore**: No marques esta opción
   - **Choose a license**: No es necesario
5. Haz clic en **"Create repository"**

**GitHub te mostrará un código para inicializar el repositorio ✅**

---

### PASO 3: SUBIR TU CÓDIGO A GITHUB

Abre la **Terminal/Command Prompt** en tu computadora y ejecuta estos comandos:

```bash
# Navega a la carpeta del proyecto
cd /home/ubuntu/sanwill_tienda

# Inicializa git (si aún no lo has hecho)
git init

# Añade todos los archivos
git add .

# Crea un commit (guardado)
git commit -m "Tienda SANWILL - Inicial"

# Añade el repositorio remoto (reemplaza TU_USUARIO con tu username de GitHub)
git remote add origin https://github.com/TU_USUARIO/sanwill-tienda.git

# Sube el código a GitHub
git branch -M main
git push -u origin main
```

**⚠️ IMPORTANTE:** Cuando ejecutes `git push`, GitHub te pedirá:
- **GitHub username**: Tu nombre de usuario de GitHub
- **GitHub password**: Tu token de acceso personal (PAT)

**Para crear un token:**
1. Ve a **https://github.com/settings/tokens**
2. Haz clic en **"Generate new token"**
3. Dale un nombre: "sanwill-deploy"
4. Marca el checkbox de **"repo"**
5. Copia el token y úsalo como contraseña

**Tu código está en GitHub ✅**

---

### PASO 4: CONECTAR VERCEL A TU REPOSITORIO

1. Ve a **https://vercel.com**
2. Haz clic en **"Sign up"** (o "Log in" si ya tienes cuenta)
3. Selecciona **"Continue with GitHub"**
4. **Autoriza Vercel** para acceder a tu cuenta de GitHub
5. Haz clic en **"Import Project"**
6. Selecciona **"Import Git Repository"**
7. Pega la URL de tu repositorio:
   ```
   https://github.com/TU_USUARIO/sanwill-tienda
   ```
8. Haz clic en **"Continue"**

**Vercel configurará automáticamente tu proyecto ✅**

---

### PASO 5: COMPLETAR LA CONFIGURACIÓN EN VERCEL

En la pantalla de configuración:

- **Project Name**: `sanwill-tienda` (o el nombre que prefieras)
- **Framework Preset**: Selecciona **"Other"** (es un sitio HTML estático)
- **Root Directory**: Deja vacío
- **Build Command**: Deja vacío
- **Output Directory**: Deja vacío

Haz clic en **"Deploy"**

**Vercel está desplegando tu sitio ✅** (Esto toma 1-2 minutos)

---

### PASO 6: ¡TU SITIO ESTÁ EN LÍNEA!

Una vez completado el despliegue:

1. Vercel te mostrará tu **URL pública** (algo como: `https://sanwill-tienda.vercel.app`)
2. Haz clic en esa URL para ver tu tienda en línea
3. **Guarda esa URL** - Es tu dominio permanente

---

## 🔄 ¿CÓMO ACTUALIZAR EL SITIO?

Si haces cambios en tu código y los subes a GitHub, Vercel **automáticamente** desplegará los cambios:

```bash
# En tu terminal, dentro del proyecto
git add .
git commit -m "Descripción del cambio"
git push
```

Vercel detectará el cambio y redesplegará el sitio automáticamente.

---

## 🎯 INFORMACIÓN ÚTIL

### Tu URL permanente será algo como:
```
https://sanwill-tienda.vercel.app
```

### Donde aparece tu sitio:
- Google
- Redes sociales (cuando compartes el enlace)
- Clientes que acceden desde cualquier dispositivo

### Características incluidas:
✅ **HTTPS automático** - Conexión segura
✅ **Dominio .vercel.app** - Gratuito
✅ **Actualizaciones automáticas** - Sin hacer nada extra
✅ **Ancho de banda ilimitado** - Sin costos ocultos
✅ **SSL incluido** - Tu sitio es seguro

---

## ❓ PREGUNTAS FRECUENTES

### P: ¿Cuánto cuesta?
**R:** Completamente gratis para sitios estáticos como el tuyo.

### P: ¿Mi sitio estará activo 24/7?
**R:** Sí, siempre estará en línea.

### P: ¿Puedo usar un dominio personalizado?
**R:** Sí, Vercel permite agregar dominios personalizados (en la configuración del proyecto).

### P: ¿Dónde veo mis estadísticas?
**R:** En el panel de Vercel dentro de tu proyecto.

### P: ¿Qué pasa si hay errores?
**R:** Vercel te notificará y puedes revisar los logs en el panel.

---

## 📞 SOPORTE

Si tienes problemas:
- Vercel tiene una excelente documentación: **https://vercel.com/docs**
- GitHub Help: **https://docs.github.com**
- Comunidad de Vercel: **https://github.com/vercel/next.js/discussions**

---

## ✅ CHECKLIST FINAL

Antes de desplegar, verifica:

- [ ] Todos los archivos están en `/home/ubuntu/sanwill_tienda/`
- [ ] El archivo `index.html` existe
- [ ] La carpeta `/images/` contiene todas las bebidas
- [ ] El archivo `vercel.json` está creado
- [ ] El archivo `.gitignore` está creado
- [ ] El archivo `package.json` está creado
- [ ] Tienes una cuenta de GitHub
- [ ] Git está inicializado en el proyecto
- [ ] Los cambios están commiteados en git
- [ ] El código está subido a GitHub
- [ ] Vercel está conectado a tu repositorio
- [ ] Tu sitio está en línea

---

**¡Felicidades! Tu tienda SANWILL está en línea 🎉**

*Recuerda compartir tu URL con tus clientes:*
```
https://tu-usuario.vercel.app/sanwill-tienda
```

---

*Última actualización: Abril 2025*
