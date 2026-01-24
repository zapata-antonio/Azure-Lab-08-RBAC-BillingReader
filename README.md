# Lab 08 — RBAC: Segregación de funciones con Billing Reader | Azure

## Contexto (por qué lo hice)
En entornos reales, perfiles como **finanzas** necesitan visibilidad de costes y facturación, pero no deberían poder crear recursos ni tener permisos administrativos.  
En este lab aplico **mínimo privilegio** usando **RBAC** a nivel de **suscripción**, validando que el usuario puede consultar facturación sin capacidad operativa técnica.

## Objetivo
Aplicar **segregación de funciones** y **mínimo privilegio** para un perfil no técnico:
- Permitir lectura de información de facturación
- Impedir creación/modificación de recursos
- Evitar privilegios administrativos fuera de Azure (Entra)

---

## Tareas realizadas
1. Asignación del rol **Billing Reader** a nivel de **suscripción** (IAM / Access control).
2. Validación práctica de restricciones: el usuario puede ver información de facturación, pero no ejecutar acciones técnicas.

---

## Evidencias

### 01) Asignación del rol en IAM (suscripción)
[<img src="images/01-iam-billing-reader.png" width="800">](images/01-iam-billing-reader.png)

### 02) Denegación de acción técnica (Access denied)
[<img src="images/02-access-denied.png" width="800">](images/02-access-denied.png)

---

## Checklist de verificación
- [x] Puede ver facturación (Billing)
- [x] No puede crear recursos
- [x] No puede administrar Microsoft Entra ID

---

## Qué explicaría en una entrevista / a un cliente
“Uso RBAC con roles específicos como **Billing Reader** para dar acceso a facturación sin conceder permisos excesivos tipo **Contributor**. Así aplico **mínimo privilegio** y mantengo segregación de funciones entre equipos técnicos y no técnicos.”
