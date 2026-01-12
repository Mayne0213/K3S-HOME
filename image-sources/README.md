# Image Sources

Container image sources for Zot registry mirroring.

Renovate tracks these images and creates PRs when new versions are available.

## Usage

When Renovate creates a PR for a new version:

1. Review the PR
2. Mirror the image to Zot:
   ```bash
   skopeo copy --dest-creds "admin:PASSWORD" \
     docker://SOURCE:TAG \
     docker://zot0213.kro.kr/DEST:TAG
   ```
3. Update the actual K8s manifests in the corresponding repo
4. Merge the PR
