# OpenShift NPM Cartridge

## Installation - OpenShift Online

Runs NPM on OpenShift using downloadable cartridge support. To install to OpenShift from the CLI, create your app and then run:

```
rhc add-cartridge http://cartreflect-claytondev.rhcloud.com/reflect?github=twtstudio/openshift-npm
```

## Installation - OpenShift Origin

```
curl -L https://github.com/twtstudio/openshift-npm/archive/master.tar.gz | tar zxv
oo-admin-cartridge -d -a install -s ./openshift-npm-master/ --mco
oo-admin-broker-cache --console
```

Then add composer cartridge to your app via `rhc` cli or web console.

## Markers

| marker | control |
|--------|---------|
| `npm_off` | skipping `npm install` when build |
| `force_clean_build` | clean node_modules pre-saved but not npm cache |


