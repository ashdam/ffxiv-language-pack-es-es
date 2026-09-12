# Decisiones de topónimos

Traducir los componentes descriptivos de todos los topónimos, incluidos mapas e instancias.
Conservar los nombres propios opacos, como Doma o Sastasha; traducir «Castillo de Doma».

La región es «El Bosque del Velo Negro». Sus subáreas son «Bosque central», «Bosque del este»,
«Bosque del sur» y «Bosque del norte». La compañía de Gridania es la «Orden de las Dos Víboras».

`toponimos-decisiones.csv` contiene los nombres traducibles con uso `region`, `zone` o
`territory`. Escribir el texto elegido en `decision`, sea una propuesta o una alternativa propia.
Una celda vacía significa pendiente; ninguna propuesta equivale a una traducción aprobada.

Las decisiones y el glosario contienen texto sin marcas de formato. Aplicar las cursivas
y demás macros en cada entrada del corpus según su fuente inglesa.

CSV con separador `;` y UTF-8 con BOM para Excel. Filtrar `tipo` para revisar regiones, zonas
o territorios. `territory` también incluye instancias e interiores. `map` indica una referencia
desde `Map.PlaceName`, no una obligación de conservar el inglés.

El japonés literal es una referencia semántica, no una propuesta de nombre español.
«Inglés transcrito» identifica palabras inglesas escritas en katakana. Las variantes de las
filas agrupadas se separan con `/`; `gameKeys` conserva sus identificadores.

Coordinar las familias de nombres y revisar los homónimos por contexto antes de aplicar
una decisión a todas sus filas. `glosario_actual` muestra una referencia, no una aprobación.
Las protecciones motivadas por una interfaz inglesa deben revisarse al traducir esa interfaz.

Aplicar las decisiones a `Name` y `NameNoArticle` respetando su gramática, macros y hashes.
Los nombres del buscador de contenido se entregan en `ContentFinderCondition`, columnas 43 y 44;
traducir solo los que coincidan con PlaceName, sin ampliar a otras instancias ni variantes.
Revisar las menciones y los destinos literales; cerrar la entrega con CorpusValidator y CI,
sin clases de tests unitarios. Las comprobaciones visuales requieren reiniciar el cliente.
