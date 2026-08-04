# Muestras públicas — máquina de clientes

Repo de publicación de los mockups que Giancarlo le manda a los clientes.

- **Hosting:** GitHub Pages (repo `giancarlomartinogm-create/muestras`, rama `main`, raíz).
- **URL base:** https://giancarlomartinogm-create.github.io/muestras/
- **URL de una muestra:** `<URL base>/<id-del-prospecto>/`

## Cómo se publica

No se toca a mano. Lo hace la skill `maquina_clientes.py` de JARVIS:

    publicar_mockup(id)

que copia `~/Proyectos/Prospeccion/mockups/<id>/` a `publico/<id>/`, hace commit y push,
guarda la URL en `pipeline.json` (campo `url_publica`) y la muestra en el panel.

Por voz: «Hervis, publica el mockup de <negocio>».

## Reglas

- Todo lo que está acá es **público en internet**: solo muestras con datos de ejemplo.
- Republicar el mismo id **sobrescribe** la muestra anterior (el cliente ve la nueva al recargar).
- Para bajar una muestra: borrar la carpeta `publico/<id>/`, commit y push.
- `.nojekyll` evita que GitHub Pages procese los archivos: se sirven tal cual.
