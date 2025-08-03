# Challenge-Telecom-X-an-lisis-de-evasi-n-de-clientes
Informe Final - Análisis de Evasión de Clientes (Churn) - Telecom X 🔹Introducción La empresa Telecom X se enfrenta a un elevado índice de evasión de clientes (churn), lo que impacta directamente en sus ingresos y sostenibilidad. El objetivo de este análisis es identificar patrones asociados a la cancelación del servicio por parte de los clientes, a partir de datos históricos, con el fin de proporcionar información útil para la toma de decisiones estratégicas orientadas a la retención.

🔹Limpieza y Tratamiento de Datos El dataset original fue obtenido desde una API en formato JSON y contenía información anidada sobre:

Datos del cliente (gender, SeniorCitizen, etc.)
Servicios contratados (InternetService, PhoneService, etc.)
Información de facturación (MonthlyCharges, TotalCharges)
🔹 Transformaciones realizadas:

Expansión de columnas anidadas y conversión a DataFrame plano.
Limpieza de registros vacíos y normalización de valores inconsistentes (No internet service → No).
Conversión de campos categóricos a binarios (Yes → 1, No → 0).
Creación de nueva variable: Cuentas_Diarias = MonthlyCharges / 30
Traducción de campos y valores para facilitar su comprensión.
🔹Resultado: un dataset limpio, sin valores nulos ni duplicados, con 7043 registros y 22 columnas.

🔹Análisis Exploratorio de Datos (EDA)

Distribución general de evasión 26.5% de los clientes han abandonado el servicio. Visualización de barras y torta muestran una evasión significativa.

Evasión por contrato: Los contratos mensuales concentran la mayoría de las cancelaciones. Contratos anuales y bienales presentan tasas muy bajas de churn.

Variables numéricas: Clientes que abandonan:

Tienen una permanencia promedio de ~18 meses vs 38 meses en los que se quedan.
Poseen mayor facturación mensual y diaria, lo que podría reflejar una percepción de alto costo.
Tienen una facturación total más baja, indicando que se van antes de generar ingresos significativos.
🔹 Visualizaciones clave:

Boxplots: Meses_Cliente, Facturacion_Mensual
Gráficos de barras: Contract, PaymentMethod, InternetService vs Se_Fue
Torta de distribución de churn
🔹Conclusiones e Insights El 26.5% de los clientes abandonan, un indicador crítico que necesita ser atendido con urgencia. Clientes nuevos (menores a 1 año) son los que más abandonan. Los clientes con tickets mensuales altos abandonan más, lo que indica una oportunidad de mejorar el valor percibido del servicio. Los contratos mensuales presentan una clara correlación con la evasión.

🔹Recomendaciones Estratégicas

Rediseñar contratos mensuales:
Ofrecer beneficios al migrar a contratos anuales/bienales.
Implementar promociones con permanencia mínima.
Segmentar e intervenir clientes de alto ticket: Detectar los que pagan más y ofrecer atención diferenciada. Aumentar el valor percibido con beneficios exclusivos.
Fortalecer onboarding para clientes nuevos: Los primeros 6 meses son críticos. Enviar encuestas, seguimiento personalizado y contacto preventivo.
