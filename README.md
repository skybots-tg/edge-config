# edge-config

Подписанный список доменов для клиентских приложений. Файлы генерируются на
сервере и обновляются автоматически; править их руками нельзя — подпись не
сойдётся.

- `cfg.json` — конверт `{payload, sig, alg, kid}`, Ed25519 над байтами строки `payload`
- `cfg.txt` — то же одной строкой, `v1.<base64url payload>.<base64url sig>`

Читается как `https://cdn.jsdelivr.net/gh/<owner>/edge-config@main/cfg.json`
и `https://<owner>.github.io/edge-config/cfg.json`.
