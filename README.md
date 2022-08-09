# openjny/cheat

My cheatsheets for [https://github.com/cheat/cheat](https://github.com/cheat/cheat).

## Getting started

1. Install cheat.

```
scoop install cheat
```

2. Clone this repository.

```
cd ~
git clone --recursive git@github.com:OpenJNY/cheat.git
```

3. Create local copy of the configuration file.

```
cd cheat
cp template.conf.yml conf.yml
```

3. Registor an environment variable `CHEAT_CONFIG_PATH` with value `~/cheat/conf.yml`.

```
# on shell
$env:CHEAT_CONFIG_PATH = "~/cheat/conf.yml"

# on system
[System.Environment]::SetEnvironmentVariable("CHEAT_CONFIG_PATH", "~/cheat/conf.yml", "User")
```

## Update community cheatsheets

```ps1
git submodule init # optional
git submodule update --remote community
git add community
git commit -m "update: community"
```

## Add cheatsheet repo

```
cd ~/cheat
git clone git@github.com:openjny/cheatsheets.git
```

Add settings for the cheatsheets to `~/cheat/conf.yml`, like as follows:

```
  - name: cheatsheets
    path: "~/cheat/cheatsheets"
    tags: [ cheatsheets, foo, bar ]
    readonly: false # true if you want to edit via cheat command.
```

## Basic usage of cheat

```
cheat cheat
```
