<div align="center">

<img src="snap/gui/folo.png" alt="Folo logo" width="128" />

# Folo

**Feeds, newsletters, podcasts and social media in one AI-assisted timeline**

[![folo](https://snapcraft.io/folo/badge.svg)](https://snapcraft.io/folo)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architecture: amd64](https://img.shields.io/badge/Architecture-amd64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Folo](https://github.com/RSSNext/Folo), an AI RSS reader whose desktop app connects to the hosted Folo service.

</div>

---

## Getting Started

<a href="https://snapcraft.io/folo"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install folo
folo
```

You can also launch Folo from the application menu. Sign in through your browser and allow it to reopen Folo.

## Configure

Use the application's settings. There are no `snap set` options.

```bash
sudo snap connect folo:removable-media    # optional: import and export on /media, /mnt
```

The profile and caches are stored in `~/snap/folo/common`.

## Limitations

- Files must be in your home directory or connected removable storage. Hidden folders in your home directory are not accessible.
- Syncing the sign-in to the `folocli` command-line tool is unavailable: the snap cannot run the host's `npx` or write `~/.folo`.
- An existing native installation's profile is not imported. Application updates are managed by snapd.

## Build

```bash
git clone https://github.com/sidalit/folo-snap.git
cd folo-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/folo-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/RSSNext/Folo/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/folo-snap/blob/main/LICENSE).
