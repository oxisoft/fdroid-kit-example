# fdroid-kit example: an F-Droid repo on GitHub Pages

Live demo of [fdroid-kit](https://github.com/oxisoft/fdroid-kit)'s GitHub Pages target
([docs](https://github.com/oxisoft/fdroid-kit/blob/main/docs/github-pages.md)).

- Repo: <https://oxisoft.github.io/fdroid-kit-example/fdroid/repo>
- Landing page with fingerprint and QR: <https://oxisoft.github.io/fdroid-kit-example/>

The index is signed with a **throwaway test key**: do not add this repo to a phone you care
about. It serves CyberCalc by OxiSoft, the same Play-signed APK as
[fdroid.oxisoft.io](https://fdroid.oxisoft.io), which is the real repo.

`fdroid/` holds config.yml (no secret: key path and passphrase come from the environment),
the app metadata with its pinned signer, and the repo icon. APKs are not committed: the
action restores them from the live site before each publish.
`.github/workflows/publish.yml` publishes, deploys Pages and verifies the live site.
