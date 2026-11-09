# Amir's Living Koi

Amir's Living Koi turns public GitHub activity into an elegant, language-colored
koi with organic movement, playful turns, occasional jumps, feeding moments, and
subtle bubbles. The fish's language coat, growth, and streak markings still come
from the existing Git Koi pipeline. A nightly workflow can place the looping GIF
on a GitHub profile README.

<p align="center">
  <img src="docs/bodies-light.png" width="432" alt="Amir's Living Koi color and body designs" />
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/bodies-dark.png" />
  <img src="docs/bodies-light.png" alt="The six bodies, white, black, Asagi, tea, gold, and platinum, at each growth stage" />
</picture>

## Repository Structure

```text
.
├── .github/      workflows, issue forms, and Dependabot
├── docs/         the getting-started guide and the render sheets
├── examples/     the profile workflow and the koi library generator
├── src/          the library and the git-koi command
├── tests/        the public-boundary tests and their fixtures
└── action.yml    the GitHub Action
```

## Usage

### Show it on your profile

Copy [examples/profile-workflow.yml](examples/profile-workflow.yml) into your
profile repository as `.github/workflows/koi.yml`, publish a compatible release
from this fork, and add this to its `README.md`:

```html
<img src="koi/koi.gif" width="432" alt="Amir's Living Koi" />
```

The Action writes `koi/koi.gif` as a 512 × 512 infinitely looping GIF; the
snippet displays it at 432 pixels wide.

### Requirements

- For a koi on your profile README: a GitHub account. The Action runs in your
  profile repository's workflow with its built-in token.
- For the command line: a binary from the
  [releases page](https://github.com/amiraftorrr-spec/git-koi/releases), or Rust
  at or above the `rust-version` in [Cargo.toml](Cargo.toml), plus the
  [GitHub CLI](https://cli.github.com), authenticated.
- For the library: Rust at or above that same version.

[docs/getting-started.md](docs/getting-started.md) walks through all three: the
Action in a profile workflow, the command line, and the library. The API is
documented on [docs.rs](https://docs.rs/git-koi).

## Author

**Amir**

- GitHub: [@amiraftorrr-spec](https://github.com/amiraftorrr-spec)

This fork builds on [Git Koi by Anthony Yalong](https://github.com/yalongwastaken/git-koi).

## License

MIT. See [LICENSE](LICENSE).
