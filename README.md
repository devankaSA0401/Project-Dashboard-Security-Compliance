# Security Compliance Dashboard

A lightweight PHP + SQLite security compliance platform based on a simple checklist model.

## Methodology
- `YES` = control implemented/compliant.
- `NO` = control gap/non-compliant.
- `N/A` = excluded from the denominator.
- Score = `YES / (YES + NO) * 100`.

## Current modules
- Dashboard with overall/domain compliance and charts
- Asset inventory
- Add asset form for Network / Server / Endpoint
- YES / NO / N/A assessment checklist
- Configurable security controls
- Findings foundation

## Flexible asset model
Do not hard-code device names into the score. New devices are added as assets and automatically inherit controls for their selected domain. Future asset types can be introduced by adding a domain and controls rather than rewriting the dashboard.

## Run locally
Requirements: PHP 8+ with PDO SQLite.

```bash
php -S 0.0.0.0:8080
```
Open `http://localhost:8080`.

The SQLite database is created automatically on first run.

## Next recommended phases
1. Import the real Excel workbook into assets/controls.
2. Add login + roles.
3. Add evidence upload and finding creation from `NO` results.
4. Add Excel/PDF reports.
5. Add assessment history and monthly trend.
6. Add API integrations later (Wazuh, vulnerability scanner, monitoring, firewall) without changing the core YES/NO scoring model.
