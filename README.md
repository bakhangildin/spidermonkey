# How to build


## Bootstrap system
```console
curl https://hg.mozilla.org/mozilla-central/raw-file/default/python/mozboot/bin/bootstrap.py -O
python3 bootstrap.py --vcs=git

rustup target add wasm32-wasi

curl https://wasmtime.dev/install.sh -sSf | bash
```
Delete mozilla-unified

## Compiling
```console
./js/src/devtools/automation/autospider.py wasi
```

## Running
```console
wasmtime obj-spider/js.wasm 
```