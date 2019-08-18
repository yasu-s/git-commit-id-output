# 概要

Gitで現在のブランチのコミットIDをファイルに出力するシェルスクリプトのサンプルです。  

# 実行環境

* Bash
* Git

# サンプルソース

## ./output-text.sh

現在のブランチのコミットIDのみをテキストファイルに出力するサンプルです。

```shell
git log -n 1 --pretty=format:"%H" > dist/commit-id.txt
# c8f8ab484161c025f5b1e62135f3d067aa841791
```

## ./output-json.sh

現在のブランチのコミットIDをJSON形式のファイルに出力するサンプルです。

```shell
git log -n 1 --pretty=format:"{ \"commitId\": \"%H\" }" > dist/commit-id.json
# { "commitId": "c8f8ab484161c025f5b1e62135f3d067aa841791" }
```
