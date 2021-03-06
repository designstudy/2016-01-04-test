# Eclipseのインストール・設定
Javaのプログラミングを行なう際、前述のようにコマンドプロンプトを使用した方法の他に、IDE（統合開発環境）と呼ばれるプログラム開発用のソフトウェアを使用する方法があります。IDEとは、プログラミングを行なう上で必要となる、エディタやコンパイル実行機能、デバッガなどが1つになっているもので、非常に便利なツールです。ほとんどのJavaアプリ開発の現場ではなんらかのIDEが使われています。ここでは、数あるIDEのうち、もっともよく使われているEclipseというソフトを使用できるようにします。

## インストール

***

ダウンロードについては割愛します。以下のMergeDoc Project のサイトからPleiades All-in-One Eclipse Java をダウンロードするのがよいです。
■Pleiades - Eclipseプラグイン日本語化プラグイン| MergeDoc Project:
http://mergedoc.sourceforge.jp/

***

※以下、All-In-OneEclipseのバージョン3.1.1を前提に説明します。Eclipseのインストーラをダブルクリックしてください。インストーラが立ち上がりますので、しばらく待ちましょう。言語を選択するウィンドウが立ち上がったら、そのまま「Japanese」を選択してください。  

![img](images\EclipseInstall\Language.png)  


画面が変わったら、基本的には「次へ」ボタンを押下してください。途中、ライセンスに同意する箇所がありますので、「同意します」にチェックを入れ、「次へ」ボタンを押下してください。

![img](images\EclipseInstall\Setup1.png)  


![img](images\EclipseInstall\Setup2.png)  



インストール先を設定する画面が表示されますが、そのままで構いません。「インストール」ボタンを押しましょう。インストールが始まったら、終わるまでしばらく待ちましょう。  
![img](images\EclipseInstall\Setup3.png)  
  

![img](images\EclipseInstall\Setup4.png)  


インストール作業が終了すると、以下のようなウィンドウが表示されます。「完了」ボタンを押下し、Eclipseを起動してみましょう。
![img](images\EclipseInstall\Setup5.png)  


しばらくすると、「ワークスペース」を選択するウィンドウが表示されます。ワークスペースというのは、Eclipse上で作成したプログラムを保管しておくためのフォルダのことです。作成したプログラムはここで選択したフォルダの中に保管されることになります。これは任意の場所で構いません。試しに「D:\workspace_test」としてみましょう。入力したら、「OK」ボタンを押してください。

![img](images\EclipseInstall\Starting1.png)  

以下のような画面が立ち上がります。この画面では特に何もしませんので、左上の「×」を押下してください。
![img](images\EclipseInstall\Starting2.png)  


最後に、以下のような画面が表示されます。これがEclipseのメインになる画面であり、プログラムはここで作成することになります。  
![img](images\EclipseInstall\Starting3.png)  


#### Eclipseのバージョン
EclipseのバージョンEclipseはこれまでに何回もバージョンアップを繰り返しています。ただ、現場では「以前のバージョンでないと不都合がある」などの理由から、必ず最新バージョンが使われているとは限りません。Eclipseの各バージョンにはコードネームが付与されています（3.2以降）。ちょっとまとめてみましょう。

3.2…Callisto  
3.3…Europa  
3.4…Ganymede  
3.5…Galileo  
3.6…Helios  
3.7…Indigo  
4.2…Juno  

3.2から3.5までは木星の衛星の名前ですね。3.5はもともとIo（イオ）になる予定だったのが、他の単語と紛らわしいことから最終的にこの名前に決まったそうです。

## Javaのバージョンや名称について
Javaのバージョンや名称については、複雑で分かりにくいものが多々あります。まとめておきましょう。

1. バージョンについて

    |バージョン|内部バージョン|
    |:-:|:-:|
    |1.1|1.1|
    |1.2|1.2|
    |1.3|1.3|
    |1.4|1.4|
    |5.0|1.5|
    |6.0|1.6|
    |7.0|1.7|
    
    バージョンは、内部バージョン1.5より表向きのバージョンとしては「5.0」となりました。以降、「6.0」「7.0」となっています。もちろん、例えば「1.7」と「7.0」というのは同じものをさしていますので、そのつもりでバージョンの記述を読み取るようにしてください。
    
1. 開発環境の種類

    |名称|正式名称|説明|
    |:-:|:-:|:-:|
    |J2SE|Java 2 StandardEdition| 基本となるもので、開発および実行環境一式が揃っている。|
    |J2EE|Java 2 EnterpriseEdition|サーバ上でJavaプログラムを動かす機能等をJ2SEに追加したもの。
    |J2ME|Java 2 MobileEdition|携帯電話や携帯端末向けの組み込み用Java。|
    
    J2SEはJDKをどれかダウンロードしてインストールすれば、そこに入っています。J2EEは後に登場する「Tomcat」など、WEBサーバでJavaプログラムを動かすソフトウェアを導入すると手に入ります。J2MEは組み込み系の開発をやる時にしか触れないと思います。
    
1. JDK のことをどう呼ぶか

    |バージョン|呼び方|
    |:-:|:-:|
    |初期～1.1|JDK(Java Development Kit)|
    |1.2～1.4|J2SDK(Java 2 Software Development Kit)|
    |1.5～現在|JDK(Java Development Kit)|
    
    JDKとJ2SDKは同じもののことを言っていると思ってください。要はJavaでプログラムを作るために必要なキットのことです。
    
1. 「.Java」と「Java2」  
「Java」のことを「Java2」と呼ぶこともありますが、現状はこれら2つを明確に区別する必要はないです。Java1.1から1.2になった際、「Java」から「Java2」と呼称が変わったものの、以降バージョンアップを繰り返したにもかかわらず、この「2」がそのままになっているだけです。

#### 補足
「JDK」と「JRE」という2つの単語も似ていて分かりにくいですね。何の略語だったかおさらいしておきましょう。JDK…JavaDevelopmentKitJRE…JavaRuntimeEnvironment直訳するとJDK＝Java開発キットJRE＝Java実行環境となります。Javaでプログラムを作成し、実行するためにはコンパイルをした後、JVMで実行させる必要があることはここまでお話しました。JDKはその「プログラムをコンパイルするため」に必要です。一方、JREは「コンパイルされたプログラムを動作させるため」に必要です。JVMはJREに含まれています。
