## インストール

この勉強会では最もメジャーなディストリビューションである`Ubuntu`をインストールする。

!!! info "ディストリビューション"
    利用者が容易にインストール・利用できるように、Linuxカーネルとその他ソフトウェア群を1つにまとめたもの。<br>
    `Ubuntu`以外にも多数存在しており、`Debian`や`CentOS`なども有名。

### WSLの機能を有効化

1. 「コントロールパネル」を開く
2. 「プログラム」＞「Windowsの機能の有効化または無効化」
3. 以下の ==２つ== にチェックを入れて「OK」
      * Hyper-V プラットフォーム
      * Linux 用 Windows サブシステム
4. Windows 再起動

<figure markdown>
  ![Enabled WSL](../../assets/images/wsl_enable_settings.drawio.svg){ width="550" }
  <figcaption>WSL機能の有効化</figcaption>
</figure>

### コマンドでインストール

PowerShellを起動してコマンドを実行する。

!!! note "インストール可能なディストリビューションの確認コマンド"

    ```powershell
    wsl --list --online
    ```

    ??? example "実行結果"

        ```
        インストールできる有効なディストリビューションの一覧を次に示します。
        'wsl --install -d <Distro>' を使用してインストールします。

        NAME            FRIENDLY NAME
        Ubuntu          Ubuntu
        Debian          Debian GNU/Linux
        kali-linux      Kali Linux Rolling
        openSUSE-42     openSUSE Leap 42
        SLES-12         SUSE Linux Enterprise Server v12
        Ubuntu-16.04    Ubuntu 16.04 LTS
        Ubuntu-18.04    Ubuntu 18.04 LTS
        Ubuntu-20.04    Ubuntu 20.04 LTS
        ```

!!! note "インストール可能なディストリビューションの確認コマンド"

    ```powershell
    wsl --install -d Ubuntu
    ```

    ??? example "実行結果"

        ```
        ダウンロード中: Ubuntu
        インストール中: Ubuntu
        Ubuntu はインストールされました。
        Ubuntu を起動しています...
        ```

正常にインストールできると、Winメニューに最近追加としてUbuntuのアプリが追加される。

<figure markdown>
  ![Install WSL](../../assets/images/wsl_install.drawio.svg){ width="300" }
  <figcaption>インストールされたWSL（Ubuntu）</figcaption>
</figure>

!!! tip "Tips"

    Ubuntuなどのディストリビューションごとのアプリは、`Microsoft Store`でもインストールできる。