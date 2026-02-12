# schutztat-reporting

Odoo 18 management module for Schutztat occupational safety platform.

Syncs Assessment, Hazard, and ActionItem data from the Django risk-hub API
for reporting, Kanban management, and approval workflows.

## Architecture

See [ADR-030](https://github.com/achimdehnert/platform/blob/main/docs/adr/ADR-030-odoo-management-app.md).

## Setup

1. Copy `schutztat_reporting/` to your Odoo addons directory
2. Set system parameters in Odoo Settings → Technical → Parameters:
   - `schutztat.django_api_url` = `https://schutztat.iil.pet/api/v1`
   - `schutztat.django_api_key` = your Bearer token
3. Install the module via Apps menu
4. Sync runs automatically every 15 minutes via scheduled actions
