# Rubocop

The `.rubocop.yml` config is based on version `0.82.0` of [Rubocop](https://www.rubocop.org/) gem ([github](https://github.com/rubocop-hq/rubocop)).

## Usage

To use this config in your project, you need to inherit it by adding:

```
inherit_from:
  - https://ghcdn.rawgit.org/Ragnarson/dotfiles/master/rubocop/.rubocop.yml

inherit_mode:
  merge:
    - Exclude
```

to your `.rubocop.yml`. It will use [RawGit](https://rawgit.org/) CDN. You can also use other CDN providers or store the `.rubocop.yml` on your own server.

After running `rubocop` locally, the inherited (dot)file will be generated. If you don't want to track it with git, add the following to your `.gitignore`:

```
# Ignore Rubocop inherited config
.rubocop-https---ghcdn-rawgit-org-Ragnarson-dotfiles-master-rubocop--rubocop-yml
```

## Ruby version

To set target Ruby version for Rubocop to use, add this to your projects `.rubocop.yml`:

```
AllCops:
  TargetRubyVersion: 2.6
```

If you don't do this, Ruby version will be taken from `.ruby-version` file.

## Contributing

If you want to introduce any changes for `.rubocop.yml` file, please open a PR.
