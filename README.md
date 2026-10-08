# Repro for issue 11247

## Versions

firebase-tools: v15.33.0

## Steps to Reproduce

1. Run `firebase deploy` in `project-a`
2. Run `firebase hosting:clone tools-11247-a:live tools-11247-b:live --project=tools-11247-b` in `project-a`
3. See the error 
```
$ firebase hosting:clone tools-11247-a:live tools-11247-b:live --project=tools-11247-b

Error: Could not find the channel live for site tools-11247-a.
```

## Notes

Not reproducible on firebase-tools v15.31.0 or 15.32.1

```
$ firebase --version
15.31.0
$ firebase hosting:clone tools-11247-a:live tools-11247-b:live --project=tools-11247-b
✔ Cloning site content...
✔  Site tools-11247-a channel live has been cloned to site tools-11247-b channel live.
✔  Channel URL (live): https://tools-11247-b.web.app
```

```
$ firebase --version
15.32.1
$ firebase hosting:clone tools-11247-a:live tools-11247-b:live --project=tools-11247-b
✔ Cloning site content...
✔  Site tools-11247-a channel live has been cloned to site tools-11247-b channel live.
✔  Channel URL (live): https://tools-11247-b.web.app
```