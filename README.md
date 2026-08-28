# TuneCue releases

Update feed for [TuneCue](https://github.com/) — stage MIDI control for
Auto-Tune in UAD Console.

| File | What it is |
|---|---|
| `appcast.xml` | The feed the app polls once a day |
| `TuneCue-<version>.pkg` | The installer that feed points at |

Both are produced by `./make_update.sh "release notes"` in the app repo.
The `.pkg` is signed with an EdDSA key held in the developer's login keychain;
the matching public key is compiled into the app, so a package that was not
signed with it is refused.

Nothing here is built by hand — replace both files together, keeping the same
names, or the app will download a package whose signature no longer matches.
