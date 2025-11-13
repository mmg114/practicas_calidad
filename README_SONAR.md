# 🚀 Guía rápida para ejecutar SonarQube con Docker Compose

## 📌 1. Ejecutar Docker Compose

Para levantar todos los servicios definidos en tu archivo `docker-compose-sonar.yml`, utiliza:

```
docker compose -f docker-compose-sonar.yml up -d
```

- `up` → crea y levanta los contenedores
- `-d` → modo *detached` (en segundo plano)

---

## 🔐 2. Usuario y contraseña por defecto de SonarQube

Después de iniciar el servicio, abre en tu navegador:

👉 **http://localhost:9000**

Las credenciales por defecto son:

| Tipo      | Valor     |
|-----------|-----------|
| **Usuario**   | `admin` |
| **Contraseña** | `admin` |

> 💡 La primera vez que ingresas, SonarQube te pedirá cambiar la contraseña obligatoriamente.

---

## 📁 3. Ruta por defecto de acceso

Una vez levantado el contenedor:

- URL de acceso a SonarQube: **http://localhost:9000**
- Si usaste otro puerto, reemplaza `9000` por el que asignaste.

Ejemplo:

```
ports:
  - "9100:9000"
```

Acceso:

👉 **http://localhost:9100**

---

## 📄 4. Ver logs del contenedor (opcional)

Si necesitas revisar el estado de SonarQube:

```
docker logs -f sonarqube
```

---

## 🎯 Con esto ya puedes:
- Levantar SonarQube
- Acceder a la interfaz web
- Iniciar sesión con las credenciales por defecto
- Validar que todo esté funcionando correctamente
