# Evaluación Económico-Financiera — Aura Costello

**Flujo de caja, VAN, TIR, payback, punto de equilibrio y sensibilidad · Horizonte 10 años · Moneda CLP**

> Integración cuantitativa de los cuatro estudios previos (`03` mercado, `04` modelo/estrategia, `05` técnico, `06` legal). Toma sus supuestos, reconcilia las diferencias de precio y costo, y evalúa la rentabilidad del proyecto. **Todos los supuestos están declarados y el modelo es auditable.** Cifras en pesos chilenos (CLP) nominales.

**Versión:** 1.0 · **Fecha:** Julio 2026 · **Base:** RM–Santiago · **Escala:** inversión mayor con espacio físico propio

---

## 1. Parámetros y supuestos base

| Parámetro | Valor | Fuente / justificación |
|---|---|---|
| Horizonte de evaluación | 10 años | Definición del usuario |
| Moneda | CLP nominal | Definición del usuario |
| Inflación / reajuste anual | 3,5% | Aplica a precios, costos variables y OPEX fijo (mantiene márgenes reales) |
| Tasa de descuento base | **15%** | Emprendimiento turístico PyME de riesgo medio-alto en Chile, sin historia y con demanda cíclica. Sensibilidad a 12% y 20% |
| Régimen tributario | Pro-Pyme, **25%** | Supuesto; aplica sobre utilidad (EBITDA − depreciación). A validar con contador |
| CAPEX inicial (Año 0) | **$75.000.000** | Estudio técnico `05` |
| OPEX fijo mensual (Año 1) | **$13.712.500** | Estudio técnico `05`; crece 3,5%/año |

### 1.1 Reconciliación del ticket promedio (mercado vs. técnico)

Mercado (`03`) sugería un ticket ponderado ~$68–75k (mayor peso premium); el técnico (`05`) usó ~$48k. **Se resuelve construyendo el ticket desde los precios por línea del modelo (`04`) con un mix de volumen realista, dominado por productos de entrada (barrio, food tour) y una cola premium acotada:**

| Línea | Precio (CLP) | Costo variable directo | Margen contrib. | Peso en volumen |
|---|---:|---:|---:|---:|
| Inmersión de barrio | 28.000 | 11.000 | 61% | 28% |
| Food tour de mercado | 42.000 | 18.000 | 57% | 32% |
| Clase de cocina "mercado a la mesa" | 65.000 | 26.000 | 60% | 17% |
| Excursión Cajón del Maipo (día) | 85.000 | 48.000 | 44% | 9% |
| Ruta del vino (día) | 110.000 | 62.000 | 44% | 8% |
| Premium: maridaje privado | 170.000 | 70.000 | 59% | 6% |
| **Ponderado** | **58.980** | **26.740** | **54,7%** | **100%** |

> **Ticket bruto base usado: $58.980.** **Margen de contribución antes de comisiones de canal: 54,7%.** (Nota: el costo variable del técnico, ~$12.560/cliente, subestimaba el real porque excluía honorarios de guía/cocinero por salida y degustaciones/viñas; se usa el costo por línea del `04`, más completo.)

### 1.2 Otros supuestos operativos

- **Rampa de demanda (`03`):** 3.600 clientes Año 1 → 15.000 Año 5, luego +4–6%/año hasta 18.900 en Año 10. **Verificación de capacidad:** el régimen técnico es ~15.240 clientes/año (1.270/mes) y el máximo teórico ~26.400/año; los años 6–10 (15.900–18.900) se sostienen elevando la utilización con guías freelance (costo variable), **sin CAPEX adicional** y por debajo del techo teórico.
- **Comisiones de canal (`04`):** ponderadas 18% (Año 1) → 12% (régimen), a medida que crece la venta directa. Aplican sobre el ingreso por experiencias.
- **Ingreso complementario de retail** (productos curados en el espacio): 0% Año 1 → 7% del ingreso por experiencias en régimen; con costo de venta 55%.
- **Estacionalidad (`03`):** índice mensual 0,80 (invierno) – 1,25 (verano); no altera el total anual pero sí el equilibrio mensual. *Ajuste con dato duro:* la serie de turismo interno con destino RM (SERNATUR Big Data, 2024 completo) muestra un rango real **más plano, 0,88–1,18**, lo que **reduce el riesgo de meses valle** y mejora la utilización del espacio físico. El 0,80–1,25 se conserva como supuesto conservador.
- **Depreciación:** activos tecnología+marca ($15M) a 5 años; habilitación+cocina+mobiliario ($38M) a 10 años → $6,8M/año (Años 1–5) y $3,8M/año (Años 6–10). Capital de trabajo y garantías no se deprecian.

---

## 2. Flujo de caja proyectado (caso base, CLP)

| Año | Clientes | Ticket | Ingreso exper. | Margen contrib. | OPEX fijo | EBITDA | FCF neto | FCF acumulado |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 0 | — | — | — | — | — | — | **−75.000.000** | −75.000.000 |
| 1 | 3.600 | 58.980 | 212.328.000 | 77.844.960 | 164.550.000 | −86.705.040 | −86.705.040 | −161.705.040 |
| 2 | 7.200 | 61.044 | 439.518.960 | 173.885.117 | 170.309.250 | 3.575.867 | 3.575.867 | −158.129.173 |
| 3 | 10.200 | 63.181 | 644.444.675 | 267.203.502 | 176.270.074 | 90.933.428 | 69.900.071 | −88.229.102 |
| 4 | 12.600 | 65.392 | 823.941.471 | 361.814.102 | 182.439.526 | 179.374.576 | 136.230.932 | **48.001.830** |
| 5 | 15.000 | 67.681 | 1.015.213.599 | 460.527.258 | 188.824.910 | 271.702.349 | 205.476.762 | 253.478.591 |
| 6 | 15.900 | 70.050 | 1.113.790.839 | 510.256.514 | 195.433.782 | 314.822.732 | 237.067.049 | 490.545.640 |
| 7 | 16.700 | 72.501 | 1.210.774.702 | 554.687.341 | 202.273.964 | 352.413.377 | 265.260.033 | 755.805.673 |
| 8 | 17.500 | 75.039 | 1.313.183.041 | 601.603.261 | 209.353.553 | 392.249.708 | 295.137.281 | 1.050.942.954 |
| 9 | 18.200 | 77.665 | 1.413.510.225 | 647.565.750 | 216.680.927 | 430.884.823 | 324.113.617 | 1.375.056.571 |
| 10 | 18.900 | 80.384 | 1.519.251.663 | 696.008.649 | 224.264.759 | 471.743.890 | 354.757.917 | 1.729.814.489 |

*(Margen de contribución = ingreso total − comisiones de canal − costos variables − costo de retail. FCF = EBITDA − impuesto. El ingreso total incluye el retail complementario además del ingreso por experiencias mostrado.)*

---

## 3. Indicadores de rentabilidad (caso base)

| Indicador | Valor |
|---|---|
| **VAN (tasa 15%)** | **$556.834.006 CLP** |
| **TIR** | **51,3%** |
| **Payback (flujo acumulado)** | **3,6 años** |
| VAN @ 12% | $693.757.072 |
| VAN @ 20% | $386.127.516 |

> **El VAN es fuertemente positivo y la TIR (51,3%) supera con holgura la tasa de descuento (15%).** El proyecto crea valor incluso descontado al 20%. El resultado se apoya en la **alta escalabilidad**: los costos fijos crecen lento mientras el volumen y el ticket suben, y el margen de contribución (~55%) es elevado por el peso de experiencias de barrio/cocina de bajo costo variable.

---

## 4. Punto de equilibrio

En régimen (Año 5), con margen de contribución de **$30.702 por cliente** (después de comisiones y costos variables) y OPEX fijo anual de **$188.824.910**:

| Métrica | Valor |
|---|---|
| **Punto de equilibrio** | **≈ 6.150 clientes/año** |
| Equivalente mensual | **≈ 513 clientes/mes** |
| Ingreso de equilibrio | ≈ $416.256.829/año |

> El equilibrio (513 clientes/mes) se alcanza **entre el Año 2 y el Año 3** de la rampa y equivale a **~40% de la capacidad de régimen** (1.270/mes). Hay amplio colchón entre el punto de equilibrio y la capacidad instalada.

---

## 5. Análisis de sensibilidad y escenarios

Escenarios variando simultáneamente ticket, volumen, comisión y OPEX (tasa 15%):

| Escenario | Supuestos | VAN (CLP) | TIR | Payback |
|---|---|---:|---:|---:|
| **Pesimista** | Ticket −10%, clientes −20%, comisión +2 pp, OPEX +5% | **$80.947.197** | **20,8%** | 6,1 años |
| **Base** | Supuestos centrales | **$556.834.006** | **51,3%** | 3,6 años |
| **Optimista** | Ticket +8%, clientes +10%, comisión −2 pp, OPEX −2% | **$901.520.882** | **71,9%** | 2,8 años |

> **Robustez:** incluso en el escenario pesimista el **VAN sigue positivo y la TIR (20,8%) supera la tasa de descuento (15%)**. El proyecto resiste una caída conjunta de precio y volumen. La variable más sensible es el **volumen (rampa de demanda)**; el riesgo principal no es de rentabilidad sino de **liquidez en el arranque** (ver §6).

---

## 6. Necesidad de financiamiento (hallazgo crítico)

El CAPEX de $75M **no es la caja total requerida**. El flujo acumulado toca su punto más bajo al final del **Año 1 en −$161,7M** (CAPEX $75M + pérdida operativa del Año 1 $86,7M), y no vuelve a terreno positivo hasta el **Año 4**.

| Concepto | Monto |
|---|---:|
| CAPEX inicial | $75.000.000 |
| Pérdida operativa acumulada hasta el quiebre (rampa) | ~$87.000.000 |
| **Caja total a financiar (peak funding need)** | **≈ $162.000.000** |

> **Implicancia:** modelar la operación con la dotación completa (6 personas) y arriendo desde el Año 1, mientras solo se atienden 300 clientes/mes, exige financiar **~$162M**, no $75M. Dos caminos, no excluyentes:
> 1. **Levantar el capital completo (~$165–170M con colchón)**: capital propio + fondos + deuda. La rentabilidad lo justifica (VAN $557M).
> 2. **Escalonar el OPEX del Año 1** (equipo mínimo + guías freelance, contrataciones por hitos de demanda). Reduce fuertemente el peak funding y mejora el payback; es la vía recomendada para un arranque prudente dada la señal de moderación 2026.

---

## 7. Estructura de financiamiento sugerida

Sobre una necesidad de ~$165M (CAPEX + runway):

| Fuente | Monto estimado | Naturaleza |
|---|---:|---|
| **Capital propio (socios)** | $60–80M | Base; alinea incentivos y habilita fondos |
| **CORFO (Semilla Inicia/Expande)** | ~$20M | Cofinanciamiento no reembolsable (concursable) |
| **SERCOTEC (Capital Semilla/Abeja)** | ~$3,5M | Cofinanciamiento no reembolsable (concursable) |
| **Deuda bancaria / crédito CORFO** | $50–70M | Complemento; sujeto a garantías y flujo |

> Los fondos concursables (**$23,5M**) se modelan como **reducción del aporte de capital propio**, no como ingreso operacional. Con ellos, el aporte propio directo a CAPEX baja a **~$51,5M**. No están garantizados: el escenario base **no** depende de ganarlos (son un *upside* de estructura de capital).

---

## 8. Conclusión

> **El proyecto es rentable y viable a 10 años.** Con ticket base de $58.980 y captura modesta del mercado (SOM <6% del SAM), entrega **VAN de $557M CLP y TIR de 51,3%** al 15%, con payback de 3,6 años y equilibrio en ~513 clientes/mes (≈40% de la capacidad). La rentabilidad es **robusta**: resiste el escenario pesimista (VAN +$81M, TIR 20,8%).
>
> **El riesgo dominante no es de rentabilidad sino de liquidez de arranque:** se requiere financiar ~$162M (no solo el CAPEX de $75M) para atravesar la rampa del Año 1, o bien escalonar el OPEX inicial. Con una estructura de capital que combine aporte propio, fondos CORFO/SERCOTEC y deuda acotada, y con contrataciones por hitos de demanda, el proyecto tiene un perfil financiero atractivo y defendible.

---

## Supuestos y fuentes

- **Estudios internos:** `03-estudio-de-mercado.md` (volumen, ticket por segmento, estacionalidad), `04-modelo-de-negocio-y-estrategia.md` (precios y márgenes por línea, mix de canales/comisiones), `05-estudio-tecnico-y-operaciones.md` (CAPEX, OPEX, capacidad), `06-estudio-legal-organizacional-y-ambiental.md` (costos legales, fondos concursables).
- **Supuestos clave declarados:** inflación 3,5%; tasa de descuento 15% (sens. 12%/20%); impuesto Pro-Pyme 25%; ticket ponderado $58.980; margen de contribución 54,7%; comisión de canal 18%→12%; rampa de demanda de `03` topada a capacidad de `05`.
- **Limitaciones:** modelo determinístico anual; no incorpora estacionalidad intramensual en el flujo (sí en el equilibrio), ni IVA (débito/crédito neutro en el margen para un servicio afecto), ni variaciones de tipo de cambio que afecten el volumen de argentinos/brasileños. Todas las cifras son referenciales y deben refinarse con cotizaciones reales antes de comprometer inversión.
