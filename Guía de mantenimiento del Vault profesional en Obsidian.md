# Guía de mantenimiento del Vault profesional en Obsidian

## 1. Objetivo del sistema

Este vault está diseñado para servir como sistema central de conocimiento profesional, aprendizaje, investigación y producción documental.

El modelo combina cuatro enfoques:

- **PARA** para organizar trabajo y responsabilidades.
- **MOC — Maps of Content** para estructurar conocimiento.
- **Evergreen Notes** para conservar conocimiento reutilizable.
- **CODE** para gestionar el ciclo de vida de la información.

La arquitectura debe mantenerse simple. El objetivo no es almacenar el máximo número de notas, sino construir conocimiento reutilizable que permita:

- ejecutar proyectos;
- aprender de forma acumulativa;
- documentar decisiones;
- producir informes;
- preparar investigaciones;
- desarrollar publicaciones;
- recuperar información rápidamente;
- relacionar conocimientos entre dominios.

---

# 2. Principios fundamentales

## 2.1. Las carpetas representan función, no conocimiento

Las carpetas indican **para qué sirve una nota dentro del sistema**.

No deben utilizarse para crear taxonomías temáticas profundas.

Correcto:

```text
02 Projects
03 Areas
04 Knowledge
05 Sources
06 Outputs
```

Incorrecto:

```text
Tecnología
    Sistemas
        Linux
            Docker
                Redes
```

El conocimiento se estructura mediante:

- enlaces;
- propiedades;
- etiquetas;
- Maps of Content.

---

## 2.2. Cada nota debe tener una razón para existir

Antes de conservar una nota debe poder responderse:

> ¿Qué utilidad futura tiene esta información?

Una nota debe cumplir al menos una de estas funciones:

- apoyar un proyecto;
- documentar una decisión;
- conservar conocimiento;
- registrar una fuente;
- desarrollar una idea;
- producir un entregable;
- servir como referencia futura.

Si no cumple ninguna, probablemente no debe incorporarse al vault.

---

## 2.3. Capturar no significa conservar

La información recién capturada es provisional.

Todo elemento nuevo entra inicialmente en:

```text
01 Inbox
```

Después debe decidirse qué hacer con él.

El Inbox no es almacenamiento permanente.

---

# 3. Arquitectura del Vault

```text
00 System
01 Inbox
02 Projects
03 Areas
04 Knowledge
05 Sources
06 Outputs
07 Archive
```

---

# 4. Función de cada carpeta

## 00 System

Contiene la infraestructura del vault.

Ejemplos:

```text
00 System/
├── Templates/
├── MOCs/
├── Dashboards/
├── Attachments/
├── Queries/
└── Documentation/
```

Aquí debe almacenarse:

- esta guía;
- plantillas;
- convenciones;
- documentación del sistema;
- consultas Dataview;
- dashboards;
- configuraciones metodológicas.

No debe contener conocimiento profesional.

---

# 5. Inbox

```text
01 Inbox
```

Es el punto único de entrada.

Puede contener:

- ideas rápidas;
- notas de reuniones;
- enlaces;
- documentos;
- fragmentos;
- referencias;
- capturas;
- notas procedentes de IA;
- información pendiente de clasificar.

## Regla

Ningún elemento debería permanecer indefinidamente en Inbox.

Durante la revisión deberá convertirse en:

```text
Project
Area
Knowledge
Source
Output
Archive
Delete
```

---

# 6. Projects

```text
02 Projects
```

Un proyecto es un esfuerzo con:

- objetivo definido;
- resultado esperado;
- principio y final.

Ejemplos:

```text
TFG NIS2
Migración Business Central
Implantar sistema IA local
Preparar artículo científico
Auditar arquitectura de red
```

Cada proyecto debería disponer de una nota principal.

Ejemplo:

```markdown
# Proyecto — TFG NIS2

## Objetivo

## Estado

## Próximas acciones

## Decisiones

## Recursos

## Conocimiento relacionado

## Entregables

## Riesgos

## Registro
```

---

# 7. Areas

```text
03 Areas
```

Una Area representa una responsabilidad permanente.

No tiene fecha final.

Ejemplos:

```text
Ciberseguridad
Gestión de proyectos
Investigación
Formación
Infraestructura
Carrera profesional
```

Regla práctica:

> Si tiene un resultado final, es Project.  
> Si debe mantenerse indefinidamente, es Area.

---

# 8. Knowledge

```text
04 Knowledge
```

Contiene conocimiento reutilizable.

Es el núcleo intelectual del vault.

Ejemplos:

```text
Qué es Zero Trust
NIS2 introduce responsabilidad de la dirección
Diferencia entre RTO y RPO
CAP theorem obliga a aceptar compromisos
PostgreSQL utiliza MVCC para controlar concurrencia
```

No debe estructurarse mediante una jerarquía profunda de carpetas.

El conocimiento se organiza principalmente mediante:

```text
MOCs
+
enlaces
+
propiedades
```

---

# 9. Sources

```text
05 Sources
```

Contiene notas asociadas a fuentes externas.

Ejemplos:

- libros;
- artículos científicos;
- normas;
- legislación;
- documentación técnica;
- cursos;
- vídeos;
- podcasts;
- informes;
- páginas web.

Una nota de fuente resume **lo que dice otra persona**.

Una nota Evergreen expresa **lo que consideramos conocimiento integrado**.

Esta distinción debe mantenerse.

---

# 10. Outputs

```text
06 Outputs
```

Contiene conocimiento producido.

Ejemplos:

```text
Informes
Artículos
Presentaciones
Procedimientos
Guías
Publicaciones
Documentación técnica
Material docente
```

Representa la última fase de CODE:

```text
Express
```

---

# 11. Archive

```text
07 Archive
```

Contiene elementos que ya no están activos.

Principalmente:

- proyectos finalizados;
- áreas abandonadas;
- documentación obsoleta;
- outputs antiguos.

Archivar no significa eliminar.

Permite mantener limpia la estructura activa sin perder trazabilidad.

---

# 12. Ciclo de vida de la información

Todo conocimiento debe recorrer aproximadamente este proceso:

```text
CAPTURE
   ↓
Inbox
   ↓
ORGANIZE
   ↓
Source / Project / Area
   ↓
DISTILL
   ↓
Knowledge
   ↓
CONNECT
   ↓
MOCs + Links
   ↓
EXPRESS
   ↓
Outputs
```

---

# 13. Flujo operativo CODE

## Capture

Capturar únicamente información potencialmente útil.

No intentar organizar durante la captura.

Destino:

```text
01 Inbox
```

---

## Organize

Preguntar:

> ¿Dónde será útil esto?

En lugar de:

> ¿De qué tema trata?

Ejemplo:

Una referencia sobre NIS2 utilizada en el TFG puede estar físicamente en:

```text
05 Sources
```

aunque esté relacionada con:

```text
[[MOC NIS2]]
[[MOC Ciberseguridad]]
[[Proyecto TFG]]
```

---

## Distill

Reducir la información a sus ideas fundamentales.

Evitar guardar grandes cantidades de texto sin procesar.

Proceso recomendado:

```text
Fuente
↓
Resumen
↓
Ideas importantes
↓
Notas Evergreen
```

---

## Express

El conocimiento debe utilizarse.

Ejemplos:

```text
Notas
↓
Informe

Notas
↓
Artículo

Notas
↓
Presentación

Notas
↓
Decisión

Notas
↓
Proyecto
```

Un vault que solo captura y organiza termina convirtiéndose en un archivo pasivo.

---

# 14. Tipos de notas

El sistema utilizará principalmente:

```text
Project Note
Area Note
Source Note
Evergreen Note
MOC
Meeting Note
Decision Note
Output
```

---

# 15. Evergreen Notes

Una Evergreen Note representa una idea reutilizable.

Debe cumplir cuatro principios.

## Atomicidad

Una nota debe contener preferentemente una idea central.

---

## Autonomía

Debe poder comprenderse sin necesidad de leer otras notas.

---

## Conectividad

Debe relacionarse con otras ideas.

---

## Evolución

Puede revisarse y mejorar con el tiempo.

---

# 16. Convención para títulos Evergreen

Evitar títulos genéricos.

Incorrecto:

```text
Zero Trust
NIS2
Gobierno del dato
Docker
```

Preferible:

```text
Zero Trust elimina la confianza implícita basada en ubicación de red

NIS2 introduce responsabilidad directa de los órganos de dirección

El gobierno del dato define responsabilidades sobre los activos de información

Los contenedores Docker comparten el kernel del sistema anfitrión
```

El título debería expresar una afirmación cuando sea posible.

---

# 17. Plantilla Evergreen

```markdown
---
type: knowledge
status: evergreen
created:
updated:
moc:
---

# Título declarativo de la idea

## Idea

Explicación de la idea con palabras propias.

## Implicaciones

Consecuencias prácticas o conceptuales.

## Evidencia

Fuentes que respaldan la afirmación.

## Relacionado

- [[Nota relacionada]]
- [[Nota relacionada]]

## Aplicación

Contextos profesionales, académicos o proyectos donde puede utilizarse.
```

---

# 18. Source Notes

Una Source Note representa una fuente concreta.

Ejemplo:

```markdown
---
type: source
source_type: article
author:
year:
url:
doi:
status: processed
---

# Título de la fuente

## Referencia

## Resumen

## Ideas principales

## Evidencias relevantes

## Limitaciones

## Notas derivadas

- [[Evergreen Note]]
- [[Evergreen Note]]
```

---

# 19. Regla Source → Knowledge

No copiar automáticamente información de una fuente a Knowledge.

Primero debe interpretarse.

Proceso:

```text
SOURCE

"La NIS2 establece..."

↓

INTERPRETACIÓN

La directiva incrementa la responsabilidad de los órganos de dirección.

↓

KNOWLEDGE

[[NIS2 convierte la ciberseguridad en una responsabilidad de gobierno corporativo]]
```

---

# 20. Maps of Content

Los MOC son mapas conceptuales.

No son carpetas.

Ejemplo:

```markdown
# MOC — Ciberseguridad

## Fundamentos

- [[Confidencialidad integridad y disponibilidad forman la tríada CIA]]
- [[Zero Trust elimina la confianza implícita]]

## Gobierno

- [[NIS2 introduce responsabilidad de la dirección]]
- [[ISO 27001 requiere liderazgo de la alta dirección]]

## Riesgos

- [[El riesgo combina probabilidad e impacto]]

## Arquitectura

- [[La segmentación reduce movimiento lateral]]

## Investigación

- [[MOC NIS2]]
- [[MOC Seguridad Internacional]]
```

---

# 21. Cuándo crear un MOC

No crear MOCs preventivamente.

Crear uno cuando existan aproximadamente:

```text
5–10 notas relacionadas
```

y resulte útil disponer de navegación estructurada.

Un MOC emerge del conocimiento existente.

No debería construirse una taxonomía completa antes de disponer del conocimiento.

---

# 22. Jerarquía de MOCs

Puede existir navegación multinivel.

Ejemplo:

```text
Home

↓
MOC Tecnología

↓
MOC Ciberseguridad

↓
MOC NIS2
```

Una misma nota puede pertenecer a varios MOCs.

Ejemplo:

```markdown
## MOCs

- [[MOC NIS2]]
- [[MOC Gestión de riesgos]]
- [[MOC Gobierno corporativo]]
```

---

# 23. Política de enlaces

Crear un enlace cuando exista una relación conceptual significativa.

No enlazar palabras indiscriminadamente.

Un buen enlace responde a alguna relación:

```text
A explica B
A contradice B
A amplía B
A depende de B
A es ejemplo de B
A aplica B
A proporciona evidencia sobre B
```

---

# 24. Backlinks

Los backlinks deben utilizarse como herramienta de descubrimiento.

Durante la revisión de una nota comprobar:

```text
Linked mentions
Unlinked mentions
```

Preguntar:

> ¿Qué otras notas explican o dependen de esta idea?

---

# 25. Tags

Las etiquetas no deben utilizarse como taxonomía temática principal.

Evitar:

```text
#ciberseguridad
#redes
#docker
#linux
#servidores
```

Los temas se gestionan mediante MOCs y enlaces.

Utilizar etiquetas principalmente para estados o procesos.

Ejemplo:

```text
#status/draft
#status/review
#status/evergreen

#priority/high

#action/research
#action/review
```

---

# 26. Propiedades

Las propiedades permiten estructurar metadatos.

Campos recomendados:

```yaml
---
type:
status:
created:
updated:
project:
area:
moc:
source:
---
```

No añadir propiedades que no tengan una utilidad clara.

---

# 27. Estados de conocimiento

Las notas pueden evolucionar.

```text
seed
↓
developing
↓
evergreen
```

### Seed

Idea inicial.

### Developing

Idea desarrollada pero incompleta.

### Evergreen

Conocimiento suficientemente sólido y reutilizable.

Ejemplo:

```yaml
status: developing
```

---

# 28. Gestión de proyectos

Cada proyecto debe disponer de una nota central.

```markdown
# Proyecto — Nombre

## Resultado esperado

## Estado actual

## Próximas acciones

- [ ]

## Decisiones

## Riesgos

## Recursos

## Conocimiento

## Entregables

## Registro de actividad
```

---

# 29. Separar conocimiento de proyecto

No almacenar conocimiento permanente dentro de proyectos.

Ejemplo:

Durante un proyecto Docker descubres:

> Los contenedores comparten el kernel del host.

Debe convertirse en:

```text
04 Knowledge
```

y enlazarse desde el proyecto.

Así el conocimiento seguirá disponible cuando el proyecto termine.

---

# 30. Decision Notes

Las decisiones importantes deben documentarse.

Plantilla:

```markdown
# DEC — Título

## Contexto

## Decisión

## Alternativas consideradas

## Razones

## Riesgos

## Consecuencias

## Fecha

## Relacionado
```

Esto es particularmente útil para:

- arquitectura;
- proyectos tecnológicos;
- investigación;
- metodología;
- infraestructura.

---

# 31. Registro de reuniones

Las reuniones no deben mezclarse con conocimiento permanente.

Plantilla:

```markdown
# Reunión — YYYY-MM-DD — Tema

## Participantes

## Objetivo

## Notas

## Decisiones

## Acciones

- [ ] Acción — responsable — fecha

## Conocimiento derivado

- [[Nota]]
```

---

# 32. Política de IA

La IA puede utilizarse para:

- resumir;
- clasificar;
- detectar conceptos;
- generar borradores;
- comparar fuentes;
- sugerir relaciones;
- transformar documentos en Markdown.

Pero el contenido generado por IA no debe convertirse automáticamente en conocimiento validado.

Proceso:

```text
IA
↓
Inbox
↓
Revisión humana
↓
Fuente / Knowledge / Output
```

---

# 33. Fiabilidad del conocimiento

Cuando sea relevante, distinguir:

```text
Hecho
Hipótesis
Interpretación
Opinión
Estimación
```

Puede utilizarse una propiedad:

```yaml
confidence: high
```

o:

```yaml
confidence: medium
```

Especialmente importante en investigación.

---

# 34. Política de fuentes

Para conocimiento importante intentar conservar siempre trazabilidad.

Prioridad:

```text
1. Fuente primaria
2. Documentación oficial
3. Investigación académica
4. Fuente secundaria especializada
5. Fuente divulgativa
```

Las afirmaciones relevantes deberían poder rastrearse hasta su origen.

---

# 35. Rutina diaria

La rutina diaria debe ser mínima.

## Durante el día

Capturar en:

```text
01 Inbox
```

No perder tiempo clasificando.

## Final del día

Cuando resulte necesario:

```text
Procesar Inbox
Actualizar proyectos activos
Registrar decisiones importantes
```

Objetivo:

```text
5–10 minutos
```

---

# 36. Revisión semanal

La revisión semanal es el principal mecanismo de mantenimiento.

Debe comprobarse:

## Inbox

```text
¿Hay elementos pendientes?
```

## Projects

```text
¿Qué proyectos están activos?
¿Qué proyecto está bloqueado?
¿Cuál es la próxima acción?
```

## Knowledge

```text
¿Qué conocimiento nuevo merece consolidarse?
```

## MOCs

```text
¿Ha surgido algún grupo de notas que necesite MOC?
```

## Sources

```text
¿Hay fuentes capturadas pero no procesadas?
```

## Outputs

```text
¿Qué conocimiento puede convertirse en un resultado?
```

Tiempo aproximado recomendado:

```text
20–40 minutos
```

---

# 37. Revisión mensual

Una vez al mes revisar la arquitectura.

## Comprobar

```text
Proyectos abandonados
Proyectos finalizados
Notas huérfanas
MOCs excesivamente grandes
Fuentes sin procesar
Notas duplicadas
Conocimiento desactualizado
```

---

# 38. Revisión trimestral

La revisión trimestral debe ser estratégica.

Preguntar:

```text
¿Qué áreas profesionales están creciendo?

¿Qué conocimientos estoy desarrollando?

¿Qué temas merecen investigación adicional?

¿Qué proyectos generan mayor aprendizaje?

¿Qué partes del vault no utilizo?

¿Qué procesos generan fricción?
```

Eliminar complejidad innecesaria.

---

# 39. Criterios para archivar

Archivar cuando:

- un proyecto haya terminado;
- una responsabilidad deje de existir;
- un documento haya sido sustituido;
- una nota haya quedado obsoleta pero tenga valor histórico.

Destino:

```text
07 Archive
```

---

# 40. Criterios para eliminar

Eliminar cuando:

- existe duplicación sin valor;
- la información carece de utilidad;
- la fuente no es fiable;
- el contenido puede recuperarse fácilmente y no aporta contexto;
- la nota nunca fue procesada y ya no resulta relevante.

El vault no debe convertirse en un almacén indiscriminado.

---

# 41. Notas huérfanas

Una nota sin enlaces puede indicar conocimiento aislado.

Durante revisiones comprobar notas que:

```text
no enlazan a ningún MOC
no reciben backlinks
no pertenecen a ningún proyecto
```

No es necesario que todas estén conectadas, pero deben revisarse.

---

# 42. Evitar sobreorganización

No crear:

- cientos de tags;
- decenas de propiedades;
- estructuras de cinco niveles;
- MOCs vacíos;
- carpetas para cada tema;
- plantillas excesivamente complejas.

Principio:

> La estructura debe aparecer cuando resuelve un problema real.

---

# 43. Regla de los 30 segundos

Debe ser posible decidir dónde colocar una nota en menos de 30 segundos.

Si no es posible, probablemente la arquitectura es demasiado compleja.

---

# 44. Regla de búsqueda antes de crear

Antes de crear una nota nueva:

```text
1. Buscar el concepto.
2. Revisar notas existentes.
3. Ampliar una existente si corresponde.
4. Crear una nueva solo si representa una idea distinta.
```

Esto reduce duplicados.

---

# 45. Regla de mínima estructura

No añadir una nueva:

```text
carpeta
tag
propiedad
tipo de nota
plugin
```

hasta que exista un problema concreto que lo justifique.

---

# 46. Dashboard principal

Crear:

```text
00 System/Home.md
```

Ejemplo:

```markdown
# Home

## Trabajo activo

- [[Proyecto A]]
- [[Proyecto B]]

## Areas

- [[MOC Ciberseguridad]]
- [[MOC Gestión de proyectos]]
- [[MOC Investigación]]

## Conocimiento

- [[MOC Tecnología]]
- [[MOC Seguridad]]
- [[MOC IA]]

## Pendientes

- [[Inbox]]

## Outputs

- [[Outputs]]
```

---

# 47. Métricas útiles

No medir el éxito por número de notas.

Las métricas relevantes son:

```text
Conocimiento reutilizado
Outputs producidos
Decisiones documentadas
Fuentes procesadas
Ideas conectadas
Tiempo necesario para recuperar información
```

---

# 48. Señales de que el sistema está fallando

## Inbox creciendo continuamente

Problema:

```text
captura > procesamiento
```

Solución:

Reducir capturas y aumentar revisión.

---

## Demasiadas carpetas

Problema:

Se está usando clasificación jerárquica para representar conocimiento.

Solución:

Migrar temas hacia MOCs.

---

## Miles de notas sin enlaces

Problema:

El vault funciona como archivo, no como sistema de conocimiento.

---

## Demasiadas etiquetas

Problema:

Se está intentando recrear una taxonomía rígida.

---

## Nunca se generan Outputs

Problema:

El sistema captura conocimiento pero no lo utiliza.

---

# 49. Protocolo para incorporar documentos externos

Cuando se incorpore un documento:

```text
Documento
↓
Source Note
↓
Resumen
↓
Ideas
↓
Evergreen Notes
↓
MOC
↓
Proyecto / Output
```

Nunca convertir automáticamente un documento completo en múltiples notas sin evaluar su valor.

---

# 50. Protocolo para convertir documentos a Markdown

## Paso 1

Preservar:

```text
Título
Autor
Fecha
Fuente
URL
Contexto
```

## Paso 2

Eliminar:

```text
navegación
publicidad
elementos visuales irrelevantes
duplicaciones
```

## Paso 3

Mantener estructura semántica:

```markdown
# H1

## H2

### H3
```

## Paso 4

Crear Source Note.

## Paso 5

Extraer conocimiento únicamente cuando tenga valor independiente.

---

# 51. Convención básica de nombres

## Proyectos

```text
Proyecto — Nombre
```

## MOCs

```text
MOC — Tema
```

## Reuniones

```text
YYYY-MM-DD — Reunión — Tema
```

## Decisiones

```text
DEC — Decisión
```

## Fuentes

Mantener título original siempre que sea razonable.

## Knowledge

Utilizar títulos declarativos.

---

# 52. Política de evolución del sistema

La arquitectura del vault no debe considerarse definitiva.

Cada cambio deberá responder a:

```text
Problema observado
↓
Hipótesis de mejora
↓
Cambio mínimo
↓
Uso durante varias semanas
↓
Evaluación
```

Evitar rediseños completos frecuentes.

---

# 53. Reglas maestras

## Regla 1

Las carpetas representan función.

## Regla 2

Los enlaces representan relaciones.

## Regla 3

Los MOCs representan estructura conceptual.

## Regla 4

Las fuentes representan evidencia.

## Regla 5

Las Evergreen Notes representan conocimiento.

## Regla 6

Los Projects representan ejecución.

## Regla 7

Los Outputs representan resultados.

## Regla 8

Inbox representa incertidumbre temporal.

## Regla 9

Archive representa conocimiento inactivo.

## Regla 10

La simplicidad tiene prioridad sobre la sofisticación.

---

# 54. Algoritmo rápido para cada nueva nota

Cuando aparezca nueva información:

```text
¿Es temporal?
        │
       Sí
        ↓
      Inbox
        │
        ↓
¿Está asociada a un objetivo con final?
        │
       Sí
        ↓
     Project
        │
       No
        ↓
¿Es responsabilidad permanente?
        │
       Sí
        ↓
      Area
        │
       No
        ↓
¿Proviene de otra fuente?
        │
       Sí
        ↓
     Source
        │
       No
        ↓
¿Es conocimiento reutilizable?
        │
       Sí
        ↓
    Knowledge
        │
       No
        ↓
¿Es un producto terminado?
        │
       Sí
        ↓
     Output
```

---

# 55. Ciclo completo del Vault

```text
                        CAPTURE
                           │
                           ▼
                        INBOX
                           │
                           ▼
                       ORGANIZE
                           │
          ┌────────────────┼────────────────┐
          ▼                ▼                ▼
       PROJECTS           AREAS           SOURCES
          │                │                │
          └────────────────┼────────────────┘
                           ▼
                        DISTILL
                           │
                           ▼
                       KNOWLEDGE
                           │
                     ┌─────┴─────┐
                     ▼           ▼
                   LINKS        MOCs
                     │           │
                     └─────┬─────┘
                           ▼
                        EXPRESS
                           │
                           ▼
                        OUTPUTS
                           │
                           ▼
                        ARCHIVE
```

---

# 56. Criterio final

El vault está funcionando correctamente cuando permite responder rápidamente:

```text
¿Qué estoy haciendo?

¿Qué sé?

¿Por qué creo que lo sé?

¿Dónde está la evidencia?

¿Qué decisiones he tomado?

¿Qué puedo reutilizar?

¿Qué debería producir a partir de este conocimiento?
```

Si el sistema responde a estas preguntas sin requerir demasiado mantenimiento, debe conservarse.

Si necesita más trabajo para organizarlo que el valor que devuelve, debe simplificarse.

---

# 57. Norma de gobierno del Vault

Esta guía constituye la norma base del sistema.

Cualquier modificación estructural importante deberá documentarse en:

```text
00 System/Documentation
```

registrando:

```markdown
## Cambio

## Problema que resuelve

## Fecha

## Impacto

## Resultado esperado
```

El objetivo es evitar que el vault evolucione mediante cambios improvisados y termine perdiendo coherencia.

---

# Versión

```text
Modelo: PARA + MOC + Evergreen + CODE
Versión: 1.0
Estado: Baseline
```