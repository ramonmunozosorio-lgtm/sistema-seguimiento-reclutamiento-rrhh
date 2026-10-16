# 📊 Sistema de Seguimiento y Control Operativo de Reclutamiento (RR.HH.)

## 🎯 Descripción del Proyecto
Prototipo de solución operativa en **Microsoft Excel avanzado** diseñado para el control, seguimiento y auditoría de procesos de reclutamiento y selección de personal en consultoras de RR.HH. 

El sistema resuelve la pérdida de trazabilidad en la gestión de candidatos, previene alertas falsas mediante reglas de negocio automatizadas y ofrece un **Dashboard interactivo** para la toma de decisiones gerenciales.

---

## 🛠️ Arquitectura y Reglas de Negocio
El libro está estructurado en 5 módulos integrados sin macros (VBA), utilizando exclusivamente fórmulas nativas avanzadas y referencias estables:

1. **`PARAMETROS`**: Tablas de validación centralizadas y **Glosario Técnico** de etapas y semáforos.
2. **`VACANTES`**: Control de requerimientos activos, días de apertura y cantidad de candidatos asociados.
3. **`CANDIDATOS`**: Matriz operativa principal de seguimiento individual.
   - *Control Inteligente de Alertas (`Estado_Accion`)*: Compara fechas meta contra `HOY()`. Detecta vencimientos, tareas del día y pasa automáticamente a estado **`Cerrado`** cuando un candidato es contratado/descartado o cuando el contacto falla por datos erróneos o límite de intentos (Intento 3 - Final).
   - *Control de Citas*: Gestión explícita del estado de entrevistas (Pendiente, Confirmada, Realizada, Cancelada).
4. **`DASHBOARD`**: Panel visual gerencial con KPIs automáticos:
   - Candidatos Activos, Entrevistas Agendadas, Acciones Vencidas y Documentación Pendiente.
   - Análisis de fuentes: Identificación dinámica del **Portal de Empleo con mayor rendimiento (%)**.
   - Control preventivo de **Entrevistas Pasadas Sin Actualizar**.
5. **`PRUEBAS`**: Hoja de Protocolo de Aseguramiento de Calidad (**QA**) con 13 casos de prueba (CP-01 a CP-13) para validación de datos límite y reglas de control.

---

## 📋 Tecnologías y Estándares Aplicados
- **Formato Nativo**: Microsoft Excel (.xlsx) con tablas estructuradas y formato condicional.
- **Configuración Regional**: Español (Chile), separador de argumentos (`;`) y formato de fecha `DD/MM/AAAA`.
- **Seguridad y Privacidad**: Datos 100% sintéticos para demostración, adhiriendo a principios de minimización de datos.
