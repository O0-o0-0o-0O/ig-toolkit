# ig-toolkit

Instagramの非公式ログイン・投稿メディア保存を試すための個人用ツール群。

## セットアップ

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```
## スクリプト

### login_test.py

`.env` の認証情報でInstagramに実際にログインできるか確認する。成功時は `sessionid` などのCookieを表示する。

```bash
python login_test.py
```

### save_post_image.py

公開投稿のURL(またはshortcode)を渡すと、画像・動画を保存する。カルーセル投稿は全アイテムを連番で保存する。ログイン不要。

```bash
python save_post_image.py
```

## 注意

- `.env` やセッション情報(`sessionid`など)は絶対にコミット・共有しない。
- 自分が管理するアカウント以外に対してログイン系のスクリプトを使わない。
- Instagram側の内部APIに依存しているため、仕様変更で動かなくなることがある。
