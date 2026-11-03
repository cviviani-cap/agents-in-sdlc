---
title: "Lección 12: Despliega el sitio con GitHub Pages"
description: "Utiliza la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar Space Quiz en producción."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Ofrece a Space Quiz un hogar público desplegándolo con GitHub Pages. Copilot puede preparar el flujo de trabajo y guiar el despliegue, pero tú eres responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- Pide a Copilot que configure un despliegue con GitHub Pages.
- Revisa el flujo de trabajo y la solicitud de incorporación de cambios antes de combinarla.
- Sigue el despliegue y comprueba el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero la gente aún necesita una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages permite acceder a él mediante una URL pública sin añadir un servidor ni una dependencia de ejecución.

## Pide a Copilot que despliegue el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Habilita GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo despliegue en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla localmente si aún no existe. Crea una solicitud de incorporación de cambios con estos cambios y combínala cuando se superen las comprobaciones obligatorias. Supervisa el despliegue hasta que finalice correctamente y, después, indica la URL final del sitio web publicado. Si no tienes permiso para habilitar Pages o combinar la solicitud, dime exactamente qué debo aprobar o hacer; no indiques que ha terminado correctamente hasta que el sitio esté publicado.
```

![Diagrama de tres etapas: una solicitud de incorporación de cambios de space-quiz combinada; una ejecución correcta de Deploy website en GitHub Actions con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y combine una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de despliegue y cualquier solicitud de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba el despliegue

1. Confirma que el README solo se ha añadido si el repositorio aún no tenía uno.
2. Revisa los cambios de la solicitud, incluidos los pasos de compilación y despliegue del flujo de trabajo.
3. Combina la solicitud únicamente después de que se superen las comprobaciones obligatorias.
4. Sigue la ejecución de despliegue de GitHub Actions hasta que finalice correctamente.
5. Abre la URL indicada y confirma que se carga Space Quiz.

Si el agente no puede habilitar Pages o combinar la solicitud, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que el despliegue se complete correctamente y el sitio esté disponible.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio publicado y has comprobado el despliegue sin depender del informe del agente. Continúa con la [Lección 13: Revisión y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
