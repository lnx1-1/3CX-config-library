# 3CX Config Library

Custom provisioning templates, small tweaks, and helper scripts for 3CX.

## Repository structure
- `templates/` Provisioning templates grouped by vendor and model
- `scripts/` Helper scripts for managing or validating configs (optional)
- `docs/` Notes and guidance (optional)

## Usage
### Option A: Upload via 3CX Web UI
Use the 3CX Management Console to upload the template, then assign it to the device model.

### Option B: Place the file on the server
Linux (default 3CX install):
- `/var/lib/3cxpbx/Instance1/Data/Http/Interface/provisioning/<tenant>/CustomTemplates/fxs/`

Windows (default 3CX install):
- `C:\ProgramData\3CX\Instance1\Data\Http\Interface\provisioning\<tenant>\CustomTemplates\fxs\`

Notes:
- Replace `<tenant>` with your provisioning folder (example: `ox05wy2n8vt6pa`).
- After placing the file, assign the template to the phone model in the 3CX console.

## Current template
- Yealink W70B (FXS) custom provisioning template
- File: `templates/yealink/w70b/yealink.W70B_CustomV1.fxs.fxs.xml`

## What this changes vs stock
- This is a custom provisioning template (not firmware).
- It is functionally aligned with the stock 3CX Yealink W70B template.
- The main functional change is the custom template name/model binding so 3CX serves this file.
- Any additional differences are formatting-only and do not change device behavior.

## Contributing
Add new templates under `templates/<vendor>/<model>/` and document any functional deviations from stock templates.
