# Logimétrica V41 — Sistema de Operaciones de Almacén

Sistema web de gestión operativa para almacenes. Single-file HTML con integración Firebase Auth.

## 🚀 Publicar en GitHub Pages

1. Sube este repositorio a GitHub
2. Ve a **Settings → Pages**
3. En *Branch* selecciona `main` y carpeta `/root`
4. Guarda — en ~1 min estará en `https://tu-usuario.github.io/logimetrica/`

## 🔐 Modos de Login

| Modo | Cómo usarlo |
|------|-------------|
| Admin local | Usuario: `admin` / Contraseña: `admin123` |
| Firebase Auth | Ingresa el **correo** y **contraseña** registrados en Firebase |

Los usuarios locales (creados desde el panel Admin) usan su nombre de usuario.  
Los usuarios Firebase usan su correo electrónico completo.

## ⚙️ Configuración Firebase

El archivo `index.html` ya incluye la configuración de tu proyecto Firebase:

```js
const firebaseConfig = {
  apiKey: "AIzaSyBD7rDFK7VEJn_gghds8Gtj9NGEGAeNCNs",
  authDomain: "prueba1-10f2e.firebaseapp.com",
  projectId: "prueba1-10f2e",
  ...
};
```

Para cambiar de proyecto Firebase, edita ese bloque en `index.html`.

## 📦 Módulos incluidos

- **Inicio** — KPIs, foto de equipo, acceso rápido
- **Asistencia** — Control diario con estados configurables
- **Apoyo** — Registro de carga/armado con ranking
- **Ingreso** — Carga de KardexIngreso Excel, pallets rack vs picking
- **Consolidado** — Excel de consolidado, digitador vs armador
- **Salida** — KardexSalida, solicitante/abastecedor/apilador
- **OV / Consultas** — Contador click + tickets de cambio de lote
- **Dashboard General** — Ranking, radar de competencias, gráficos
- **Dashboard Incidencias** — Estadísticas de infracciones
- **Dashboard Apiladores** — Solo usuarios con título APILADOR
- **Observaciones** — Registro y seguimiento
- **Infracciones** — Registro con tipos configurables
- **Inducción** — Manual editable por supervisores
- **Administración** — Usuarios, permisos, pesos, bitácora
- **Permisos** — Control de acceso por módulo y usuario

## 🛠️ Tecnologías

- HTML/CSS/JS puro (sin frameworks)
- [SheetJS](https://sheetjs.com/) para lectura de Excel
- [Firebase Auth](https://firebase.google.com/docs/auth) para autenticación
- Google Fonts (Plus Jakarta Sans + JetBrains Mono)

## 📝 Notas

- Los datos son **en memoria** (se pierden al recargar). Para persistencia total, conectar Firestore.
- El chat (LogiChat) es local por sesión, sin backend real-time.
- Compatible con Chrome, Edge, Firefox modernos.
