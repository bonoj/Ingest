# Observer report inbox

This public repository is a disposable target for testing authenticated writes from a static web page.

Each accepted report will be a separate JSON file at `reports/<unique-id>.json`.

Suggested payload:

```json
{
  "id": "example-unique-id",
  "observed_at": "2026-10-09T00:00:00Z",
  "build_sha": "example",
  "scene": "jit",
  "observations": {}
}
```

The static page must not embed a GitHub personal access token, OAuth client secret, or other long-lived credential. Public reports must not contain secrets or private information.

This file defines the target only; it does not implement browser authentication or authorize anonymous writes.
