# Trading Strategy — Adaptive Agent v1.0
# Este archivo es la fuente de verdad del agente.
# Se actualiza automáticamente cada semana.

## Filosofía
Superar al S&P 500 a largo plazo mediante una estrategia
adaptativa que evoluciona con evidencia empírica propia.
El agente comienza conservador y solo aumenta riesgo
cuando los datos de su propio historial lo justifican.

## Universo de activos permitidos
- Acciones del S&P 500 con capitalización >$10B
- ETFs de índice (SPY, QQQ, VTI)
- Sin criptomonedas, sin opciones, sin apalancamiento
- Sin penny stocks ni OTC

## Reglas de entrada
- Solo comprar cuando hay 2+ catalizadores confirmados
- Catalizadores válidos: earnings beat, upgrade analista,
  expansión de mercado, recompra de acciones, momentum >3M
- Nunca perseguir precio: si subió >5% en el día, esperar

## Reglas de salida
- Stop loss por posición: -7% desde precio de entrada
- Take profit parcial: vender 30% al llegar a +15%
- Trailing stop: 10% sobre máximo alcanzado (automático)
- Salida total si el catalizador original se invalida

## Gestión de riesgo (GUARDRAILS — NO MODIFICAR)
- Máximo 5% del portafolio por posición
- Stop loss global diario: si el portafolio cae -3% en un día,
  no abrir nuevas posiciones hasta el día siguiente
- Máximo 3 nuevas posiciones por semana
- Máximo 10 posiciones abiertas simultáneas
- Cash mínimo reservado: 20% del portafolio siempre

## Estado actual de la estrategia
- Versión: 1.0 — baseline conservador
- Semanas operando: 0
- Win rate histórico: N/A
- Alpha vs S&P 500 acumulado: N/A
- Última modificación: [AGENTE: actualizar fecha]

## Registro de ajustes a la estrategia
# El agente documenta aquí CADA modificación con justificación
# basada en datos reales de trade_log.md y weekly_review.md
# Ejemplo:
# 2025-01-15: Reducido stop loss de -10% a -7% porque el
# análisis de las últimas 8 semanas muestra que las
# posiciones que llegaron a -7% solo se recuperaron el 18%
# de las veces. Evidencia: trades T-045, T-046, T-052.
