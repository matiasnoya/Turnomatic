# TURNOMATIC - Documento de Producto

**Versión:** 1.0  
**Fecha:** Octubre 2025

---

## 🎯 ¿QUÉ ES TURNOMATIC?

Sistema web para gestionar turnos de negocios de servicios (barberías, consultorios, salones de belleza, etc).

**Problemas que resuelve:**
- Turnos por WhatsApp son caóticos
- Doble booking de agendas
- Clientes que no se presentan
- Dueños sobrecargados gestionando todo

**Solución:**
- Agenda digital para cada trabajador
- Página web donde clientes reservan 24/7
- Recordatorios automáticos
- Panel de control para el dueño

---

## 👥 ROLES DE USUARIOS

### 1. Owner (Dueño)
**Lo que puede hacer:**
- Ver y editar todas las agendas
- Agregar/eliminar trabajadores
- Configurar servicios y precios
- Ver reportes del negocio
- Gestionar la suscripción

### 2. Worker (Trabajador)
**Lo que puede hacer:**
- Ver y editar SU agenda
- Configurar su disponibilidad
- Ver sus clientes
- Marcar turnos como completados

### 3. Client (Cliente)
**Lo que puede hacer:**
- Ver disponibilidad
- Reservar turnos
- Cancelar/reagendar (hasta 24hs antes)
- No necesita registrarse

---

## ⚙️ FUNCIONALIDADES PRINCIPALES

### PARA EL DUEÑO

**Dashboard Principal:**
- KPIs: Turnos hoy, Ingresos, Ocupación, No-shows
- Agenda visual con todos los trabajadores
- Próximos turnos
- Botón para crear nuevo turno

**Gestión de Trabajadores:**
- Lista de todo el equipo
- Agregar nuevo (envía invitación por email)
- Editar información
- Asignar servicios que puede realizar
- Ver su desempeño

**Gestión de Servicios:**
- Lista de servicios del negocio
- Crear nuevo servicio:
  - Nombre (ej: "Corte de pelo")
  - Duración (30 min)
  - Precio ($500)
  - Quién puede hacerlo
- Editar/eliminar servicios

**Clientes:**
- Base de datos de todos los clientes
- Historial de turnos de cada uno
- Estadísticas (frecuencia, total gastado)
- Identificar clientes VIP y en riesgo

**Reportes:**
- Ingresos por período
- Turnos completados/cancelados
- Ranking de servicios más pedidos
- Performance de cada trabajador
- Horarios con más demanda

**Configuración:**
- Datos del negocio (nombre, dirección, teléfono)
- Logo y fotos
- Horarios de atención
- Políticas de cancelación
- Método de pago para suscripción

---

### PARA EL TRABAJADOR

**Mi Agenda:**
- Ver solo mis turnos del día
- Timeline con horarios libres/ocupados
- Información del cliente en cada turno
- Botones: Completar, Cancelar, Editar

**Mi Disponibilidad:**
- Configurar mis horarios de trabajo
- Días que trabajo
- Breaks/descansos
- Días libres/vacaciones

**Mis Estadísticas:**
- Turnos esta semana/mes
- Historial de mis clientes
- Mi desempeño

---

### PARA EL CLIENTE (Página Pública)

**URL:** `turnomatic.uy/nombre-del-negocio`

**Lo que ve:**
- Información del negocio
- Lista de servicios con precios
- El equipo de profesionales
- Horarios de atención
- Ubicación en mapa
- Botón grande: "RESERVAR TURNO"

**Flujo de Reserva (5 pasos):**

1. **Elegir Servicio:**
   - Ve lista de servicios
   - Selecciona uno (ej: Corte de pelo - 30min - $500)

2. **Elegir Profesional:**
   - "Cualquiera disponible" o
   - Elegir específico (Juan, María, etc)

3. **Elegir Fecha:**
   - Calendario
   - Solo días disponibles

4. **Elegir Horario:**
   - Slots disponibles (09:00, 09:30, 10:00...)
   - Los ocupados aparecen bloqueados

5. **Datos del Cliente:**
   - Nombre
   - Teléfono
   - Email (opcional)
   - Notas especiales

**Confirmación:**
- Email con detalles del turno
- Link para cancelar/reagendar
- Botón "Agregar a calendario"

---

## 📧 NOTIFICACIONES AUTOMÁTICAS

### Email de Confirmación (inmediato)
Cuando el cliente reserva, recibe:
- Detalles del turno
- Profesional asignado
- Dirección del local
- Link para gestionar turno

### Recordatorio 24hs Antes
Envío automático:
- "Tu turno es mañana a las 15:00"
- Link para confirmar
- Link para cancelar si no puede

---

## 🛠️ STACK TECNOLÓGICO

### Frontend:
- **Framework:** Next.js (React)
- **Styling:** Tailwind CSS
- **State:** React Context / Zustand

### Backend:
- **Framework:** Spring Boot
- **Base de datos:** PostgreSQL
- **ORM:** JPA
- **Autenticación:** JWT

### Infraestructura:
- **Hosting:** Vercel (frontend) + Railway (backend)
- **Email:** Gmail
- **Storage:** AWS S3 (imágenes)

### Integraciones:
- Google Maps API
- Google Calendar API (futuro)
