# Packaging

## macOS

Gera bundle em `dist/`

```console
bash packaging/build_macos.sh
```

## Linux

Gera binário em `dist/` para converter em AppImage

```console
bash packaging/build_linux.sh
```

## Windows

Gera um executável único e independente em `dist/`.

```console
powershell -ExecutionPolicy Bypass -File packaging/build_windows.ps1
```

Saída:

```text
dist/spsvalidator.exe
```

O arquivo pode ser distribuído e executado isoladamente. Não é necessário
instalar Python nem copiar diretórios auxiliares como `_internal`.

O build deve ser executado em Windows, pois o PyInstaller não realiza
compilação cruzada entre sistemas operacionais.
