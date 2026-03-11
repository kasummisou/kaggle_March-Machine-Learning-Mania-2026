# Kaggle March Machine Learning Mania 2026

## セットアップ

### 前提条件

- Python 3.11 以上
- Poetry（Python パッケージマネージャー）
- Kaggle アカウント

### Poetry を使用する（推奨）

#### 1. Poetry のインストール

Poetry がインストール済みでない場合：

```bash
pip install poetry
```

または、公式インストーラーを使用：

```bash
curl -sSL https://install.python-poetry.org | python3 -
export PATH="$HOME/.local/bin:$PATH"  # ~/.bashrc または ~/.zshrc に追加
```

#### 2. Kaggle API キーを取得

```bash
# ブラウザで開く
open https://www.kaggle.com/account/settings/account

# "API" セクションから "Create New API Token" をクリック
# → kaggle.json がダウンロードされます

# プロジェクトルートに kaggle.json を配置
cp ~/Downloads/kaggle.json ./

# .gitignore で自動除外されます（セキュリティ保護）
```

#### 3. 仮想環境の構築と依存関係のインストール

```bash
# 仮想環境を構築してパッケージをインストール
poetry install
```

#### 4. Jupyter Lab の実行

**方法 1: Poetry の仮想環境で直接実行**

```bash
poetry run jupyter lab
```

**方法 2: 仮想環境を有効化してから実行（推奨）**

```bash
# 仮想環境を有効化
poetry shell

# Jupyter Lab を起動
jupyter lab

# 仮想環境から抜ける
exit
```

#### 5. よく使うコマンド

```bash
# スクリプトを実行
poetry run python script.py

# 新しいパッケージを追加
poetry add package_name

# パッケージを削除
poetry remove package_name

# 仮想環境にログイン
poetry shell

# 仮想環境情報の確認
poetry env info

# インストール済みパッケージ一覧
poetry show
```

## 構成

- `notebooks/` - Jupyter ノートブック
- `Date/` - データセット（.gitignore で除外）
- `pyproject.toml` - Poetry プロジェクト設定
- `poetry.lock` - Poetry ロックファイル（正確な版管理）
- `requirements.txt` - 参考用（Poetryに統合済み）
- `kaggle.json` - Kaggle API キー（.gitignore で除外）
