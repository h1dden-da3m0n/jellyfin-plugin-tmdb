<!-- Optional: add a release summary here -->
[Plugin build can be downloaded here](https://repo.jellyfin.org/releases/plugin/themoviedb/themoviedb_2.0.0.0.zip).

## :sparkles: What's New

### :construction_worker: CI & build changes

* add some super cool workflow (#5) @h1dden-da3m0n

EOS)
export VERSION="2.0.0.0"
export CHANGELOG=""
rm cl.md

yq eval ".version = env(VERSION) | .changelog = env(CHANGELOG)" build.yaml
sed -i **/*.csproj   -e "s;<AssemblyVersion>.*;<AssemblyVersion></AssemblyVersion>;"   -e "s;<FileVersion>.*;<FileVersion></FileVersion>;"
