# Enonic Site Framework tutorial fixture

Sample content for the [Enonic Site Framework tutorial](https://developer.enonic.com/learn/enonic-site-framework).

When the app starts, it creates the content project `siteframework` (displayed as `Site Framework`) and imports the
content in `src/main/resources/import/`: the `Hello World` site, three countries, their cities, and three photos.
If the project already exists, the app does nothing.

The app holds content only. The content types are created by the reader of the tutorial, in an app that must be named
`com.example.tutorial.siteframework`, because the content refers to its content types by that name. The site has no
application assigned; the reader adds theirs in Content Studio.

## Build

```bash
enonic project build
```

The app is built to `build/libs/tutorial-siteframework-fixture.jar`.

## Install

Upload the jar from the Install dialog in the Applications admin tool, or copy it to the `deploy` folder of the XP home.

## Updating the content

Edit the content in a sandbox, export `/content/hello-world` from the `draft` branch of the project, and replace the
contents of `src/main/resources/import/` with the unpacked export. Remove the application from the site before
exporting. The complete content at the end of the tutorial lives in
https://github.com/enonic/tutorial-site-framework and must be re-exported when the sample content changes.

## Compatibility

| Version | Enonic XP |
|---------|-----------|
| 1.0.0 | 8.1 |
