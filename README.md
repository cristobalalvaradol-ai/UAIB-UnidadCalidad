# UAIB · Unidad de Calidad — Autorizaciones CEC y Dirección

Archivo en línea de los respaldos de autorización de la investigación observacional
institucional del **Hospital Las Higueras de Talcahuano** (Servicio de Salud Talcahuano),
a cargo de la **Unidad de Apoyo a la Investigación Biomédica (UAIB)**.

El sitio muestra, para cada uno de los **600 estudios** del consolidado 2013-2026, la imagen
de sus dos respaldos de autorización:

- **Pronunciamiento del CEC** (acta o protocolo de aprobación del comité) — 332 documentos
- **Autorización definitiva de la Dirección** (ORD del Hospital) — 274 documentos

En total **606 documentos** y **1.4 mil páginas**, en escala de grises a 105 dpi.

## Cómo está armado

| Archivo | Qué es |
|---|---|
| `index.html` | El sitio completo: filtros, indicadores, tabla de los 600 estudios y el visor de documentos. No depende de ninguna librería externa. |
| `img/a2013.json` … `img/a2026.json` | Un archivo por año con las páginas de los documentos de ese año, en JPEG base64. La página los descarga **solo cuando se abre un documento de ese año**, así la carga inicial es liviana. |
| `.nojekyll` | Evita que GitHub Pages procese el sitio con Jekyll. |

## Cómo se actualiza

El sitio se genera desde la carpeta de trabajo

```
C:\Users\calvarado\Desktop\MATERIAL TRABAJO\2. INVESTIGACIÓN CLÍNICA HLH\AUTORIZACIONES CEC Y DIRECCIÓN
```

cada vez que entran documentos nuevos. El procedimiento completo está en
`_CLAUDE\INSTRUCTIVO ACTUALIZACION CEC Y DIRECCION.md` de esa carpeta.

Una actualización toca `index.html` (que trae los datos del consolidado) y el archivo
`img/a<año>.json` del año que cambió. El resto queda igual.

## Alcance y límites

- Es un **índice de respaldos**, no el expediente completo: no incluye informes, cartas de
  envío al CEC, autorizaciones preliminares ni anexos del investigador.
- Los ensayos clínicos de industria farmacéutica **no** forman parte de esta base.
- Las imágenes son una representación de lectura; el documento original firmado vive en la
  carpeta del estudio.
