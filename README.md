<div align="center">

# ¡Hola! 👋 Soy ManChoi

**Técnico de Soporte IT N2** con base en Lima, Perú 🇵🇪 — 5+ años gestionando endpoints, identidad y nube.
Fuera del trabajo construyo sistemas de agentes de IA que corren 24/7 — arrancaron en una Raspberry Pi 3 y hoy corren en un servidor x86_64, sin perder las costumbres que la Pi impuso.

[![GitHub](https://img.shields.io/badge/GitHub-Manxoig-181717?style=for-the-badge&logo=github)](https://github.com/Manxoig)

</div>

---

### 🌙 En qué ando ahora — un mismo sistema, dos hardware distintos 🖖

Empezó en una **Raspberry Pi 3 Model B** headless con 1 GB de RAM: ese techo obligó a declarar
todo presupuesto de memoria, timeout y concurrencia en vez de asumirlo. Hoy el grueso corre en un
**servidor x86_64** con 15 veces esa RAM, y la Pi quedó de nodo de respaldo — veterana, no
retirada: cumplió su turno bajo 1 GB de RAM sin pedir más, y eso en esta casa se dice con una
sola palabra: **Qapla'** 🗡️. El sistema sigue pensando en nodos plural, no en una sola máquina:
cada límite se declara **por nodo de ejecución**, así que lo que protege a la Pi no asfixia al
servidor grande, y viceversa. De ese contraste —diseñar primero para lo chico, escalar después a
lo grande sin reescribir— salieron la mayoría de las habilidades que vengo afilando:

**Backend y arquitectura**
- 🐍 **APIs REST en Python con FastAPI**, partidas por dominio (varios routers en vez de un archivo monolítico), con Pydantic para validar y HTTPS/TLS para servir
- 🗄️ **SQLite en modo WAL** como única fuente de verdad compartida entre procesos independientes, sin broker de mensajes
- 🎫 **Máquinas de estado explícitas** (estilo ITIL) con una sola función de transición, que rechaza en vez de aplicar en silencio lo que no está en la tabla
- 🧠 **Grafos de propiedades** para modelar agentes, capacidades y reglas de negocio como datos — un límite se cambia desde una interfaz, no desplegando código
- 🔀 **Enrutamiento de trabajo por agente**, con desambiguación explícita cuando dos reglas podrían matchear lo mismo
- 🧩 **Frontend estático en vanilla JS** — sin build, sin framework, con los módulos compartidos (estado→interfaz, navegación, sanitizado de markdown) factorizados una sola vez

**Operación, gobernanza y hardware**
- ⚙️ **Presupuestos de recursos declarados por nodo de ejecución** (timeout, RAM, concurrencia) para que el mismo código corra seguro tanto en la Pi como en el servidor grande
- 🔒 **Endurecimiento Linux**: firewall UFW, certificados TLS, y detección activa de credenciales filtradas antes de aceptar un resultado generado por IA
- ✅ **Puertas humanas auditadas** — nada crítico se publica, cobra o escala sin una aprobación que queda registrada, con su propio veredicto y motivo
- 🧪 **Pruebas estáticas sobre la arquitectura** (análisis por AST, sin pytest): no sólo corren el código, verifican que nadie viole una invariante de diseño
- 📡 **Integración con APIs externas con degradación controlada** — si falta una credencial, el sistema lo dice y no inventa un número
- 🖥️ **systemd en modo usuario** (servicios y timers) con techos de recursos generados por nodo, y migración de una infraestructura ARM64 a x86_64 sin perder continuidad de datos

---

### 🛠️ Stack profesional (soporte y nube)

![Intune](https://img.shields.io/badge/-Microsoft%20Intune-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![SCCM](https://img.shields.io/badge/-SCCM%2FMECM-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![M365](https://img.shields.io/badge/-Microsoft%20365-D83B01?style=flat-square&logo=microsoft-office&logoColor=white)
![Active Directory](https://img.shields.io/badge/-Active%20Directory-0078D4?style=flat-square&logo=windows&logoColor=white)
![Windows Server](https://img.shields.io/badge/-Windows%20Server-0078D4?style=flat-square&logo=windows&logoColor=white)
![ServiceNow](https://img.shields.io/badge/-ServiceNow-00C487?style=flat-square&logo=servicenow&logoColor=white)
![Jira Service Management](https://img.shields.io/badge/-Jira%20SM-0052CC?style=flat-square&logo=jira&logoColor=white)

![GCP](https://img.shields.io/badge/-Google%20Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Azure](https://img.shields.io/badge/-Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

### 🖥️ Stack del laboratorio (Pi 3 + servidor x86_64)

![Raspberry Pi](https://img.shields.io/badge/-Raspberry%20Pi%203B-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![Debian](https://img.shields.io/badge/-Debian%2013%20trixie-A81D33?style=flat-square&logo=debian&logoColor=white)
![Python](https://img.shields.io/badge/-Python%203.13-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Uvicorn](https://img.shields.io/badge/-Uvicorn-499848?style=flat-square&logo=gunicorn&logoColor=white)
![SQLite](https://img.shields.io/badge/-SQLite%20(WAL)-003B57?style=flat-square&logo=sqlite&logoColor=white)
![systemd](https://img.shields.io/badge/-systemd-30D475?style=flat-square&logo=linux&logoColor=black)
![Nginx-free TLS](https://img.shields.io/badge/-HTTPS%2FTLS-005571?style=flat-square&logo=letsencrypt&logoColor=white)
![UFW](https://img.shields.io/badge/-UFW%20Firewall-EF3B2D?style=flat-square&logo=iptables&logoColor=white)

### 💻 Stack personal (estación de trabajo y desarrollo)

![CachyOS](https://img.shields.io/badge/-CachyOS%20(Arch)-1793D1?style=flat-square&logo=archlinux&logoColor=white)
![KDE Plasma](https://img.shields.io/badge/-KDE%20Plasma-1D99F3?style=flat-square&logo=kde&logoColor=white)
![Wayland](https://img.shields.io/badge/-Wayland-FFBC00?style=flat-square&logo=wayland&logoColor=black)
![C#](https://img.shields.io/badge/-C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Shell](https://img.shields.io/badge/-Shell%20Script-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)
![Claude Code](https://img.shields.io/badge/-Claude%20Code-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Ollama](https://img.shields.io/badge/-Ollama-000000?style=flat-square&logo=ollama&logoColor=white)

---

### 📌 Proyectos propios

| Repo | Lenguaje | Descripción |
|---|---|---|
| [`ninxa`](https://github.com/Manxoig/ninxa) | JavaScript | Agente basado en Ollama |
| [`raspkali`](https://github.com/Manxoig/raspkali) | Python | Kali Linux ejecutado en una Raspberry Pi |
| [`lcars_manxoig`](https://github.com/Manxoig/lcars_manxoig) | Shell | Escritorio con interfaz LCARS |
| [`CharV`](https://github.com/Manxoig/CharV) | C# | Proyecto en C# (GPL-3.0) |

---

<div align="center">

📍 Lima, Perú &nbsp;·&nbsp; 🐧 CachyOS + KDE Plasma &nbsp;·&nbsp; 🌙 Agentes IA en Pi 3 + x86_64 &nbsp;·&nbsp; 🔧 Soporte IT N2

</div>
