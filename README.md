# sls-releases

Public download host for Stock Label Studio desktop installers and their update manifests, served by GitHub Pages.
The app's source code is not here.

## What is here now

`rc/` holds an **internal test only**: two Release Candidate versions used to prove that a Release Candidate app
updates itself safely from one version to the next. It is not a product release, it is not linked from the website,
and it may be removed after the test. Release Candidate apps install apart from the real app and never touch its data.

There is no Stable (customer) release yet. The website Download button does not point here.

## Layout

- `<channel>/latest.json`: the update manifest that installed apps of that channel read
- `<channel>/<version>/`: the installer, its updater signature (`.sig`) and a release record. Never replaced once published.

Every installer is signed with the channel's own updater key; installed apps refuse anything that does not verify.
