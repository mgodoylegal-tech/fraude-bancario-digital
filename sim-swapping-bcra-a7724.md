# SIM Swapping y la Comunicación BCRA "A" 7724
## Qué deben hacer los bancos argentinos — y qué pasa cuando no lo hacen

**Área:** Fraude Bancario Digital · Responsabilidad de Entidades Financieras  
**Norma:** Comunicación BCRA "A" 7724 (vigente desde septiembre 2023)  
**Autor:** Matías Godoy — Abogado  
**Fecha:** Abril 2026

---

## ¿Qué es el SIM swapping?

El SIM swapping (o SIM hijacking) es una modalidad de fraude en la que el atacante logra que la operadora telefónica transfiera el número de teléfono de la víctima a una SIM card bajo su control.

El mecanismo es simple: el atacante llama a la operadora haciéndose pasar por el titular, invoca un motivo verosímil (robo del teléfono, reposición de SIM) y, si la verificación de identidad de la telco es deficiente, obtiene el número en minutos.

Una vez obtenido el número, el atacante puede recibir los SMS de autenticación (OTP) que los bancos envían como segundo factor. Con ese código, accede al homebanking y opera como si fuera el titular.

**El problema de fondo no es técnico — es de diseño.** Los bancos que usan SMS como único factor de autenticación para operaciones de alto valor construyeron su seguridad sobre un elemento que no controlan y que puede ser transferido mediante ingeniería social.

---

## La Comunicación BCRA "A" 7724 — qué exige a los bancos

La Comunicación "A" 7724, vigente desde el 6 de septiembre de 2023, establece los requisitos mínimos para la gestión y control de los riesgos de tecnología y seguridad de la información en todas las entidades financieras argentinas.

En materia de autenticación y canales electrónicos, la norma establece obligaciones concretas:

### Sobre el uso del SMS como factor de autenticación

El requisito **RCA085** (Sección 5.7.2.3) establece que la autenticación fuera de banda mediante SMS debe tener **uso restringido** y requiere la aplicación de **controles complementarios** ante los riesgos inherentes a ese canal.

Esto significa que el SMS no puede ser el único factor de autenticación para operaciones de alto valor. Es un requisito explícito, no una recomendación.

### Sobre las transferencias inmediatas

El escenario **ETR005** (Transferencias Inmediatas) tiene clasificación de **Criticidad 1** — el nivel más alto de exigencia normativa. Para este escenario, el requisito **RCA032** exige que antes de confirmar la operación, el banco aplique técnicas de autenticación complementarias para revalidar la identidad del usuario.

### Sobre la notificación al cliente

La Sección 11 establece que los bancos deben implementar mecanismos de comunicación alternativa para notificar al cliente ante:
- Cambios en factores de autenticación
- Alertas surgidas del monitoreo transaccional
- Operaciones sospechosas detectadas por el sistema

Estas notificaciones deben usar **canales previamente validados** — no el mismo canal que puede haber sido comprometido.

### Sobre la respuesta ante detección de fraude

El requisito **RMC004** establece tres modelos de acción ante operaciones sospechosas:

- **Modelo Preventivo:** actuar *antes* de confirmar la operación
- **Modelo Reactivo:** actuar *después* de la operación y comunicarse con el cliente
- **Modelo Asumido:** asumir la devolución ante el reclamo del cliente

El banco tiene la obligación de elegir uno de estos modelos e implementarlo. No actuar no es una opción válida.

### Sobre la conservación de registros

Los registros de auditoría (logs) deben conservarse por un plazo **no menor a 6 años** y deben contener, como mínimo: identificación unívoca, tipo de evento, fecha y hora, usuarios intervinientes, dispositivo y canal de origen.

---

## Los incumplimientos más frecuentes en casos de SIM swapping

Basado en el análisis de la norma, los incumplimientos más habituales que se verifican en casos de fraude por SIM swapping son:

| Código | Sección | Incumplimiento típico |
|--------|---------|----------------------|
| RCA085 | 5.7.2.3 | SMS como factor único sin controles complementarios |
| RCA032 | 11.7.2  | Sin revalidación de identidad en transferencias inmediatas |
| RMC004 | 11.7.4  | Detección de fraude sin activación de modelo preventivo |
| RMC005 | 11.7.4  | Sin notificación al cliente por canal alternativo |
| RMC011 | 11.7.4  | Monitoreo sin umbrales dinámicos basados en comportamiento |
| Sec. 10 | —      | Sin gestión del riesgo de la operadora como tercera parte |

---

## La responsabilidad del Directorio

La A 7724 establece que el Directorio de la entidad es el **responsable primario** de la gestión de la seguridad informática en los canales electrónicos. Esta responsabilidad es **indelegable** — aunque los procesos estén tercerizados, la responsabilidad jurídica permanece en la entidad.

Esto tiene una consecuencia práctica directa para el litigio: el banco no puede excusarse en la falla de la operadora telefónica. Si la autenticación dependía de un tercero (la telco), el banco tenía la obligación de gestionar ese riesgo de cadena de suministro (Sección 10 de la norma).

---

## Qué hacer si fuiste víctima de SIM swapping bancario

Si sufriste una transferencia no autorizada originada en un SIM swap, estos son los pasos clave:

**1. Denuncia policial inmediata**  
Documentá la fecha y hora. En algunos escenarios de la norma (créditos preaprobados), el plazo para reclamar es de 90 días desde el vencimiento de la primera cuota.

**2. Reclamo formal al banco**  
Por escrito, con fecha cierta. El banco tiene la obligación de responder y proveer canales de atención las 24 horas.

**3. Preservación de evidencia**  
Solicitá a la operadora el historial de cambios de SIM de tu número. Guardá todos los SMS, correos y notificaciones recibidas (o no recibidas) en el período del fraude.

**4. Solicitud de logs mediante pericial informática**  
En el proceso judicial, podés solicitar al juez que ordene al banco presentar los registros de autenticación, los scores del motor antifraude y los logs de notificaciones enviadas. El banco tiene obligación de conservarlos por 6 años.

**5. Marco legal aplicable**  
- Com. BCRA "A" 7724 — incumplimientos normativos específicos
- Ley 24.240 Art. 40 — responsabilidad objetiva del proveedor de servicios
- Código Civil y Comercial Arts. 1749 y ss. — responsabilidad por actividad riesgosa
- Ley 25.326 — protección de datos personales

---

## Conclusión

El SIM swapping no es una falla del usuario. Es el resultado predecible de un sistema de autenticación que el banco diseñó con el factor más débil disponible, sobre una cadena de proveedores que no gestionó, sin los protocolos de respuesta que la norma exige.

La Comunicación BCRA "A" 7724 establece estándares mínimos claros. Los bancos que no los implementaron no pueden presentarse como víctimas inocentes del fraude digital.

---

## Referencias normativas

- Comunicación BCRA "A" 7724 — [bcra.gob.ar](https://www.bcra.gob.ar/Pdfs/comytexord/A7724.pdf)
- Ley 24.240 — Defensa del Consumidor
- Ley 25.326 — Protección de Datos Personales
- Código Civil y Comercial de la Nación
- NIST Cybersecurity Framework — [nist.gov](https://www.nist.gov/cyberframework)

---

*Matías Godoy — Abogado*  
*Fraude Bancario Digital · Compliance en Ciberseguridad*  
*Ciudad Autónoma de Buenos Aires, Argentina*
