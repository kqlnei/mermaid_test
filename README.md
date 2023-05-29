# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid

graph LR
    Start(開始) --> Play(プレイ中)
    Play --> GameOver(ゲームオーバー)
    Play -->|ぷよ落下| ClearCheck(連鎖チェック)
    ClearCheck -->|連鎖あり| Chain(連鎖中)
    Chain -->|ぷよ消去| ClearCheck
    ClearCheck -->|連鎖なし| Play
    Chain -->|連鎖終了| Play
    ClearCheck -->|ぷよ積み上げ| Overstack(オーバースタック)
    Overstack -->|上部まで積み上げ| GameOver
```

## シーケンス図
### 条件
- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
    actor 太郎
    actor 花子
    太郎->>花子: おはよう！
    activate 花子
    花子-->>太郎: おはようございます!
    deactivate 花子
```

## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
```mermaid
classDiagram
    キャラクター o-- アイテム
```
