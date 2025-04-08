# Práctica Final - Prometheus y Grafana

Este proyecto consiste en la creación de un entorno de monitoreo utilizando **Prometheus**, **Grafana** y **Node Exporter**, con métricas simuladas, paneles personalizados y dashboards organizados según una serie de requerimientos.

---

## 📦 Contenido del proyecto

```
.
├── docker-compose.yml
├── prometheus.yml
├── grafana/
│   ├── dashboards/
│   │   ├── metricas_latencia.json
│   │   └── recursos_sistema.json

---

## 🚀 Servicios incluidos

- **Prometheus**: servidor de monitoreo
- **Grafana**: visualización de métricas
- **Node Exporter**: métricas de sistema
- **Servicios demo**: exponen endpoints con métricas simuladas

---

## ⚙️ Cómo levantar el entorno

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/raamirezz/practica-final-prometheus.git
   cd practica-final-prometheus
   ```

2. Levantar los contenedores:
   ```bash
   docker-compose up -d
   ```

3. Acceder a los servicios:

   - Prometheus: http://localhost:9090  
   - Grafana: http://localhost:3000  
     - Usuario: `admin`
     - Contraseña: `admin`

---

## 📊 Dashboards incluidos

### 🔹 1. Dashboard de métricas HTTP (latencia)

Contiene **3 paneles** en un mismo dashboard:

- Percentil 90 de tiempo de respuesta
- Percentil 95 de tiempo de respuesta
- Promedio de duración de solicitudes

---

### 🔹 2. Dashboard de recursos de cómputo

Contiene **una fila (`row`)** con:

- Panel **Stat**: número de CPUs
- Panel **Gauge**: porcentaje de uso del disco `/` con umbrales de color:
  - 🟠 80%
  - 🔴 90%

🗂️ Archivo: `grafana/dashboards/dashboard-recursos.json`

---

## ✅ Notas

- Las métricas utilizadas (`demo_...`) provienen de los servicios `julius/prometheus-demo-service`.
- En este entorno de práctica, el uso del disco se considera representativo del sistema de ficheros raíz (`/`) al no haber métricas más detalladas por montaje.

---

## ✍️ Autor

Carlos Ramírez  
[GitHub: @raamirezz](https://github.com/raamirezz)

---

## 📄 Licencia

Este proyecto fue creado como parte de una práctica académica.
