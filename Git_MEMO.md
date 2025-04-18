# Git学習メモ
## Git Commands

- Create local repository
    - git init
- ファイルの状態を確認
    - git status

- Python 100Day Challenge Notes
    Day 1: 課題：四則演算プログラム
    Day 2: 課題：数当てゲーム
    Day 3: 課題：簡単な計算機 (Simple Calculator)
    Day 4: 単語カウンター
    Day 5: To-Do List アプリ (コンソール版)
    Day 6: Rock, Paper, Scissors Game
    Day 7: FizzBuzz Game
    Day 8: タイマーアプリ（シンプルなコンソールタイマー）

# Githubでの管理の仕方
# 0. Terminalでディレクトリに移動（cd Documents/Python/100project_challenge/Dayxx）
# 1. ファイル追加 or 修正
# 2. ステージング
git add .

# 3. コミット（メッセージは分かりやすく）
git commit -m "Add Day009: タイトルなど"

# 4. プッシュしてGitHubへアップ
git push origin main

# ローカル → GitHub に初回アップロードする手順
ローカルに次のようなフォルダがあるとします（例：SleekFavorites/）：
ステップ1：Gitの初期化（※まだしてなければ）
cd SleekFavorites
git init
ステップ2：ファイルをGitに追加
git add .
git commit -m "Initial commit"
ステップ3：GitHub上に空のリポジトリを作成
GitHub上で以下のようにリポジトリを作成（例：SleekFavorites）
作成時は「README.mdの自動追加」などをせず、完全に空の状態で作成するとスムーズです。
ステップ4：リモートリポジトリを登録してPush
git remote add origin https://github.com/あなたのユーザー名/SleekFavorites.git
git branch -M main  # メインブランチ名をmainにする
git push -u origin main
これで、ローカル → GitHub に初回アップロード完了！ 
② 今後の連携（commit → push）
1.	ローカルで変更したら：
git add .
git commit -m "変更内容の説明"
git push origin main
2.	GitHubから変更を取り込むときは：
git pull origin main

# .DS_Storeをアップロードしないようにするには
対処法：.DS_StoreをGitの追跡対象から除外する
① .gitignore ファイルに追記（推奨）
プロジェクトルートに .gitignore ファイルを作成または編集して、以下を追加：
.DS_Store
② すでにコミットされている.DS_Storeを削除
git rm --cached .DS_Store
git commit -m "Remove .DS_Store from tracking"
git push

# ✅ .gitignore に .DS_Store を追加する手順（VSCode編）
🪜 ステップ①：プロジェクトのルートを開く
	•	すでにプロジェクト（例：SleekFavorites/）をVSCodeで開いている状態でOK！
🪜 ステップ②：.gitignore ファイルを作成（または開く）
	•	左のエクスプローラーでルートフォルダを右クリック →
New File（新しいファイル） → ファイル名を .gitignore として作成
※すでに .gitignore ファイルが存在する場合は、それを開いて編集でOK
🪜 ステップ③：以下を .gitignore に追記して保存
# macOS 用: Finderの設定ファイル
.DS_Store
他にも不要なものがあれば追記できます（例：node_modules/ や dist/ など）
🧹 ステップ④：すでにGitで追跡されている .DS_Store を除外（1回だけ必要）
git rm --cached .DS_Store
git commit -m "Remove .DS_Store from tracking"
git push

# ターミナルの移動方法
cd ~/Documents/PythonApps/SleekFavorites
ポイント：
	•	~ を使うとホームディレクトリに一発で移動できます
	•	スペースを含む場合は \ を使うか、"で囲む


# Pythonを仮想環境で使う手順
おすすめの安全な方法：仮想環境（venv）を使う
仮想環境はPythonでの開発の定番スタイルで、システム環境を汚さず、安全にパッケージをインストールできます。
ステップ①：仮想環境を作成
--> VSCodeだと、command + Shift P --> Python Select Interpreter --> Create Virtual Environmentで仮想環境構築できるっぽい？
ターミナルで、作業用ディレクトリを作成して移動します：
例
mkdir flet_project
cd flet_project
そして仮想環境を作成：
python3 -m venv venv
ステップ②：仮想環境を有効化
source venv/bin/activate
すると、プロンプトがこう変わるはず：
(venv) yourname@MacBook ~ %
ステップ③：fletをインストール
pip install flet
ステップ④：確認
python3 -c "import flet; print('Flet is installed successfully!')"
which python3でpyenv...などの仮想環境が選択されているかチェックする

# プロンプト用
今回の記事に関して以下の点について、コメントがあればお願いします！
# 感想をお願いします！
# 表現の代替案や言い換えなどを提示
# 文章の流れや言葉遣いについて改善案があれば提示
# さいごに、次回以降の題材の提案（以下がこれまでのリストですので、参考にしてください）
────────────────
- Blog 100day challenge lists
    Day1: 最近、こころが動いた瞬間
    Day2: 最近、ちょっと成長したなと思ったこと
    Day3: 最近、ちょっとしたことで笑ったこと
    Day4: 日常の中で「贅沢だな」と思った瞬間
    Day5: 最近「これ、意外といいな」と思ったこと
    Day6: 「これ、子どもの頃と変わらないな」と思ったこと
    Day7: 「これって、自分だけ？」と思うこと
    Day8: ルーティン化していること
    Day9: この感覚、なんて言うんだろう？
    Day10: なぜか好きなもの
    Day11: 昔は苦手だったけど、今は好きになったもの
    Day12: これがないと落ち着かないもの
    Day13: 無性に食べたくなるもの
    Day14: やめようと思っても、ついやってしまうこと
    Day15: 最近なんとなく気になっていること
    Day16: ちょっとした日課
    Day17: 気になっているけど、まだ試していないこと
    Day18: 最近ちょっと変わった習慣
    Day19: 最近見つけたお気に入りの小さな幸せ
    Day20: 一日の終わりに感じる小さな幸せ
    Day21: 最近、ちょっと嬉しかったこと
    Day22: 子どもの頃に夢中になったもの
    Day23: 自分にとっての ‘心が落ち着く時間’
    Day24: 最近感動したこと
    Day25: 好きな香り
    Day26: 自分にとっての贅沢な時間 
    Day27: つい後回しにしてしまうこと
    Day28: 最近、自分に対して ‘よくやった’ と思ったこと
    Day29: なんとなく ‘これが私っぽい’ と思う瞬間
    Day30: ふとした瞬間に感じる ‘大人になったな’ と思うこと
    Day31: 子どもの頃に思い描いていた ‘大人’ ってどんな存在だった？
    Day32: 最近、つい見入ってしまったもの
    Day33: 最近「なんだか気持ちがほっとしたな」と思った瞬間
    Day34: 最近「ちょっとしたご褒美」になったこと
    Day35: 昔は理解できなかったけど、今ならわかること
    Day36: ちょっとしたことでやる気が出た瞬間
    Day37: 自分だけの ‘こだわり’
    Day38: なんだか今日は冴えてるかも？と思った日
    Day39: 最近 ‘これって大人の余裕かも’ と思ったこと
    Day40: あのときの ‘なんとなくの選択’ が意外と良かった話
    Day41: 最近、昔の自分なら驚くようなことをした話
    Day42: ちょっと昔の自分に伝えたいこと
    Day43: これって私の ‘ちょっとした美学’ かも？と思う瞬間
    Day44: 最近『あ、こういうの大事だな』と思った瞬間
    Day45: 最近、ちょっとだけ見方が変わったもの
    Day46: 最近、誰かの言葉でハッとしたこと
    Day47: ふとした瞬間に ‘あ、今この瞬間好きだな’ と思ったこと
    Day48: 過去の自分にちょっとだけ謝りたいこと
↓こちらが今回の記事です。↓
────────────────

