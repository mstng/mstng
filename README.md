# Hi, I'm Masato 👋

Engineering Manager @ dip Corporation  
Building tools with AI. Learning in public.

---

## 🚀 Projects

### 🔐 [Authentication Learning Lab](https://github.com/mstng/auth-learning-lab) — [repo](https://github.com/mstng/auth-learning-lab)
Password認証とSession認証を実際に動かし、**HTTP・Cookie・DBが何をどう保存するか**を目で追える学習アプリ。
「ログインすると何が保存される？」「次のアクセスでは何を送る？」「ログアウトすると何が消える？」
「ログアウト後も情報を見られる？」の**4つの問いを1画面ずつ**確かめる構成で、
各操作の前後でCookieの値とDBの件数を並べて比べられる。最後の401が正しい結果だと分かるところまで運ぶ。
DBは組み込みの**PGlite**をNode内で動かすので、Dockerも外部DBも要らず clone してすぐ起動できる。
仕事で扱うID基盤の理解を深めるために作った教材。デモは持たず、リポジトリが本体。
`Next.js` `TypeScript` `PGlite` `bcrypt` `Playwright`

---

### 📅 [トシガタリ](https://toshi-gatari.vercel.app) — [repo](https://github.com/mstng/toshi-gatari)
1950〜2026年の77年間を、1年ぶん1枚のカードで振り返る年表サイト。
世の中の流行まとめは「音楽は音楽だけ」とカテゴリ別に縦へ切られていることが多い。これを**年で横に切り直す**と、その年の空気が一度に立ち上がる——1998年を選べば、夜空ノムコウとタイタニックと長野五輪と「だっちゅーの」と、はがき50円が同じ画面に並ぶ。音楽・映画・ドラマ・アニメ・本・ゲーム・CM・流行語・ヒット商品・ファッション・食べもの・スポーツ・モノの値段・出来事の**14カテゴリ × 77年 = 約4,900項目**。
既存サイトからの転載はせず、オリコン年間ランキング・興行収入・新語流行語大賞・郵便料金の改定履歴などの公開記録から構成し直した。同時に**カテゴリごとの確度の差をREADMEに明記している**。年間ランキングのある音楽・映画と、公式記録が存在しないファッションやCMを、同じ顔で並べたくなかったため。
年代でページのアクセントカラーが変わり（50年代セピア→80年代ショッキングピンク→20年代ブルー）、生まれ年を入れるとその年の自分の年齢が出る。ビルド不要の静的サイト。
`HTML` `CSS` `JavaScript`

---

### 🥚 [デジタルモンスター 3D](https://digital-monster-play.masato-nahoo.chatgpt.site) — 本人限定公開
携帯育成玩具「デジタルモンスター」を3Dで再現した、非公式のブラウザ育成ゲーム。
**本体を回転させられる**ようにしてあり、3つのボタンで食事・特訓・掃除・睡眠を操作する。
タイミング特訓とターン制バトルを搭載し、**育て方に応じて進化が分岐する**。
育成データはブラウザ内に自動保存される。
実機ROMの忠実な再現ではなく、育成・バトルのルールは独自に調整したファン作品。
`React` `TypeScript` `Three.js` `Canvas` `Web Audio API` `localStorage`

---

### 🫀 [心臓のなか 3D](https://shinzou-real-3d.masato-nahoo.chatgpt.site) — 本人限定公開
心臓手術のあと、心臓の構造と血液の流れを立体で学ぶために作った3Dアトラス。
公開の解剖学データをもとに、**外観・断面・血流の3モード**で観察できる。
モデルの回転・拡大に加え、拍動の再生・停止と速度も操作できる。
2Dの「心臓のなか」を立体でやり直した一作。
`React` `TypeScript` `Three.js` `React Three Fiber`

---

### 📜 [三国志年代記](https://sangokushi-jin.masato-nahoo.chatgpt.site/)
黄巾の乱（184年）から東晋の終焉（420年）まで、三国志**とその後**を12章でたどるインタラクティブ年表。
51人の人物録と12の合戦録を収録し、人物・合戦・王朝のつながりを行き来しながら読める。
**史実と『三国志演義』の違い**も明示してある。物語が終わったあとの歴史まで含めたのが狙い。
`React` `TypeScript` `データ可視化`

---

### 🏛️ [もしも闘技場](https://moshimo-arena.vercel.app) — [repo](https://github.com/mstng/moshimo-arena)
時代も分野も違う偉人16人を、一騎討ち・会戦・謀略戦・発明レース・人心掌握・天下取りという共通の土俵に乗せて戦わせる対戦シミュレータ。信長とナポレオンが天下を争ったら、呂布とニュートンが発明を競ったら——を数値で出す。
同種の企画は「AIに聞いて答えを出す」形が多いが、**これは実行時にAIを呼ばない**。判定はすべてコードで完結し、**根拠を全部画面に出す**。データ自体はClaude Codeと一緒に作っており、その数値に入っていたAIの評価のクセこそが、この作品の見どころになった（後述）。16人×6ステータス＝96個の数値すべてに、史実に基づく根拠を1行添えてある。乱数を使わないので同じ組み合わせなら結果は常に同じ。
数値そのものは作者の主観である。それを隠さず晒して**読者が反論できる形にする**ことが設計の目的で、土俵ごとに重みが変わるため同じ2人でも土俵次第で勝敗が入れ替わる。
初版ではジャンヌ・ダルクだけがどの土俵でも勝率50%を超えなかった。原因は土俵ではなくデータ側で、作者が**「カリスマ」と「実績による威光」を混同**し、有名な征服者に軒並み90台をつけていたためだった。軸の定義を「その人望は、勝ったからついてきたのか、勝つ前からあったのか」に絞り直して16人を再評価している。このときバランスを取るためにジャンヌの数値を上げる修正はしていない——土俵（ルール）は作者が決めてよいが、人物（事実の解釈）をゲームの都合で動かせば根拠を公開する意味そのものが失われるため。経緯はREADMEに残した。
`HTML` `CSS` `JavaScript` `node:test`

---

### 🔐 [認証の歴史](https://mstng-portfolio.vercel.app/works/auth-history.html)
1961年のMIT CTSSから現在のパスキーまで、認証技術65年を**「破られては、作り直されてきた」因果**で並べた年表。
共有秘密・Webセッション・企業SSO・権限委譲・パスワードレスの5世代が、置き換わるのではなく**消えずに積み重なっている**様子と、パスワードハッシュ・多要素認証の2つの系譜を1枚にまとめた。
ID基盤の仕事で使うOAuth/OIDC学習の補助資料として作成。フレームワークなしの静的HTML1ファイル。
`HTML` `CSS`

---

### 🚀 [星よけダッシュ](https://browser-game-phi-orcin.vercel.app) — [repo](https://github.com/mstng/star-dodge)
宇宙船を左右に動かし、落ちてくる流星を60秒間避け続けるアクションゲーム。
15秒ごとにレベルが上がり（最大4）、後半は流星の速度と密度が上がる。
ゲームロジックをUI描画から切り離し、衝突判定・難易度・スコア計算を`node:test`で4件検証。
**AIエージェント（Codex）に設計から実装まで一任した**実験作。キーボード＋タッチ操作対応。
`JavaScript` `ES Modules` `node:test`

---

### 🫀 [心臓のなか](https://shinzou-no-naka.vercel.app) — [note](https://note.com/mstng/n/nbca80885b6de)
自分自身の心臓手術をテーマに、心臓内の血流を**止めて・巻き戻して・コマ送りで**追える可視化。
一番見せたい相手は家族なので、医学知識ゼロでも分かることを最優先にした。
全4章のうち公開しているのは第1・2章まで（第3・4章の内容はnoteの続編記事にまとめた）。
`HTML` `CSS` `JavaScript`

---

### ⚔️ [rpg-kit](https://rpg-kit-topaz.vercel.app) — [repo](https://github.com/mstng/rpg-kit)
19日以内に20階の底のドラゴンを倒す、ターン制コマンドバトルの「型」。
作りながら二度「単調だ」という壁にぶつかり、二度とも同じ直し方をした——**選択肢を足すのではなく、先の情報を1つ開示する**。
戦闘には敵の大技予告（予告ターンは敵が攻撃してこない＝まるごと選択時間になる）、潜行には下の階の予兆（同じHP4割でも、けはいなら帰り、金属音なら潜る）を入れた。
ロジックを描画から切り離してあるので、「HPが◯%を切ったら帰る」を総当たりして勝率カーブを描き、**一度おぼえたら終わりの正解が存在しないこと**を数字で確かめられる（固定最強55.4%に対し状況適応76.2%）。
途中で「進捗を戻す」と「成長を奪う」を同時に入れて回復不能な詰みを作った失敗もREADMEに残してある。
`JavaScript` `HTML` `CSS`

---

### 🧬 [言語系譜](https://gengo-keifu.vercel.app) — [repo](https://github.com/mstng/gengo-keifu)
FORTRAN(1957)からZig(2016)まで、主要60言語の「誰が誰に影響を与えたか」を1枚の家系図にした読み物。
言語をクリックすると祖先と子孫だけが浮かび上がり、その言語が**いま何を動かしているか**（COBOLは銀行の勘定系、Selfは実用ゼロだがJIT技術がV8とHotSpotに直結、など）まで読める。影響線は106本。
GIGAZINE(2007)が紹介していた Éric Lévénez の約2500言語の系統図が元ネタ。そこから主要60言語を抜き出し、影響関係を自前で整理し直した。
データの原本はPython側に置いて index.html を生成する一方通行にし、列の衝突・孤立ノード・親子の年順をテストで検出する構成にしている。
`HTML` `CSS` `JavaScript` `SVG` `node:test` `Python`

---

### 🏢 [開発会社物語](https://kaihatsu-monogatari.vercel.app) — [repo](https://github.com/mstng/kaihatsu-monogatari)
小さな開発会社を経営するシミュレーション。案件を受け、技術を選び、社員を育てて会社を続けていく。
ジャンル×技術の21通りの相性が隠されていて、当たりを引くと数字が跳ねる。一度試した組み合わせは記録され、次に活きる。
カイロソフト『ゲーム発展国』の骨格をお借りしたオマージュ（借りたのは仕組みと様式まで。固有の表現は不使用）。
放置ゲーとPMシムを2本外したすえに「増える・育つ」と「判断」の両方が要ると分かって作った4本目で、その過程はREADMEに残してある。
`JavaScript` `ES Modules` `node:test`

---

### 🌳 [idle-kit（そだつ）](https://idle-kit.vercel.app) — [repo](https://github.com/mstng/idle-kit)
放置育成ゲームの「型」。遊べる完成品ではなく、次にちゃんとした放置ゲーを作るときそのまま流用できる参考実装として書いた。
実時間tick・オフライン進行・指数コスト曲線・転生・巨大数対応・オートバイヤー・バランスシミュレータまでを依存パッケージゼロで実装。ルールを純粋関数に閉じたので、数日ぶんのプレイを0.2秒で早送りして設計の欠陥を洗い出せる。12の型それぞれに「なぜそう作ったか」と実際に失敗して直した記録をREADMEに残している。
`JavaScript` `ES Modules` `PWA` `node:test`

---

### 🕰️ [いくらだったの？](https://ikura-datta.vercel.app) — [repo](https://github.com/mstng/ikura-datta)
明治8年〜2024年の物価で日本を時間旅行するミニアプリ。年代当てクイズ・任意の年の物価探索・生まれ年の物価カード共有の3モードで遊べる。
品目の登場年管理・銭/厘表示・対数の推移グラフつき。主要系列は総務省CPI・値段史などの公開統計で裏取り（その他は概算と明記）。
`HTML` `CSS` `JavaScript` `Canvas` `SVG` `Web Audio API`

---

### 📱 [こころのホーム画面メーカー](https://kokoro-home.vercel.app) — [repo](https://github.com/mstng/kokoro-home)
名前を入れると、あなたの関心事がスマホのホーム画面（アプリアイコン＋通知バッジ）として並ぶ可視化トイ。推し活・課金・締切・承認欲求…を可視化してスクショ感覚でシェアできる。
2007年『脳内メーカー』を「頭の中→スマホのホーム画面」に翻訳した令和版オマージュ（同作・特定OSの素材は不使用）。
`HTML` `CSS` `JavaScript` `Canvas` `Web Audio API`

---

### 📜 [ぼうけんのしょメーカー](https://boken-no-sho.vercel.app) — [repo](https://github.com/mstng/boken-no-sho)
状況質問で性格を診断し、入力した名前で隠しステータスが変わる冒険者キャラシート生成トイ。「なまえを変える」と答えはそのままに能力値だけ変わる。
『ドラゴンクエストIII』(1988)の性格診断と、名前で成長率が変わる隠し仕様に着想を得たオリジナル・オマージュ（同作のブランド・素材は不使用）。
`HTML` `CSS` `JavaScript` `Web Audio API`

---

### 💬 [ELIZA 令和版](https://eliza-puce.vercel.app) — [repo](https://github.com/mstng/eliza)
見た目は今どきのAIチャット、中身は1966年生まれの会話ボット「ELIZA」のルールエンジン。キーワード照合とオウム返しだけで"会話している感"を出す。
右上の「タネあかし」で緑のターミナル（1966モード）に反転し、AIではないと明かされる。占いトイ三部作（振る/書く/話す）の締め。
`HTML` `CSS` `JavaScript`

---

### 🌀 [MASH らくがき未来占い](https://mash-pearl-xi.vercel.app) — [repo](https://github.com/mstng/mash)
紙とペンの未来占い「MASH」の令和版。候補を書いて、うずまきを長押しして運命の数を決めると、消去ループで住まい・結婚相手・仕事…があなたの未来として確定する。
効果音はWeb Audioで合成、キーボード操作にも対応。八球オラクルの型を流用した占いトイ2作目。
`HTML` `CSS` `JavaScript` `Web Audio API` `Canvas`

---

### 🎱 [八球オラクル](https://eightball-rho.vercel.app) — [repo](https://github.com/mstng/eightball)
問いを胸に球をふると、7人の占い師（老賢者・ギャル・毒舌・母・関西商売人・中二病・AI執事）が口調を変えてお告げを返す、令和版マジック8ボール。
お告げは「バーナム効果＋問いの語ひろい＋ちょい毒」の3段生成。吉凶で球が発色し、Web Audioでドラムロール、吉なら紙吹雪。1ファイル完結。
`HTML` `CSS` `JavaScript` `Web Audio API` `Canvas`

---

### 🧭 [マンダラチャート](https://mandala-chart-umber.vercel.app) — [repo](https://github.com/mstng/mandala-chart)
9×9マス（大谷選手の目標シート形式）の目標達成シートを作れるWebアプリ。ログイン不要で開いてすぐ書け、撮影・印刷で持ち出せる。ミラーセルは同期処理なしで自動連動する設計。  
`Next.js` `TypeScript` `Tailwind CSS` `Zustand` `Supabase`

---

### 🦁 [がおがお](https://gaogao-chi.vercel.app) — [repo](https://github.com/mstng/gaogao)
2〜3歳向けの知育PWA。ライオン「がお」と、ことば・かず・いろ・おと であそぶ。  
まだ文字が読めない娘のために、絵と音声だけで指1本で遊べるように作った。  
`Next.js` `TypeScript` `Zustand` `PWA` `Web Speech`

---

### 🗼 [デスマーチ・スパイア](https://deathmarch-spire.vercel.app) — [repo](https://github.com/mstng/deathmarch-spire)
エンジニアの開発現場をテーマにしたデッキ構築ローグライク。バグや仕様変更を倒し、リリースの頂を目指す。企画からリリースまで1日で作った初のゲーム作品。  
`JavaScript` `HTML` `CSS`

---

### 🌐 [Web タイムマシン](https://web-timemachine.vercel.app) — [repo](https://github.com/mstng/web-timemachine)
1994〜2023年、Webデザインの歴史を8つの時代で体験できるインタラクティブサイト。  
当時のニュースを、当時のデザインで読む。  
`HTML` `CSS` `JavaScript`

---

### 🎯 [Manager Type Quiz](https://manager-type-quiz.vercel.app) — [repo](https://github.com/mstng/manager-type-quiz)
10問の質問に答えて、あなたのマネジメントスタイルに最も近い歴史上の人物を診断するクイズ。  
`Next.js` `TypeScript` `Vercel`

---

### 💬 [Moyan（もやん）](https://moyan-ten.vercel.app) — [repo](https://github.com/mstng/moyan)
匿名でお悩みを投稿し、共感で繋がるボード。  
`Node.js` `Express` `Supabase` `Vercel`

---

### 🌱 [ことのめ](https://kotonome.vercel.app)
子どもの言葉を記録するモバイルファーストPWA。「きゅうきゅうしゃ」を忘れたくなくて作った。  
`Next.js` `TypeScript` `shadcn/ui` `PWA`

---

### 🗳️ [Vote Live](https://github.com/mstng/vote-live) — [repo](https://github.com/mstng/vote-live)
チームミーティングで使えるリアルタイム匿名投票ツール。URLを共有するだけで賛成/反対/保留を即時集計。  
`Node.js` `WebSocket` `JavaScript`

---

### 📚 [三国志歴史図鑑](https://sangokushi-zukan.vercel.app/) — [repo](https://github.com/mstng/sangokushi-zukan)
好きが高じてAIと作った、武将1776人の歴史図鑑。Wikidataから人物データを取得し、
タイムライン・相関図・戦場マップ・物語を横断できる。
人物データの生成からビジュアルまでAIと分業した、**物量勝負**の一作。
`HTML` `CSS` `JavaScript` `AI生成コンテンツ`

---

### 📈 [EngGrowth](https://eng-growth.vercel.app/) — [repo](https://github.com/mstng/eng-growth)
エンジニアスキルを**5カテゴリ22項目**のレーダーチャートで可視化する成長記録ツール。
サーバーを持たずLocalStorageに保存するので、ログインなしで開いてすぐ書ける。
`D3.js` `JavaScript` `LocalStorage`

---

### 🎮 [Gamemory](https://gamemory-cyan.vercel.app/)
プレイしたゲームを記録・振り返りできるアプリ。RAWG APIからタイトル情報を引いてくる。
`Next.js` `Supabase` `RAWG API`

---

### 🏢 [野口装飾 コーポレートサイト](https://noguchi-soshoku.vercel.app/)
実在する内装業のコーポレートサイトを、設計から公開まで担当した。
**実案件**としてのヒアリングと要件整理も含む。作って終わりではない一件。
`Next.js` `Tailwind CSS` `Vercel`

---

### 🍾 ながしびん — 開発中
匿名のメッセージをボトルに入れて流し、誰かが拾うサービス。Phase1まで完了。
`Node.js` `Supabase`

---

### 🧪 [mstng-lab](https://github.com/mstng/mstng-lab) — [repo](https://github.com/mstng/mstng-lab)
AIチームと一緒に学習・実験・アウトプットするリポジトリ。  
`HTML` `CSS` `JavaScript`

---

## 🛠️ Tech Stack

![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Next.js](https://img.shields.io/badge/-Next.js-000000?style=flat&logo=next.js&logoColor=white)
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Supabase](https://img.shields.io/badge/-Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat&logo=vercel&logoColor=white)

---

*Engineering Manager with 15+ years in the industry. Currently exploring AI-augmented development.*
