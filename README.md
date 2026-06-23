# monitor-mediador-releases

Repositório de **distribuição** do Monitor Mediador (não contém código-fonte).

- **`version.json`** (branch `main`): manifesto que o app consulta no boot para saber
  se há versão nova. Campos: `versao_atual`, `url_download`, `notas_atualizacao`, `sha256`.
- **Releases**: cada versão publica o executável `Monitor Mediador.exe` como _asset_.
  O `url_download` aponta sempre para o asset do release mais recente
  (`releases/latest/download/Monitor.Mediador.exe`).

O código-fonte fica em [`mediador-automacao`](https://github.com/JPed552/mediador-automacao).

## Publicar uma nova versão

1. No código-fonte: subir `VERSAO_ATUAL` em `core/config.py` e gerar o `.exe` (`build.bat`).
2. Calcular o SHA256 do `.exe`.
3. Aqui: criar um **Release** novo (tag `vX.Y`), anexar o `Monitor Mediador.exe`.
4. Atualizar o `version.json` (`versao_atual`, `notas_atualizacao`, `sha256`) e dar push no `main`.
