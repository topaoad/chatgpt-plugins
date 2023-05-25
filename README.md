# ChatGPT plugins quickstart

Get a todo list ChatGPT plugin up and running in under 5 minutes using Python. If you do not already have plugin developer access, please [join the waitlist](https://openai.com/waitlist/plugins).

## Setup

To install the required packages for this plugin, run the following command:

```bash
pip install -r requirements.txt
```

To run the plugin, enter the following command:

```bash
python main.py
```

Once the local server is running:

1. Navigate to https://chat.openai.com. 
2. In the Model drop down, select "Plugins" (note, if you don't see it there, you don't have access yet).
3. Select "Plugin store"
4. Select "Develop your own plugin"
5. Enter in `localhost:5003` since this is the URL the server is running on locally, then select "Find manifest file".

The plugin should now be installed and enabled! You can start with a question like "What is on my todo list" and then try adding something to it as well! 

## Getting help

If you run into issues or have questions building a plugin, please join our [Developer community forum](https://community.openai.com/c/chat-plugins/20).


## 開発環境について
venv環境推奨。現在のところDockerへのマウントは検討していない。
venv環境構築の手順
- python3 -m venv venv でvenvを作成する
- source venv/bin/activate でvenvの環境を起動する
- pip install -r requirements.txt
- python script.py などでスクリプトの実行をする
- deactivate でvenvの環境を終了する

## 必要な構築物について
- マニフェストファイル(ai-plugin.json)の作成
- モックAPI（main.py）の作成
- Open APIの定義 (openapi.yaml)の作成
- プラグインの実行スクリプト

## 必要な構築物について
- APIエンドポイントの作成（API Gateway✖︎Lambda）
- モックAPIの内容の精査
- 必要に応じてDBの作成やDocker環境の構築