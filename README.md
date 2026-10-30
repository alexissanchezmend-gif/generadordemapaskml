# Mapas BK

Web para ver la hoja de ruta diaria por BK y viaje, agrupada por EDT, y descargar los mapas de cada ruta para el equipo de transporte.

## Uso diario

1. Abre la web y pulsa **Cargar hoja del día** (o arrastra el Excel a la página).
2. Revisa los totales: fecha, rutas, viajes, clientes coordenados y clientes alejados de su ruta.
3. En **Resumen por BK y viaje**, descarga por fila:
   - **KML**: un archivo `.kml` por BK y viaje, para Google Earth o Google My Maps.
   - **PNG**: imagen del recorrido con la lista de paradas.
4. Para bajar todo junto usa **Descargar todos (PNG + KML)** o el botón **ZIP** de cada EDT.

La hoja cargada se guarda solo en el navegador de cada persona (últimos 7 días). No hay datos de clientes dentro de este repositorio.

## Formato de la hoja de ruta

Excel (.xlsx, .xls) o CSV con encabezados en la primera fila. Se detectan solas estas columnas:

| Dato | Encabezado esperado |
|---|---|
| BK | Ruta |
| Latitud / Longitud | LATITUD, LONGITUD (si vienen intercambiadas se corrigen solas) |
| Código, Cliente, Dirección | Código, Cliente, Dirección |
| Vehículo, Viaje, Secuencia | Vehículo, Viaje, Sec |
| Distrito | SKU 1 |
| Km, Entrega, Llega, Sale, Fecha | Dist (Km), Entrega, Llega, Sale, Fecha |

Si alguna columna cambia de nombre, se puede elegir en **Columnas detectadas**.

## EDT por BK

Los rangos están en `index.html`, en la constante `EDTS`:

| EDT | BK |
|---|---|
| PACHECO | BK3501 – BK3550 |
| REINA | BK3561 – BK3569 |
| DABRIXO | BK3571 – BK3579 |
| BECOR | BK3580 – BK3581 |
| DSURIM | BK3582 – BK3585, BK3559 – BK3560 |

## Publicar en GitHub Pages

1. Sube `index.html` y este `README.md` a la raíz del repositorio.
2. Ve a **Settings → Pages**, elige la rama `main` y la carpeta `/ (root)`, y guarda.
3. La web queda en `https://USUARIO.github.io/NOMBRE-REPO/`.
