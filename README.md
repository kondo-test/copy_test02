# Azure Open AI の入門ハンズオン

## 概要
Azure Open AI でAIモデルのデプロイや利用を通じて
用意されたAIの利用だけでなくカスタマイズ等の一端を体験する

<br>

## 目的

Azure Open AI の入門<br>
関連するAI情報、Microsoft情報の習得<br>

<br>

## ハンズオンの内容

このハンズオンでは実際に以下の内容を学びます。

- Azure ポータルサイトの操作
- Azure OpenAI Studio の利用
- モデルのデプロイ、利用
- VSCodeから Azure OpenAI サービスの利用


<br>

## 対象者

このチュートリアルは以下の知識がある方を対象としています。

- 会話型の生成AI(CopilotやChatGPTなどの)使用方法、プロンプトの基本知識
	- ハンズオン内で使うコード生成のために利用
	- ハンズオン内でのカスタマイズ対象
- Microsoft Azure の基本的な知識
- Visual Studio Code(VSCode)を使用したコーディング経験
	- このチュートリアルでは、VSCodeを使用して演習用ボットアプリケーションを作成します。
 	- VSCodeでのコーディング経験が必要です。


## 要件

このチュートリアルを実施するには以下の環境が必要です。

- [**Microsoft Azure サブスクリプション**](https://azure.microsoft.com/ja-jp/free/)
	- 今回は本日のみ利用できる環境をJMIXで用意しますが、個人で実施したい場合は別途用意が必要です。

<!--
と Azure Open AI サービスの[利用資格](https://aka.ms/oaiapply)**

    >【重要】現在、Azure Open AI の利用は Microsoft と既存のパートナーシップ関係があるお客様、リスクの低いユース ケース、軽減策の取り入れに取り組んでいるお客様に制限されており、**利用には申請が必要**です。申請については、以下の申請フォームに記載されています。 利用を開始するにはこちらからお申し込みください。

    - [**Azure OpenAI Service へのアクセス申請**](https://aka.ms/oaiapply)
-->

- [**Visual Studio Code**](https://code.visualstudio.com/)

    - [**REST Client 拡張**](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) （演習3で使用）

<!--
    Visual Studio Code から Azure のリソースを作成するための以下の拡張もインストールしてください。
    - [Azure Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack)
-->

- [**Node.js**](https://nodejs.org/ja/)

    - v22.11.0(LTS)バージョン (2024 年 11 月現在の最新の LTS) 


    > もし、V22.11.0 で動作しない場合は、v20.17.0 もしくは v20.18.0 の LTS バージョンでお試しください。なお、ローカル環境で Node.js のバージョンを切り替える必要がある場合には Windows では [**nvm-windows**](https://github.com/coreybutler/nvm-windows) 、Mac では [nvm](https://github.com/nvm-sh/nvm) を使用すると便利です。
    > 詳しくは以下のドキュメントを参照してください。

    - [**nvm-windows のインストール**](https://learn.microsoft.com/ja-jp/windows/dev-environment/javascript/nodejs-on-windows#install-nvm-windows-nodejs-and-npm)

    - [**nvm のインストール**](https://learn.microsoft.com/ja-jp/windows/dev-environment/javascript/nodejs-on-wsl#install-nvm-nodejs-and-npm)

- WSLのインストール
  - curlコマンド実行のためWSLのインストール（PCの再起動が求められることがあります）
  - ターミナル画面、あるいはコマンドライン画面を表示し、以下のコマンドを実行して WSL をインストールしてください。
  ```powershell
  wsl --install
  ```

## 演習

1. [**Azure Open AI リソースの作成**](Ex01-0.md)

    - [1.1 : Azure ポータルから Open AI リソースを作成する](Ex01-1.md)
    - [1.2 : Azure OpenAI Studio から言語モデル gpt-4o-mini のデプロイ](Ex01-2.md)
    - [1.3 : Azure OpenAI Studio から埋め込みモデル : text-embedding-ada-002 のデプロイ](Ex01-3.md)
    - [1.4 : Azure OpenAI Studio から画像生成モデル : dall-e-3 のデプロイ](Ex01-4.md)
	    
2. [**Azure OpenAI Studio からの AI モデルの利用**](Ex02-0.md)
    - [2.1 : システムメッセージとパラメーター設定](Ex02-1.md)
    - [2.2 :プロンプト エンジニアリング ](Ex02-2.md)
  
<!--
    - [2.3 : 独自データの追加](Ex02-3.md)
    - [オプション : Azure OpenAI Studio で作成したチャットボットを Azure App Service にデプロイ](Ex02-3.md#%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3--azure-openai-studio-%E3%81%A7%E4%BD%9C%E6%88%90%E3%81%97%E3%81%9F%E3%83%81%E3%83%A3%E3%83%83%E3%83%88%E3%83%9C%E3%83%83%E3%83%88%E3%82%92-azure-app-service-%E3%81%AB%E3%83%87%E3%83%97%E3%83%AD%E3%82%A4)
-->
3. [**Azure Open AI サービスとアプリケーションの統合**](Ex03-0.md)
    - [3.1 : Azure Open AI サービスの API 利用](Ex03-1.md)
        - [タスク 1 : curl コマンドによる呼び出しの確認](Ex03-1.md#%E3%82%BF%E3%82%B9%E3%82%AF-1---curl-%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%81%AB%E3%82%88%E3%82%8B%E5%91%BC%E3%81%B3%E5%87%BA%E3%81%97%E3%81%AE%E7%A2%BA%E8%AA%8D)
        - [タスク 2 :  HTTP Client ツールによる呼び出しの確認](Ex03-1.md#%E3%82%BF%E3%82%B9%E3%82%AF-2-http-client-%E3%83%84%E3%83%BC%E3%83%AB%E3%81%AB%E3%82%88%E3%82%8B%E5%91%BC%E3%81%B3%E5%87%BA%E3%81%97%E3%81%AE%E7%A2%BA%E8%AA%8D)
    - [3.2 : ボット アプリケーションの作成](Ex03-2.md)
        - [タスク 1 : コンソールで動作するオウム返しアプリケーションの作成](Ex03-2.md#%E3%82%BF%E3%82%B9%E3%82%AF-1--%E3%82%B3%E3%83%B3%E3%82%BD%E3%83%BC%E3%83%AB%E3%81%A7%E5%8B%95%E4%BD%9C%E3%81%99%E3%82%8B%E3%82%AA%E3%82%A6%E3%83%A0%E8%BF%94%E3%81%97%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AE%E4%BD%9C%E6%88%90)
	    - [タスク 2 : Azure OpenAI ライブラリを利用した言語モデルへのメッセージの送信](Ex03-2.md#%E3%82%BF%E3%82%B9%E3%82%AF-2--azure-openai-%E3%83%A9%E3%82%A4%E3%83%96%E3%83%A9%E3%83%AA%E3%82%92%E5%88%A9%E7%94%A8%E3%81%97%E3%81%9F%E8%A8%80%E8%AA%9E%E3%83%A2%E3%83%87%E3%83%AB%E3%81%B8%E3%81%AE%E3%83%A1%E3%83%83%E3%82%BB%E3%83%BC%E3%82%B8%E3%81%AE%E9%80%81%E4%BF%A1)
        - [タスク 3 : コンソールで動作する基本的なチャットボット アプリの作成](Ex03-2.md#%E3%82%BF%E3%82%B9%E3%82%AF-3--%E3%82%B3%E3%83%B3%E3%82%BD%E3%83%BC%E3%83%AB%E3%81%A7%E5%8B%95%E4%BD%9C%E3%81%99%E3%82%8B%E5%9F%BA%E6%9C%AC%E7%9A%84%E3%81%AA%E3%83%81%E3%83%A3%E3%83%83%E3%83%88%E3%83%9C%E3%83%83%E3%83%88-%E3%82%A2%E3%83%97%E3%83%AA%E3%81%AE%E4%BD%9C%E6%88%90)


<br>


---
## LICENSE

このドキュメントに記載されている情報 (URL や他のインターネット Web サイト参照を含む) は、将来予告なしに変更することがあります。別途記載されていない場合、このソフトウェアおよび関連するドキュメントで使用している会社、組織、製品、ドメイン名、電子メール アドレス、ロゴ、人物、場所、出来事などの名称は架空のものです。実在する商品名、団体名、個人名などとは一切関係ありません。お客様ご自身の責任において、適用されるすべての著作権関連法規に従ったご使用をお願いいたします。著作権法による制限に関係なく、マイクロソフトの書面による許可なしに、このドキュメントの一部または全部を複製したり、検索システムに保存または登録したり、別の形式に変換したりすることは、手段、目的を問わず禁じられています。ここでいう手段とは、複写や記録など、電子的、または物理的なすべての手段を含みます。

マイクロソフトは、このドキュメントに記載されている内容に関し、特許、特許申請、商標、著作権、またはその他の無体財産権を有する場合があります。別途マイクロソフトのライセンス契約上に明示の規定のない限り、このドキュメントはこれらの特許、商標、著作権、またはその他の知的財産権に関する権利をお客様に許諾するものではありません。

製造元名、製品名、URL は、情報提供のみを目的としており、これらの製造元またはマイクロソフトのテクノロジを搭載した製品の使用について、マイクロソフトは、明示的、黙示的、または法令によるいかなる表明も保証もいたしません。製造元または製品に対する言及は、マイクロソフトが当該製造元または製品を推奨していることを示唆するものではありません。掲載されているリンクは、外部サイトへのものである場合があります。これらのサイトはマイクロソフトの管理下にあるものではなく、リンク先のサイトのコンテンツ、リンク先のサイトに含まれているリンク、または当該サイトの変更や更新について、マイクロソフトは一切責任を負いません。リンク先のサイトから受信した Web キャストまたはその他の形式での通信について、マイクロソフトは責任を負いません。マイクロソフトは受講者の便宜を図る目的でのみ、これらのリンクを提供します。また、リンクの掲載は、マイクロソフトが当該サイトまたは当該サイトに掲載されている製品を推奨していることを示唆するものではありません。

Copyright (c) Microsoft Corporation. All rights reserved.
