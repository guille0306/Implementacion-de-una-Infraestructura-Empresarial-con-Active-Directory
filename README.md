# Implementación de una Infraestructura Empresarial con Active Directory

El fin de esta práctica es implementar una infraestructura empresarial basada en **Windows Server 2022** y **Active Directory**, con el fin de:

- Centralizar la gestión de usuarios y recursos de la empresa.
- Aplicar políticas de seguridad mediante GPO.
- Garantizar la protección de los datos mediante copias de seguridad.
- Mejorar la seguridad con firewall, antivirus y proxy inverso.
- Facilitar la administración remota mediante Windows Admin Center.
- Analizar el consumo energético para dimensionar correctamente un SAI.

## Prerrequisitos

- **OS:** Windows Server 2022
  - Active Directory Domain Services (AD DS)
  - DNS
  - IIS
  - Windows Server Backup
  - Windows Admin Center
  - Firewall de Windows

- **OS:** Windows 10 (Cliente)
  - Unión al dominio
  - Aplicación de políticas GPO

- **Herramientas**
  - VirtualBox
  - Malwarebytes
  - PowerShell
  - Pinza amperimétrica
  - SAI

---

## Práctica

### Instalación de Windows Server

Se instala Windows Server 2022 en una máquina virtual configurando los recursos hardware necesarios. Posteriormente se realiza la configuración inicial del sistema operativo para preparar la instalación de los servicios corporativos.
<img width="656" height="351" alt="image" src="https://github.com/user-attachments/assets/8e15dbe2-b896-4fcd-a497-7d284d79a6a0" />

---

### Configuración de Active Directory

Se instala el rol **Active Directory Domain Services (AD DS)** y se promociona el servidor a controlador de dominio, creando un nuevo bosque y configurando el servicio DNS para la resolución de nombres del dominio.

---

### Creación de usuarios, grupos y Unidades Organizativas

Se crean las diferentes Unidades Organizativas (OU), grupos de seguridad y usuarios correspondientes a cada departamento de la empresa, facilitando una administración centralizada de todos los recursos.
<img width="593" height="328" alt="image" src="https://github.com/user-attachments/assets/0d6425f5-dc05-4778-847d-aab00cda9197" />

---

### Configuración de Directivas de Grupo (GPO)

Se implementan diferentes políticas de grupo adaptadas a cada departamento, restringiendo el acceso a determinadas herramientas administrativas, bloqueando dispositivos USB y limitando la ejecución de aplicaciones como CMD, PowerShell o el Editor del Registro cuando sea necesario.
<img width="311" height="280" alt="image" src="https://github.com/user-attachments/assets/e46d5c02-b201-47e1-bd0c-7cefd8502611" />

---

### Configuración del Firewall

Se configuran reglas de entrada y salida para proteger los servicios de la empresa, permitiendo únicamente las conexiones necesarias y bloqueando accesos no autorizados.
<img width="687" height="394" alt="image" src="https://github.com/user-attachments/assets/bf03fb37-93b9-4861-9f32-c99304cf2849" />

---

### Instalación del Antivirus

Se instala Malwarebytes como solución antivirus, habilitando la protección en tiempo real y configurando análisis automáticos para detectar y eliminar amenazas.
<img width="840" height="298" alt="image" src="https://github.com/user-attachments/assets/ed837d1a-a9ef-4926-92d6-833d9e93e6c6" />

---

### Configuración del Proxy Inverso

Se instala IIS junto con Application Request Routing (ARR) para configurar un proxy inverso encargado de recibir las solicitudes web y redirigirlas a los servicios internos correspondientes.
<img width="1101" height="438" alt="image" src="https://github.com/user-attachments/assets/4c781b32-a47c-4347-aa35-1628d1d7e998" />

---

### Windows Admin Center

Se instala Windows Admin Center para administrar de forma remota toda la infraestructura, permitiendo supervisar servidores, ejecutar scripts de PowerShell y gestionar usuarios desde una única interfaz.
<img width="291" height="193" alt="image" src="https://github.com/user-attachments/assets/ff4d3971-4b06-47d9-a446-c4666068e893" />

---

### Configuración del SAI

Mediante una pinza amperimétrica se mide el consumo eléctrico de los equipos de la infraestructura. Con los valores obtenidos se calcula la potencia necesaria del Sistema de Alimentación Ininterrumpida (SAI), seleccionando un modelo de 4500 VA para garantizar la continuidad del servicio.
<img width="768" height="429" alt="image" src="https://github.com/user-attachments/assets/fbf514d0-3b21-4a65-9f5d-3da72f0c6985" />

---

### Programación de Copias de Seguridad

Se configura Windows Server Backup para realizar copias de seguridad automáticas en un servidor de respaldo siguiendo una planificación semanal basada en copias completas, incrementales y diferenciales.
<img width="728" height="294" alt="image" src="https://github.com/user-attachments/assets/bb363e80-e920-4765-b18b-1103ed19f363" />

---

### Automatización mediante PowerShell

Se desarrolla un script en PowerShell que permite crear automáticamente usuarios en Active Directory a partir de un archivo CSV, agilizando el proceso de incorporación de nuevos empleados.
![Uploading image.png…]()

---
