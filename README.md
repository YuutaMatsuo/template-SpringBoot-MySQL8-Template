# 1.環境
- IDE: VScode
- Java: eclipse-temurin:17-jdk
- MySQL: mysql8

## SpringBoot + MySQL8 開発テンプレート
SpringBootとMySQLを用いたWebアプリ開発用テンプレートです
workspaceディレクトリにあるsampleプロジェクトはbuild確認用のサンプルの為、必要に応じて新規プロジェクトを作成してください

# 2.手順(VSCode)
  ## 2-1 MySQLの環境変数を設定する
  docker/mysql/.envファイルを開きユーザーやルートパスワードなどの環境変数を設定する

  ## 2-2 springプロジェクトの作成
  [spring initializr](https://start.spring.io/) からSpring Bootプロジェクトを作成し、workspaceにコピーする
  <dl>
  <dt>ビルドツール</dt>
  <dd>Gradle</dd>
  <dt>バージョン</dt>
  <dd>Java:17</dd>
  <dd>Spring Boot: お好みで</dd>
  <dt>圧縮後の拡張子</dt>
  <dd>Jar</dd>
  <dt>依存関係</dt>
  <dd>Spring Boot DevTools</dd>
  <dd>Lombok</dd>
  <dd>Thymeleaf</dd>
  <dd>Spring Web</dd>
  <dd>Spring Data JPA</dd>
  <dd>MySQL Driver</dd>
  <dd>など必要なライブラリを選択</dd>
  </dl>

  ## 2-3 application.propertiesにデータベースの環境を追加
  ``````src/main/resources/application.properties
  spring.datasource.driverClassName=com.mysql.cj.jdbc.Driver
  spring.datasource.url=jdbc:mysql://mysql:3307/環境変数で設定したdatabase名
  spring.datasource.username=環境変数で設定したuser名
  spring.datasource.password=環境変数で設定したpassword
  ``````

  ## 2-4 VSCodeのdevcontainerからコンテナにアクセスする
  vscode左下のリモートアクセスからコンテナを再度開くを選択する事で、自動的にdockerコンテナがビルドされる


# 2.手順(Eclipse)
  ## 2-1 制作中


