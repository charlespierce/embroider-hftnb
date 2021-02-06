# embroider-hftnb

Reproduction of an issue with Embroider builds and [`ember-holy-futuristic-template-namespacing-batman`](https://github.com/rwjblue/ember-holy-futuristic-template-namespacing-batman)

## Steps to Reproduce

Run `ember build` and notice the error

## Expected Behavior

The build completes successfully. Note that this _does_ work under classic ember build, which you can see by running:

```sh
CLASSIC=1 ember build
```

## Actual Behavior

The build fails with an error on parsing a template:

```
Build Error (PackagerRunner) in lib/my-addon/templates/components/my-component.hbs

Module Error (from ~/embroider-hftnb/node_modules/@embroider/hbs-loader/src/index.js):
Parse error on line 1:
Announcement: {{my-addon@other-compo
----------------^
Expecting 'ID', 'STRING', 'NUMBER', 'BOOLEAN', 'UNDEFINED', 'NULL', 'DATA', got 'INVALID'
```