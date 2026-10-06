# Relatório coleta — Piloto Ana
**Quando:** 2026-10-06T20:59:59.646105+00:00 (box UTC; user America/Sao_Paulo)
**Arquivo:** `/workspace/piloto-ana/data/mentions.json`
**Total:** 60 menções reais (0 inventadas)

## Contagens

| Marca | LinkedIn | Instagram | Imprensa | Total |
|-------|----------|-----------|----------|-------|
| Starian | 7 | 0 | 6 | 13 |
| Checklist Fácil | 10 | 0 | 0 | 10 |
| Projuris | 9 | 0 | 2 | 11 |
| Sienge | 10 | 0 | 3 | 13 |
| Contato Seguro | 10 | 0 | 3 | 13 |

## O que falhou / gaps
1. **Instagram: 0** — sem `APIFY_API_TOKEN`; páginas IG exigem login / bloqueiam scrape leve.
2. **LinkedIn keyword de terceiros (sem @):** sem Apify; coleta = posts públicos das **páginas oficiais** das 5 marcas (métricas reais de like/comentário quando a UI mostrou).
3. **Shares / reach:** quase sempre null (não públicos na UI).
4. **Checklist Fácil imprensa recente (7–14d):** Google News não trouxe artigo de portal novo no recorte; só LinkedIn da marca.
5. **Google News RSS:** links `news.google.com` não resolveram para canônico via curl simples — usei URLs canônicas de busca/WebFetch.

## Próximo passo (alerta WhatsApp)
- Cron diário: re-fetch páginas LI + RSS Google News → diff por URL → msg 09:00 BRT com N novas + top 3 engajamento.
- Desbloquear IG/LI keyword: creditar Apify (≤ R$2k/14d) ou equivalente.
