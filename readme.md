# web-ext-submit [![npm version](https://img.shields.io/npm/v/web-ext-submit.svg)](https://www.npmjs.com/package/web-ext-submit)

> Wrapper around Mozilla’s web-ext to submit extensions to AMO.

Mozilla’s `web-ext sign` successfully submits an extension for review, but then it throws an error. This wrapper executes the same command, but then it prevents the unrelated ["_it could not be signed_"](https://github.com/mozilla/web-ext/issues/804#issuecomment-302588357) error.

Tested on OS X and travis/linux. Requires sed, grep and tee (you likely have them on both OSes). This package will only live for as long as `web-ext` natively supports this. Follow [mozilla/web-ext#804](https://github.com/mozilla/web-ext/issues/804)

Used on https://github.com/sindresorhus/refined-github/

## Install

```sh
npm install web-ext-submit
```

## Usage

Since this is just a wrapper around [`web-ext sign`](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/web-ext_command_reference#web-ext_sign), it uses the same env variables and supports the same command-line flags as that command.

```sh
WEB_EXT_API_KEY=blahla
WEB_EXT_API_SECRET=blahla
web-ext-submit
```

or

```sh
web-ext-submit --api-key=blahbla --api-secret=blahla
```

## Related

* [`mozilla/web-ext`](https://github.com/mozilla/web-ext): A command line tool to help build, run, and test web extensions.
* [`webext-dynamic-content-scripts`](https://github.com/bfred-it/webext-dynamic-content-scripts): Automatically inject your `content_scripts` on custom domains.
* [`webext-content-script-ping`](https://github.com/bfred-it/webext-content-script-ping): One-file interface to detect whether your content scripts have loaded.
* [`webext-options-sync`](https://github.com/bfred-it/webext-options-sync): Helps you manage and autosave your extension's options.
* [`Awesome WebExtensions`](https://github.com/bfred-it/Awesome-WebExtensions): A curated list of awesome resources for Web Extensions development.

## License

MPL-2.0 © Federico Brigante — [Twitter](http://twitter.com/bfred_it)
