# Deployment

We provide 3 different types of release builds:

- development (beta/dev)
- staging (rc)
- production (stable)

## Versioning

The format of version is *MAJOR.BUILD*. Everytime we create a new release with same userland, we bump the build number.
The development use here own major number they will be bump for the stable version and the development version go to next major number.

```
0.x = development
1.x = stable
2.x = development
3.x = stable
```

## Git branch/Tag

The branch `dev` ist the actual development branch and from there we never make a release. The `master` branch contains the development version and from there we build a beta release.

If we create a new staging/productive release, we create a new branch `rel-{MAJOR}`. They will be used for the whole cycle of this release.

## Upload release files

We use [ghr](https://github.com/tcnksm/ghr) to upload files to our repository. A binary version is available inside `scripts`.
