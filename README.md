RetailPlus · Predicción de ventas: Regresión vs Random Forest 🛒📈
Comparo modelos de regresión para predecir Monto USD (o demanda) y ayudar en inventario, precios (elasticidad) y crédito.

🎯 Objetivo:
Quedarse con el modelo que mejor predice y generaliza:
Regresión (Lineal, Ridge, Lasso)
Random Forest Regressor
Métrica principal: MAPE. Apoyo: MAE, RMSE, R².

🧩 Problemas que resuelve:
Excesos y quiebres por mal pronóstico
Precios poco afinados

📦 Datos:
Target: Monto USD (o ventas_semana)
Numéricas: Cantidad, Flete, etc.
Categóricas: SECTOR_CLIENTE, RUBRO_CLIENTE, COD_MARCA, CENTRO_DESPACHO, REGION/PROVINCIA/DISTRITO/CIUDAD, CONDICION_PAGO, UNIDAD_MEDIDA
Tiempo: FECHA_FACTURA o semana
Limpieza mínima:
   Fechas bien tipadas
   Nulos bajos → imputación simple
   Filtrar valores negativos si no tienen sentido
   Outliers en Monto USD → IQR
   One-Hot a categóricas

🔧 Pipeline:
EDA breve (faltantes, outliers)
Split train/valid/test
Prepro: imputación + One-Hot (num/cat)
Modelos: Lineal, Ridge, Lasso, Random Forest
