#Reglas de Versionado - ActiveHub
Para mantener la integridad del código y la documentación del proyecto, el equipo seguirá el modelo de trabajo GitFlow simplificado.

1. Estructura de Ramas (Branches)
* main: Rama principal. Solo contiene código estable, testeado y listo para las entregas oficiales. Prohibido hacer push directo aquí.
* develop: Rama de integración. Aquí se unen todas las funcionalidades nuevas antes de pasar a main.
* feature/nombre-tarea: Ramas temporales para el desarrollo de funciones específicas (ej: feature/registro-usuarios, feature/diseño-db). Se crean a partir de develop.

2. Flujo de Trabajo Diario
* Sincronizar: Antes de empezar, traer los últimos cambios: git pull origin develop.
* Crear Rama: Crear una rama para la tarea asignada: git checkout -b feature/mi-tarea.
* Trabajar y Guardar: Hacer commits frecuentes con mensajes claros: git commit -m "Agregado filtro por disciplina".
* Subir: Subir la rama al repositorio remoto: git push origin feature/mi-tarea.

3. Reglas de Oro para el "Filtro Cruzado"
* Pull Requests (PR): Para pasar código de una feature a develop, se debe abrir un Pull Request en GitHub.
* Revisión Obligatoria: Ningún PR puede ser aprobado por el mismo autor. Debe ser revisado y aprobado por al menos otro integrante (ej: Renzo revisa a Ramiro).
* Estado "For Correction": Si el revisor encuentra errores, el estado en Jira pasará a For Correction y el autor deberá corregir antes de intentar el merge nuevamente.

4. Formato de los Mensajes de Commit
Se recomienda seguir un formato descriptivo:
* feat: para nuevas funcionalidades.
* fix: para corrección de errores.
* docs: para cambios en la documentación.
