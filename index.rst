=======================
Windowsへのインストール
=======================

Pythonのインストール
======================

Windowsは、標準でPythonがインストールされていませんので、Pythonのインストールから説明します。

Pythonをインストールする為のPythonディストリビューションにはAnaconda、ActivePython、IronPython等、他にもいくつかありますが、ここでは公式のPythonインストーラを使います。

Pythonに慣れている方であればどのディストリビューションを選択しても問題無いと思いますが、Pythonに慣れていない方は複数のPythonのインストールを避け、公式のPythonをインストールして下さい。

また、Pythonは2系と3系がありますがPython2は2020年にサポートが終わりますので公式のPython3の最新版 [#latestpython]_ をインストールしましょう。以降は Python3 の説明です。

.. [#latestpython] 2017年現在は Python3.6 系が最新です


まず https://www.python.org/downloads/ (:numref:`download-python`) を開き *Download the latest version for Windows* の下にある *Download Python 3.x.x* をクリック、インストーラをダウンロードして下さい。

.. figure:: /images/pythonorg.jpg
   :name: download-python
   :scale: 60%

   Python インストーラのダウンロード

.. note:: インストーラは 32bit 版と 64bit 版がありますがよくわからなければ 32bit 版をダウンロードして下さい。

ダウンロードが終わったら、インストーラを実行し、インストールを開始します。

.. figure:: /images/pythoninstaller01.png
   :name: pythoninstaller01
   :scale: 100%

   インストール開始

*Install Now* (:numref:`pythoninstaller01`) の直下に表示されているインストールパスをメモしてから、 *Install Now* クリックします。

.. note:: Windows10 の場合は標準で次のようなインストールパスになります。

          ::

              C:\Users\[ユーザ名]\AppData\Local\Programs\Python\Python36-32

.. figure:: /images/pythoninstaller02.png
   :name: pythoninstaller02
   :scale: 100%

   インストール中


.. figure:: /images/pythoninstaller03.png
   :name: pythoninstaller03
   :scale: 100%

   インストール完了ダイアログ

インストールが完了したら *Close* をクリックしてダイアログを閉じましょう。

.. note:: 以前は環境変数の PATH に追加する事を推奨していましたが、この記事では意図せず複数の Python をインストールしている場合がある事を考慮し、 PATH に追加せずに venv という Python の仮想環境機能を利用して Sphinx を実行する方法を説明します。


Sphinxのインストール
====================
venv という Python3.3 以降に追加された仮想環境機能を利用して Sphinx 用の環境を作成し、Sphinx をインストールする手順を紹介します。

コマンドプロンプトを起動して Python のインストール時にメモをしたインストール先をカレントディレクトリにします。 ::

    # 例: ユーザ名が user01 の場合
    cd C:\Users\user01\AppData\Local\Programs\Python\Python36-32

``dir`` コマンドで ``python.exe`` が存在する事を確認して下さい

> dir /b













Python 標準のパッケージ管理コマンド ``pip`` を使って簡単にインストールできます。コマンドプロンプトに以下のようにタイプしエンターキーを押して下さい。

.. code-block:: bat

   > pip install sphinx

これで完了です。インストールが終わったら、コマンドラインから、 ``sphinx-quickstart[エンター]`` とタイプしてみます。 :ref:`sphinx_quickstart` で説明されているような、対話メッセージが表示されればインストールは成功です。Ctrl+Cキーを押して中断しましょう。インストール作業は以上です。次は :doc:`make_project` に進んでください。


.. todo:: コマンドプロンプトを使うので、使い方は自分で調べてねって書き足す

.. todo:: Python のインストールと Sphinx のインストールは、どの OS にも共通の方法を記載し、OS 毎に違う部分は Appendix に入れる

          Windows, Mac, Ubuntu

.. todo:: アップデートの仕方を記載する

