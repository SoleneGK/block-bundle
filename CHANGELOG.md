# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [4.0.0]

### Changed

- Bump dependencies

## [3.1.1]

### Added

- Adds support for Sonata Admin 4
- Adds documentation on how to use with CKEditor

### Changed

- Updates the `easy_admin/form/panel.html.twig` view

## [3.1.0]

### Added

- Adds support for `symfony/*` ^6.0
- Adds support for EasyAdmin:
    - Adds a `PanelField`, for use in EasyAdmin
    - Adds a `easy_admin/form/panel.html.twig` view
- Adds PHP 8 attributes to the `BlockTrait`

### Changed

- Changes required Stimulus version to `@hotwired/stimulus` and updates controllers accordingly
- Updates the `README` file

### Removed

- Removes the `composer.lock` file

## [3.0.3]

## Fixed

- Add support for symfony/contracts ^2.3

## [3.0.2]

### Added

- Add PHP 8.0 support

### Changed

- Use `useDispatch` in `block` controller instead of a custom event

## [3.0.1]

### Changed

- Use a custom domain for translations

### Added

- Add translations for French and English

## [3.0.0]

### Changed

- Use [Symfony UX](https://symfony.com/ux) with stimulus to handle JS scripts

## [2.0.6]

### Added

- Add a `PanelInterface`

## [2.0.5]

### Changed

- Changes package requirement from `symfony/contracts` to `symfony/translation-contracts`

## [2.0.4]

### Added

- Adds compatibility with v3 of `symfony/contracts`

## [2.0.3]

### Fixed

- Allow the use of translation bundle on content with blocks

## [2.0.2]

### Added

- Add PHP 8.0 support

## [2.0.1]

### Changed

- Add compatibility with Symfony 5.2

## [2.0.0]

### Added

- Add a `Block` entity with `JOINED` inheritance to handle end user blocks
- Add an optional parameter `parameters` to `umanit_block_render` which will be passed to the block manager `render`
  method
- Add a `Block` entity on which all block should rely
- Add an `AbstractBlockType` form type on which all managers form type should rely
- Add a new form theme for Sylius
- Add new javascripts events
    * `ublock.on_sort_start` before sorting blocks in a panel
    * `ublock.on_sort_end` after sorting blocks in a panel

### Changed

- Entities table are prefixed with `umanit_`
- Make the Twig extension lazy loaded
- A block manager is no longer a subclass of Symfony form `AbstractType` but it should define the form type used to
  manage his block with `getManagedFormType`
- Move existing form theme and assets in a `sonata` namespace

### Removed

- Drop support for PHP < 7.1
- Drop support for Symfony < 4.4
- Remove `PanelEventSubscriber` as it becomes useless with the new entity inheritance
- Remove useless `umanit_block` configuration class
- The `AbstractBlockManager` no longer own an `Engine` attribute; If your block rendering needs a template, you must
  inject the `@twig` service yourself

## [1.1.6] - 2019-10-30

Initial version for the CHANGELOG. Last version of the 1.x branch.

[Unreleased]: https://github.com/umanit/block-bundle/compare/4.0.0...HEAD

[4.0.0]: https://github.com/umanit/block-bundle/compare/3.1.1...4.0.0

[3.1.1]: https://github.com/umanit/block-bundle/compare/3.1.0...3.1.1

[3.1.0]: https://github.com/umanit/block-bundle/compare/3.0.3...3.1.0

[3.0.3]: https://github.com/umanit/block-bundle/compare/3.0.2...3.0.3

[3.0.2]: https://github.com/umanit/block-bundle/compare/3.0.1...3.0.2

[3.0.1]: https://github.com/umanit/block-bundle/compare/3.0.0...3.0.1

[3.0.0]: https://github.com/umanit/block-bundle/compare/2.0.6...3.0.0

[2.0.6]: https://github.com/umanit/block-bundle/compare/2.0.5...2.0.6

[2.0.5]: https://github.com/umanit/block-bundle/compare/2.0.4...2.0.5

[2.0.4]: https://github.com/umanit/block-bundle/compare/2.0.3...2.0.4

[2.0.3]: https://github.com/umanit/block-bundle/compare/2.0.2...2.0.3

[2.0.2]: https://github.com/umanit/block-bundle/compare/2.0.1...2.0.2

[2.0.1]: https://github.com/umanit/block-bundle/compare/2.0.0...2.0.1

[2.0.0]: https://github.com/umanit/block-bundle/compare/1.1.6...2.0.0

[1.1.6]: https://github.com/umanit/block-bundle/compare/0.1...1.1.6
