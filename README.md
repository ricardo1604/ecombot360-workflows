# EcomBot360 — Workflows

Proyecto Final Integrador — Diplomado IA UFG 2026

## Mapa de workflows

| Archivo | Workflow | Descripción |
|---------|----------|-------------|
| 1.3b0RWipPoqFrMyxA.json  | Orquestador Central | Telegram trigger → Normalizar → Clasificar IA → Switch |
| 2.Z4w95pjkm4toetiJ.json  | WF1 Chatbot IA | AI Agent + GPT-4o-mini + Qdrant RAG + Postgres Memory |
| 3.LVsPKkR4OV8x5fDg.json  | WF2 Lead Nurturing | Scoring IA → secuencia Wait → CRM Google Sheets |
| 4.YgQ2r6OSsQwAJQIn.json  | WF3 OCR Facturas | Gemini Vision → GPT extract → validación → Sheets |
| 5.68jO7jYkjVXyo3T6.json  | WF4 NPS Post-venta | Trigger orden → Wait → NPS → acciones por segmento |
| 6.41qJv25BWf5zJUVY.json  | WF5 Sentiment Dashboard | Cron diario → Sentiment Analysis → alertas Slack |
| 7.ZVhIv6x12Fm6Bb6M.json  | Cargar Knowledge Base |
| 8.EjK7roNFCF6M82UG.json  | Tool - Crear Pedido   |

## Stack técnico
- n8n 2.13.4 (self-hosted Docker, puerto 5679)
- PostgreSQL — Chat Memory + DB principal
- Qdrant — Vector store RAG (colección: ecombot360_knowledge)
- OpenAI GPT-4o-mini + text-embedding-3-small
- Gemini 1.5 Flash — OCR facturas
- Telegram @Luna_Bot — canal principal
