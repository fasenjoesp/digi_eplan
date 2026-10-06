# Revisión del capítulo 1 y de la bibliografía

## Uso

Abra `main.tex` como documento principal y compile con pdfLaTeX, BibTeX y dos pasadas adicionales de pdfLaTeX, o con la compilación automática de su editor. Se mantiene la plantilla y el estilo de citas autor-año `apacite` del proyecto original.

Los archivos modificados son `Cap_1.tex`, `library.bib`, `main.tex` y `template_config.tex`. Los capítulos 2, 3 y 4 se conservan. El ZIP contiene los fuentes y recursos; se han omitido los archivos auxiliares de compilación y el PDF anterior para evitar confundirlo con una versión corregida.

## Correcciones a partir de las anotaciones

Las páginas indicadas corresponden al PDF anotado, contando la portada como página 1.

| Página | Observación del profesor | Corrección |
|---|---|---|
| 15 | Aclarar de qué puesta en marcha se habla e incluir un ejemplo tangible. | Se concreta el objetivo en máquinas e instalaciones industriales y se introduce una cinta transportadora con un sensor. Se distingue el dispositivo eléctrico, la variable de control y el elemento simulado. |
| 16 | La explicación de los porcentajes resulta confusa. | Se separan las tres bases de cálculo: duración del proyecto, puesta en marcha y sistemas eléctricos y de control. Se presenta el estudio VDW como una fuente histórica recogida por Wünsch. |
| 17 | ¿El ahorro compensa la creación del entorno virtual? | Se aclara, tras consultar la tesis de Wünsch, que el modelo se entregaba preparado a los participantes del experimento. Se diferencia el ahorro medido del coste total de modelado. |
| 18 | Explicaciones demasiado abstractas sobre arquitectura. | Se sustituyen por responsabilidades y ejemplos de cambios concretos: formato de exportación, acceso a EPLAN y reglas de clasificación. |
| 22 | Falta base para juzgar la elección de arquitectura. | Se justifica la separación de responsabilidades por los cambios y pruebas previstos, y la aplicación única por el flujo local planteado. Se presenta como propuesta, no como implantación ya comprobada. |
| 23 y 27 | Concordancia en «Microsoft indican». | Desaparecen esas formulaciones al sustituir el catálogo por la justificación del patrón elegido. |
| 24 | Expresión resaltada «de solo». | Se elimina junto con la descripción de un patrón ajeno al alcance del proyecto. |
| 25 | Términos extranjeros y «búfer». | Se suprime el catálogo donde aparecía el término marcado y se utilizan expresiones españolas; los términos extranjeros necesarios se introducen en cursiva. |
| 26 | No es necesario enumerar arquitecturas y patrones. | Se elimina la enumeración general y se explica únicamente la arquitectura propuesta y el procesamiento mediante canalizaciones y filtros. |
| 28 | No queda claro qué se obtiene de EPLAN ni para qué. | Se describen identificación completa, función, artículos, descripción, página y datos de señal disponibles, con su utilidad para clasificar y comparar sensores. La explicación de herramientas se adelanta a la arquitectura. |
| 28 | No combinar sangría y líneas vacías. | Se retiran los saltos forzados al final de los párrafos del capítulo y se mantiene la sangría sin espacio adicional entre párrafos. |
| 29 | Definición del PLC demasiado genérica. | Se define como dispositivo para controlar automatismos y se explica la relación entre entradas, programa y salidas. |
| 29 | Falta concreción en TIA Portal, variables y asociación con EPLAN. | Se define cada concepto y se usa el ejemplo ilustrativo de `PiezaDetectada`, tipo `Bool` y dirección `%I0.0`. No se presenta ese nombre como un dato real del proyecto. |
| 29 | Falta espacio antes de una cita. | Se corrige la separación entre texto y citas en la redacción revisada. |
| 30 | ¿Dónde se ejecuta el programa del PLC? | Se distingue el entorno de ingeniería, el controlador físico o simulado y el modelo de la instalación. Se añaden fuentes de F.EE y Siemens; no se da por confirmada una configuración concreta de EDAG. |
| 32 | Se usa PLC tag sin definición previa. | Se define antes de emplearlo y se utiliza preferentemente «variable del PLC». |
| 33 | ¿Cómo se almacena la información? ¿Podría hacerlo un agente de IA? | Se explica el CSV como resultado intermedio y la necesidad de adaptación posterior. Se justifica el uso de reglas explícitas y se presenta la IA como posible ampliación, sin inventar resultados comparativos. |
| 39 | Falta punto tras los paréntesis bibliográficos. | Se añade el punto después de las notas de `apacite` mediante un ajuste en `main.tex`, que se conserva al regenerar la bibliografía. |

## Bibliografía y alcance de la revisión

- Se conserva el estilo autor-año de la memoria; no se traslada el formato numérico del anteproyecto.
- Se conservan las fechas de consulta existentes y se normalizan las notas en español. Las nuevas fuentes consultadas llevan fecha 23 de septiembre de 2026.
- Se protegen las mayúsculas de los títulos, nombres propios y siglas mediante llaves en BibTeX.
- Se activa la visualización de las URL que la plantilla ocultaba, se completa el enlace de Visual Studio y se adapta la entrada de Beilby a `@misc`.
- Se mantienen en `library.bib` las referencias originales aunque algunas dejen de citarse al eliminar los catálogos y afirmaciones generales. BibTeX solo incluirá las citadas en la bibliografía final.
- Se retira del capítulo la cita de Marques sobre estaciones de servicio, que no justificaba directamente la afirmación general sobre la relación entre puesta en marcha virtual y gemelos digitales.
- Los porcentajes se atribuyen a Wünsch, que es la fuente consultada; VDW y Zäh se identifican como estudios recogidos por esa tesis.
- No se ha realizado una auditoría exhaustiva de todos los artículos del estado del arte. Se ha conservado su contenido esencial y se han revisado su redacción y conexión con el proyecto.

## Aspectos que se deberán concretar en la metodología

La conexión de las pruebas puede utilizar un controlador físico o uno simulado; la documentación recibida no permite fijar cuál se empleará. Tampoco se afirma que el CSV sea directamente importable por fe.screen-sim. La interfaz definitiva, los campos disponibles, los criterios de comparación y las operaciones de generación deben documentarse según la implementación y las pruebas reales.

Se conserva el foco del capítulo en sensores. Las menciones a actuadores explican el funcionamiento general del sistema o describen otros trabajos; no amplían por sí solas el alcance implementado del TFG.

## Comprobación realizada

Se ha compilado el capítulo revisado y procesado `library.bib` con BibTeX en una plantilla auxiliar, sin referencias indefinidas ni errores de sintaxis, y se han revisado visualmente sus páginas. Esta comprobación no equivale a compilar la plantilla original: el entorno de revisión no dispone de algunos paquetes que esta requiere, entre ellos `tracklang` y `apacite`. La maquetación completa y el ajuste de puntuación de `apacite` deben comprobarse al compilar `main.tex` en su entorno habitual. No se incluye un PDF auxiliar como si fuera el resultado final de la plantilla.
