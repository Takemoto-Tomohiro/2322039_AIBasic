# 2322039_AIBasic

THX for downroading!!

-はじめに-
このデータは「https://qiita.com/ysiny/items/b01250228e0c5cc0e647」、「https://qiita.com/ysiny/items/30e10a3db76c6f7c5b4d」を参考にし、また、コードもそちらのサイトからダウンロードさせてもらったものを書き換えつつ利用しています。

-使い方-

*仮想環境ごとリポジトリに入れてあります。

1,ダウンロードしたフォルダをローカル上の適切な場所に入れる

2,ファイルの補完
　→GitHubにアップロードする際に100MB以上のファイルが許可されなかったため、別途で補完。次のGoogleDriveのリンクよりフォルダにアクセスし、「libtorch_cpu.dylib」と「bert_fine_tuning_chABSA.pth」をダウンロード。その後、「libtorch_cpu.dylib」は「Task2_venv/lib/python3.9/site-packages/torch/lib/」の直下に、「bert_fine_tuning_chABSA.pth」は「drf/appv1/weights/」の直下に保存。
リンク：https://drive.google.com/drive/folders/1ROgZiuqUAY6aeCuhrhhXcI1e0OZdN8yw?usp=share_link

3,仮想環境を立ち上げる
　→ダウンロードした場所まで移動(なにもしなければダウンロードフォルダだが、解凍やファイル名の変更が必要な可能性あり)。ファイル名やパス等は環境によって違う可能性もあるので、適宜変更。
 ターミナルにて「source Task2_venv/bin/activate」を実行する

4,APIを走らせる
　→ターミナルにて「cd drf/」を実行。その後
「
python manage.py migrate
python manage.py runserver --noreload --nothreading
」
を実行。

5,実際に動かす
　→「http://127.0.0.1:8000/api/v1/predict/」にアクセスする

6,画面下部のテキスト欄に判定したいテキストを入力する
