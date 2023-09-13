+++
title = '技育CAMP_vol9'
date = 2023-09-12T05:50:57+09:00
draft = false
showToc=true
categories=["tech"]
tags=["ハッカソン","参加記"]
+++
# はじめに
9/9,10に[サポーターズの技育CAMPハッカソンvol.9](https://talent.supporterz.jp/geekcamp/)に参加してきたので参加記としてまとめようと思います。  
今回は即席チームとして参加し、Discordで通話しながらでの開発でした。
# 開発した作品
 ## 概要
ブックマークしたけど読んでないサイトを推しが通知してくれるWebアプリ「**Oshi remind**」を作りました。  
[![SuperUltraTsuyoTsuyoEngineerTeam/oshi-rimind-frontend - GitHub](https://gh-card.dev/repos/SuperUltraTsuyoTsuyoEngineerTeam/oshi-rimind-frontend.svg)](https://github.com/SuperUltraTsuyoTsuyoEngineerTeam/oshi-rimind-frontend)
  ### スクリーンショット
![chat](/img/技育CAMP_vol9/front_chat.png)
![chat](/img/技育CAMP_vol9/front_reading.png)
 ## 背景
 最初の話し合いで「作るなら日常の悩みからくるものが良いよね」となり、僕は技術記事を積読しちゃうことが結構あるので提案してみたところ、推しキャラと組み合わせる事になりました。
 ## 技術
  ### フロントエンド
  拡張機能、サイトにTypeScript,React,Next.js,tailwindcss
  ### バックエンド
  OpenAI(FineTuning),Python,django,docker
  ## 担当した部分
   拡張機能とリーディングリストの作成を担当しました。  
   TypeScript,React,Next.jsを使いました。すべて初めて触る技術だったので探り探りでしたがひとまず形にできてよかったです。  
   最初はJSとReactだけで書いていたのですが、色々あってJS→TS、React→React+Next.jsにしました。
  ## 開発手法
  タスク管理にGitHubのProjectsという機能を使いました。
  - Todoとしてissueを立てる
  - わかりやすいブランチ名でリモートリポジトリにプッシュ
  - そのブランチとissueを紐付ける
  - mainブランチにPRを作成
  - メンバーにレビューしてもらい、マージされることでissueが閉じる。

  Organizationはじめ、issueやPRなどのGitHub上での開発が初めてだったのでとてもいい経験になりました。
   ### Projectsとは？
   チーム開発でそれぞれのTODO,進捗状況を管理できるものです。  
   Table,Board,Roadmapがあり、今回はBoardを使いました。  
# 振り返り
 ## 結果
 残念ながら入賞することはできませんでした。  
 結構頑張ったので悔しいです。
 ## 苦労したこと
 React→React+Next.jsにするのが一番大変でした。  
 「React Next.js 置換」などで調べながら実装しようとしましたがうまく行かず、結局 ,`npx create-next-app`でいちから作り直しました。  
 `_document.tsx`,`layout.tsx`,`page.tsx`などNext.js特有のファイル構成を理解しないまま実装したので大変でした。  
 今後Next.jsも学んでいこうと思います。
 また、リーディングリストをデプロイできなかったのが反省です。  
 Next.jsでの置換がギリギリだったので今後はデプロイから逆算してスケジュール管理をしたいと思います。
 ## がんばったこと
 保存したいサイトで拡張機能を実行すると、そのサイトのタイトルとURLを取得してサーバーに送信するところに注力しました。  
 タイトル、URLはjson-serverを立てて管理しました。  
 サーバーとのやり取りにはAxiosというライブラリを使いました。
 それと、チームの他の方がファインチューニングを実装していて英語のドキュメントすら充実していない中、DiscordのOpenAIサーバーに入って質問していたりなどしていてすごいなと思いました。

# おわりに
 GitHubのProjectsでタスク管理することで開発の生産性がとても上がったのがすごく良かったです。  
 今までなあなあで開発してきましたが、今後は個人開発においても使っていこうと思います。（このブログでも使ってます）  

 来月の[技育CAMPキャラバン大阪](https://talent.supporterz.jp/events/6fc08c75-805e-4058-a811-77ac27d7f51e/?utm_source=next&utm_medium=geekcamp)にも参加するので、デプロイを目標に頑張っていこうと思います。