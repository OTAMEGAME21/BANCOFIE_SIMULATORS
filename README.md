# Simuladores financieros Banco FIE – Prototipo académico

Sitio web demostrativo para practicar cálculos de plan de pagos y capacidad de pagos. Está inspirado en una paleta corporativa azul y magenta; **no es un producto oficial ni está afiliado a Banco FIE**.

## Cómo abrirlo

1. Descarga y descomprime el archivo ZIP.
2. Abre la carpeta `Simuladores_Banco_FIE`.
3. Abre `index.html` con Chrome, Edge o Firefox.
4. La página pública se muestra primero. Pulsa **Iniciar sesión** para acceder al área privada.

No requiere instalación ni servidor para la demostración local. Los gráficos usan Chart.js desde CDN; si no hay conexión a internet, los cálculos y tablas siguen funcionando, pero los gráficos pueden no cargarse.

## Acceso de demostración

- Usuario: `JhonatanChoqueFie1`
- Contraseña: `JACRFIE1`
- Nombre mostrado después del acceso: **Administrador**

La contraseña se valida en JavaScript, tal como se solicitó para este prototipo. Esto **no constituye autenticación segura**: cualquier persona con acceso al código fuente puede verla o modificar la validación. No usar para proteger información real, datos personales ni operaciones bancarias. La contraseña no se guarda en el almacenamiento local; solo puede recordarse el nombre de usuario si se marca la casilla correspondiente. La sesión termina al cerrar sesión o recargar la página.

## Estructura

### Área pública (sin iniciar sesión)
- Inicio con banner y mensajes promocionales ilustrativos.
- Información y educación financiera general.
- Secciones de productos y servicios.
- Botón de inicio de sesión.
- No muestra ni permite abrir los simuladores.

### Área privada (después del acceso)
- Panel del administrador.
- Simulador de plan de pagos, en una sección independiente.
- Simulador de capacidad de pagos, en otra sección independiente.
- Envío opcional de la cuota del plan al análisis de capacidad.
- Historial local de simulaciones.
- Parámetros de simulación configurables.
- Exportación de reportes Excel compatibles (.xls basados en HTML) y PDF mediante la opción de impresión del navegador (“Guardar como PDF”).

## Plan de pagos

Incluye amortización francesa, alemana, americana y balloon; tasa nominal anual; TRe adicional; frecuencia; fechas; cargos; abonos extraordinarios; seguro de desgravamen; seguro de cesantía y otros seguros. Los seguros se estiman con tasas por mil mensuales sobre la base seleccionada (saldo o principal) y la frecuencia elegida. Si la póliza real usa otra base, tasa anual, prima fija o días exactos, la fórmula debe ajustarse a sus condiciones.

El dictamen del plan informa si el cronograma generado es consistente (por ejemplo, saldo final liquidado); **no evalúa la solvencia del solicitante ni aprueba un crédito**.

## Capacidad de pagos

Funciona independientemente o puede recibir la primera cuota calculada en el simulador de plan. Considera ingresos, gastos, otras deudas, nueva cuota y un escenario conservador. Muestra margen mensual, relación cuota/ingresos, cuota máxima orientativa y un resultado preliminar: viable, observado o no viable.

Los porcentajes y límites son supuestos configurables de demostración, no políticas oficiales de Banco FIE. Una evaluación crediticia real exige documentación, validación de ingresos, consulta de obligaciones y políticas vigentes de la entidad.

## Datos y privacidad

- Los cálculos se ejecutan en el navegador.
- El historial y parámetros se guardan localmente en el navegador del dispositivo.
- No se envían los datos a un servidor.
- No introducir información financiera o personal real.

## Archivos

- `index.html`: páginas pública y privada, formularios y vistas.
- `css/styles.css`: diseño adaptable, paleta azul/magenta y estilos de impresión.
- `js/app.js`: autenticación demostrativa, cálculos, gráficos, historial y exportaciones.
- `assets/banco-fie-logo.svg`: recurso gráfico recreado para el prototipo; no se presenta como archivo oficial del banco.
- `PRUEBAS_MANUALES.md`: lista de pruebas recomendadas.
