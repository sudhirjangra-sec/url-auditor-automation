# URL Auditor Automation

Automates URL auditing using GitHub Actions.

## How It Works

1. Update `input.xlsx` with the URLs to audit.
2. Configure column mappings in `url_auditor_config.xml`.
3. Trigger the GitHub Actions workflow (or push changes).
4. The workflow downloads the latest URL Auditor release, runs the audit, and saves the results.
5. Generated reports are committed back to the repository.

## Files

```text
input.xlsx                 # URLs to audit
url_auditor_config.xml     # Column mapping configuration
.github/workflows/         # Automation workflow
audit_output/              # Generated reports
```

## Setup

Create a GitHub Actions secret:

```text
AUDITOR_REPO_TOKEN
```

This token is used to download the latest URL Auditor release.

## Running

* Push changes to `input.xlsx` or `url_auditor_config.xml`
* Or manually run the workflow from the **Actions** tab

## Output

Audit reports are saved in:

```text
audit_output/
```

## License

Private/internal project.
