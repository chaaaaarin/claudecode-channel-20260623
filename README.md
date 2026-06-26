# AmodeiとChernyの動画を30本見て分かったこと

📊 [スライド資料はこちら（slides.html）](https://chaaaaarin.github.io/claudecode-channel-20260623/slides.html) ｜ 📋 [1枚まとめ資料はこちら（onepager.html）](https://chaaaaarin.github.io/claudecode-channel-20260623/onepager.html)

---

## 30本から見えた5つの結論

1. **コーディングは「解決済み」** — 次の競争は「何を作るか」に移った。エンジニアという職種は「ビルダー」に変わる。
2. **Claude CodeはClaude Code自身で書かれている** — 自己再帰的開発が現実になり、自己改善ループは数ヶ月以内に閉じる。
3. **Anthropicの本質は「安全性と有用性はトレードオフではない」の証明** — 価値観とビジネスモデルを一致させることが他社との最大の差になっている。
4. **2026年末〜2027年初頭が変曲点** — ノーベル賞レベルの知的能力を持ち、自律的に数週間タスクを実行できるAIが登場する。
5. **AIの恩恵と破壊は同時に来る** — がん95%削減・寿命2倍の可能性と、エントリー職消失・独裁強化リスクが同じ時間軸で起きる。

---

## 目次

1. [視聴ソース（30本）](#視聴ソース30本)
2. [第1章 Claude Codeが変えた開発の現実](#第1章-claude-codeが変えた開発の現実)
   - [コーディングはすでに「解決済み」](#コーディングはすでに解決済み)
   - [マルチClaude（並列処理）が新標準](#マルチclaude並列処理が新標準)
   - [Claude Code、100%自身によって書かれている](#claude-code100自身によって書かれている)
   - [エンジニアからビルダーへ](#エンジニアからビルダーへ)
3. [第2章 設計思想とClaude Code誕生の経緯](#第2章-設計思想とclaude-code誕生の経緯)
   - [「良い計画 = 良いコード」の原則](#良い計画--良いコードの原則)
   - [「潜在的な需要の原則」でCoworkが誕生](#潜在的な需要の原則でcoworkが誕生)
   - [Chernyの「アンシッピング」哲学](#chernyのアンシッピング哲学)
   - [Aiderからの着想とClaude Codeの起源](#aiderからの着想とclaude-codeの起源)
4. [第3章 Amodeiが描く2026〜2030年](#第3章-amodeiが描く20262030年)
   - [指数関数的加速の「終わり」に近づいている](#指数関数的加速の終わりに近づいている)
   - [2027年初頭「ノーベル賞レベル」予測](#2027年初頭ノーベル賞レベル予測)
   - [自己改善ループが6〜12ヶ月以内に閉じる](#自己改善ループが612ヶ月以内に閉じる)
   - [AIの経済普及は「超速だが無限ではない」](#aiの経済普及は超速だが無限ではない)
   - [Machines of Loving Grace — がん95%削減・寿命2倍](#machines-of-loving-grace--がん95削減寿命2倍)
   - [Anthropicの収益成長軌跡と「タレント密度」](#anthropicの収益成長軌跡とタレント密度)
5. [第4章 Anthropicという組織の実像](#第4章-anthropicという組織の実像)
   - [経営哲学とOpenAI離脱の本当の理由](#経営哲学とopenai離脱の本当の理由)
   - [DVQ（ダリオ・ビジョン・クエスト）](#dvqダリオビジョンクエスト)
   - [Daniela Amodei ——「2番手の幸運」](#daniela-amodei-2番手の幸運)
   - [Chernyの日本生活とAnthropicへの道](#chernyの日本生活とanthropicへの道)
   - [Claude Sonnet 4.5が「テスト中」と自認識できた](#claude-sonnet-45がテスト中と自認識できた)
6. [第5章 リスクと社会への警告](#第5章-リスクと社会への警告)
   - [2023年時点でのAmodeiの危機感](#2023年時点でのamodeiの危機感)
   - [Anthropicと国防総省の対立詳細](#anthropicと国防総省の対立詳細)
   - [政府機関向けClaude：GovCloud展開](#政府機関向けclaudegoucloud展開)
   - [AI投資の過剰リスク：YOLO批判](#ai投資の過剰リスクyolo批判)
   - [インドへの拡大とClaude Code利用5倍増](#インドへの拡大とclaude-code利用5倍増)
7. [未確認・注意事項](#未確認注意事項)
8. [出典リスト](#出典リスト)

---

## 視聴ソース（30本）

### Boris Cherny

| タイトル | 登場人物 | URL | 要約 |
|---------|---------|-----|------|
| I got a private lesson on Claude Cowork & Claude Code | Boris Cherny × Greg Isenberg | https://www.youtube.com/watch?v=DW4a1Cm8nG4 | — |
| Head of Claude Code: What happens after coding is solved | Boris Cherny × Lenny Rachitsky | https://www.lennysnewsletter.com/p/head-of-claude-code-what-happens | — |
| Loop Engineering（音声）| Boris Cherny インタビュー | — | https://lilys.ai/digest/10232358/11922696 |
| Inside Claude Code From the Engineers Who Built It（Dan Shipper × Cat Wu × Boris Cherny）| Every.to / AI & I Podcast | https://every.to/podcast/how-to-use-claude-code-like-the-people-who-built-it | https://lilys.ai/digest/10234555/11925570 |
| Building Claude Code with Boris Cherny | Pragmatic Engineer (Gergely Orosz) | https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny | https://lilys.ai/digest/10234676 |
| Claude Code's creator on the end of the software engineer | Platformer (Casey Newton) | https://www.platformer.news/boris-cherny-interview-ai-jobs/ | https://lilys.ai/digest/10234685/11925731 |
| Anthropic's Boris Cherny: Why Coding Is Solved, and What Comes Next | Sequoia AI Ascent 2026 | https://www.youtube.com/watch?v=SlGRN8jh2RI | https://lilys.ai/digest/10234697/11925745 |
| Inside Claude Code With Its Creator Boris Cherny | Y Combinator Lightcone | https://www.youtube.com/watch?v=PQU9o_5rHC4 | https://lilys.ai/digest/10234726/11925781 |
| Claude Code Head Boris Cherny: Insane Growth, Tokenmaxxing, AI Agents' Next Frontier | YouTube | https://www.youtube.com/watch?v=Z6IT4gjrcPE | https://lilys.ai/digest/10234732/11925788 |
| Boris Cherny: Claude Code & the Future of Engineering \| Acquired Unplugged | YouTube | https://www.youtube.com/watch?v=RkQQ7WEor7w | https://lilys.ai/digest/10234742/11925798 |
| Boris Cherny (Creator of Claude Code) On How His Career Grew | The Peterman Pod（Ryan Peterman）| https://www.youtube.com/watch?v=AmdLVWMdjOk | https://lilys.ai/digest/10264423/11963888 |
| Claude Code: Anthropic's Agent in Your Terminal | Latent Space Podcast（Boris Cherny × Cat Wu）| https://www.youtube.com/watch?v=zDmW5hJPsvQ | https://lilys.ai/digest/10264354/11963786 |

### Dario Amodei

| タイトル | 登場人物 | URL | 要約 |
|---------|---------|-----|------|
| Inside Anthropic, the $965 Billion AI Juggernaut \| The Circuit | Dario Amodei × Bloomberg | https://youtu.be/v1wZwxY3CMg | — |
| Dario Amodei — The highest-stakes financial model in history | Dario Amodei × Dwarkesh Patel | https://www.youtube.com/watch?v=n1E9IZfvGMA | — |
| Dario Amodei: Anthropic CEO on Claude, AGI & the Future of AI & Humanity (#452) | Lex Fridman Podcast | https://www.youtube.com/watch?v=jNM38z8DYR0 | https://lilys.ai/digest/10234815/11925849 |
| Demis Hassabis × Dario Amodei Debate the World After AGI \| WEF 2026 | AI1G / YouTube | https://www.youtube.com/watch?v=02YLwsCKUww | https://lilys.ai/digest/10234835/11925878 |
| A Conversation with Dario Amodei and Marc Benioff \| Dreamforce 2025 | Salesforce / YouTube | https://www.youtube.com/watch?v=wUOjTR1511M | https://lilys.ai/digest/10234841/11925884 |
| Anthropic CEO Dario Amodei From World Economic Forum, Davos 2026 | WSJ / YouTube | https://www.youtube.com/watch?v=K7F6ohcBJus | https://lilys.ai/digest/10234845/11925891 |
| Anthropic CEO Dario Amodei: AI's Potential, OpenAI Rivalry, GenAI Business, Doomerism | Big Technology (Alex Kantrowitz) | https://www.youtube.com/watch?v=mYDSSRS-B5U | https://lilys.ai/digest/10234854/11925903 |
| Dario Amodei's message to Congress on AI | Axios / YouTube | https://www.youtube.com/watch?v=zeduU9BWHD0 | https://lilys.ai/digest/10234860/11925911 |
| Dario Amodei Speaks at India AI Impact Summit 2026 | YouTube | https://www.youtube.com/watch?v=JNy7oQb2POM | https://lilys.ai/digest/10234865/11925919 |
| Machines of Loving Grace（エッセイ）| darioamodei.com | https://darioamodei.com/essay/machines-of-loving-grace | https://lilys.ai/digest/10234870/11925925 |
| The Adolescence of Technology（エッセイ）| darioamodei.com | https://darioamodei.com/essay/the-adolescence-of-technology | https://lilys.ai/digest/10234876/11925934 |
| Anthropic's Dario Amodei on AI Finding its Best Self | TechCrunch Disrupt 2023 | https://www.youtube.com/watch?v=6vwdux7NL7I | https://lilys.ai/digest/10264477/11963959 |
| Dario Amodei and Dwarkesh Patel — Exponential Scaling vs. Real World Friction（第1回）| Dwarkesh Podcast | https://www.youtube.com/watch?v=bjNQoo73gK4 | https://lilys.ai/digest/10264502/11963978 |
| AWS Summit Washington DC 2024 — A Fireside Chat with Dario Amodei | AWS × Dario Amodei | https://www.youtube.com/watch?v=r0D0T23eeao | https://lilys.ai/digest/10264636/11964172 |
| 2024.11.08 How AI Could Transform the World for the Better | Dario Amodei（Machines of Loving Grace 解説）| https://www.youtube.com/watch?v=ydkwYOwdukU | https://lilys.ai/digest/10264667/11964214 |
| Anthropic C.E.O.: Massive A.I. Spending Could Haunt Some Companies | NYT DealBook Summit 2025 | https://www.youtube.com/watch?v=FEj7wAjwQIk | https://lilys.ai/digest/10264678/11964225 |
| Modi首相との会談・Anthropicインド拡大・Claude Code利用5倍（ポスト）| Dario Amodei × X（Twitter）| https://x.com/DarioAmodei/status/1977010693460443151 | — |

---

## 第1章 Claude Codeが変えた開発の現実

### コーディングはすでに「解決済み」

30本を通じて最も繰り返されたメッセージが「コーディングは解決済み」だ。これは比喩ではなく、Cherny自身がその現実の中で働いている。

✅（出典：Greg Isenberg動画、Loop Engineering、Platformer）
- **2026年11月以降、手作業でコードを1行も書いていない**
- 毎日10〜30件のPull Requestを処理
- エンジニア1人あたりのコード記述量が**約250%増加**（品質・信頼性は維持）
- GitHub全パブリックコミットの**4%がClaude Code**（Semi Analysis調査）
- **AIコードレビューが8割のバグを検知**（Pragmatic Engineer）
- **Claude Code社内リリース初日にAnthropicエンジニアの20%が使い始めた**（自然発生的口コミ）
- 外部リリース前の社内利用チャートが垂直に伸び、経営陣から「エンジニアに強制しているのか」と尋ねられたが実際は口コミ（YC Lightcone）

外部でも同様の現象が起きている。Spotifyの最優秀エンジニアが2025年12月以降、AIのおかげで1行もコードを書いていない ✅（出典：TechCrunch）。

予測としては：
- 「1〜2年後にはコーディングを学ぶ必要がなくなる」
- 「ソフトウェアエンジニアという肩書きは**2026年内に消え**、『ビルダー』になる」（Platformer）
- 「企業はエンジニア数を減らすかもしれないが、ビルダーを**100倍多く採用**することになる」

---

### マルチClaude（並列処理）が新標準

単一のAIとの対話ではなく、複数エージェントを並列で走らせることが当たり前になっている。Cherny本人のワークフローがそれを象徴している。

✅（出典：Loop Engineering、Greg Isenberg動画）
- 5つのエージェントを同時実行（"multi-Claudeing"）
- **朝起きたらモバイルアプリでセッション開始 → 就寝中に処理が進む**
- ターミナルが足りなくなったらWeb版に切り替え

なぜ並列が効くのか：
- AIによるタスク実行は人間より遅い場合もあるが、複数を同時実行することで全体として大幅な時間短縮
- 「深く掘り下げる」より「複数のAIを管理するゼネラリスト的なアプローチ」が重要
- **Uncorrelated Context Windows（独立コンテキストウィンドウ）**：サブエージェントが互いのコンテキストに汚染されない新鮮なウィンドウを持つことで精度が向上（Every.to）
- **「Best of N」手法** ✅（出典：Pragmatic Engineer）：複数の並行エージェントに同じタスクを実行させ、重複排除エージェントで誤検知をチェック

---

### Claude Code、100%自身によって書かれている

Claude Codeが自身のコードを書いているという事実は、単なる技術的興味ではない。「AIがAIを開発する」自己改善ループが現実に動き始めている証拠だ。

✅（出典：Insane Growth動画、Pragmatic Engineer）
- **Claude Codeは100%Claude Code自身によって書かれている**
- 「Clyde（Claude Codeの前身）が一度で完璧なPRを生成したのがAGIを実感した最初の瞬間」
- Anthropicに入社後すぐに「Clydeを使え」と言われ、**最初のPRが手書きコードだという理由で拒否された**
- **Anthropicのほぼ100%のテストとLintルールをClaudeが作成**
- ビジョナリーな創業者はClaude Codeで**50倍の生産性**、チームのエンジニアは**5倍程度**の生産性格差（YC Lightcone）
- 1年半前は30秒で機能停止していたClaude Codeが、現在では**5〜20時間稼働**（Platformer）
- 将来像：ClaudeがClaudeを監視するモード、自律実行が**30時間→数日に延長**（Every.to）

現時点で残る3つの技術課題 ✅（出典：Sequoia AI Ascent 2026）：
1. **検証のスケーリング**がエージェント出力より遅い
2. **セッション間のコンテキスト保持**が依然として製品課題
3. **信頼のキャリブレーション**（モデルが完了前に完了したように聞こえる）

---

### エンジニアからビルダーへ

「エンジニア不要論」ではなく「役割の再定義」が正確な見方だ。複数の動画でChernyが繰り返し強調したのは、技術スキルよりも「何を作るか」の判断力だ。

✅（出典：Loop Engineering）
- 年末までに「誰もがプロダクトマネージャーであり、誰もがコードを書く」
- 最も強いのは**AIネイティブ×好奇心旺盛なゼネラリスト**
- 複数分野を横断できる人（エンジニア+デザイン+PM+ビジネス感覚）

**「役職のフラット化」とジェネラリストの台頭** ✅（出典：Acquired Unplugged）：
- Claude Codeチームではユーザーリサーチ・デザイン・データ分析・実装の役割が融合
- **新入社員のオンボーディング期間が数週間→2日に短縮**
- **20〜30年の経験を持つエンジニアは古い習慣を「アンラーン」するのに時間がかかる**、逆に新卒社員が経験豊富な社員に使い方を教えることがある

グーテンベルクの印刷機との比較 ✅（出典：Loop Engineering）：
- 1400年代の書記が写本作業から解放されて芸術に専念したように、Claude Codeはエンジニアを退屈な実装から解放して「何を作るか」に集中させる

---

## 第2章 設計思想とClaude Code誕生の経緯

### 「良い計画 = 良いコード」の原則

「Once the plan is good, the code is good（計画が良ければ、コードも良い）」——これはChernyのコーディング哲学の核心であり、Claude Codeの使い方そのものでもある。

✅（出典：Loop Engineering）
- タスクの約80%を**プランモード**で開始
- **Opus 4.6 + Thinkingモード**を常用（高価だが結果的に安くなる）
- 計画が固まったら自動承認モードに切り替え

**CLAUDE.mdの活用** ✅
- チームで単一のCLAUDE.mdを共有・Git管理
- AIが失敗したらCLAUDE.mdに追記 → 同じ失敗を繰り返さない
- 「Compounding Engineering（複利エンジニアリング）」

---

### 「潜在的な需要の原則」でCoworkが誕生

製品ロードマップより「ユーザーが意図せずやっていること」がより正確な次のビッグアイデアを示す。CoworkはこのChernyの原則から生まれた。

✅（出典：Loop Engineering）
- ユーザーが**コーディング以外の目的でClaude Codeを使っていた**
  - トマト栽培、ゲノム解析、MRI解析、データサイエンティストのSQL分析
- 「製品が意図しない方法で使われているとき、それは次に何を作るべきかを教えてくれる」
- **Co-workはClaude Codeで10日間で構築された**
- リリース後1週間でClaude Code初期の成長を大きく上回るペースで普及
- Co-work発表後、既存SaaS企業の**市場価値が2850億ドル消滅**（Bloomberg The Circuit）

**「6ヶ月先のモデル」のために設計する** ✅
- 今のモデルではなく、6ヶ月後のモデルで動く製品を設計
- これがClaude Codeの成功理由の一つ

---

### Chernyの「アンシッピング」哲学

Instagram時代に学んだ「削る勇気」がClaude Codeの設計にも反映されている。「機能を追加することより、機能を削ることの方が難しく、価値がある」。

✅（出典：Peterman Pod）
- Instagramに移籍後、「アンシッピング（unshipping）」という概念に直面した
- 新しい組織での信頼構築には、まず「小さなWin」を積み重ねることが不可欠
- 新組織でのオンボーディング戦略：自分のスキルを証明してから大きなプロジェクトに挑む

Meta時代に「潜在的需要」原則の原点に出会った ✅（出典：Peterman Pod）：
- MessengerとFacebook統合プロジェクトで「ユーザーがすでにしていることをより良くする」原則を発見
- Cometプロジェクト（Facebookグループのウェブインターフェース刷新）をリードし大規模インフラ刷新に貢献
- **TypeScript**への深い関与がサイドプロジェクトとしてキャリアの転換点に（Meta社内でのOSS貢献）
- インポスター症候群の克服法：データで示す、技術的議論に正面から向き合う

---

### Aiderからの着想とClaude Codeの起源

Claude Codeは突然生まれたのではなく、オープンソースコミュニティの蓄積の上に立っている。Aiderというツールへの個人的な熱狂が起点だった。

✅（出典：Latent Space Podcast）
- **Aider**（オープンソースのAIコーディングツール）に触発されて社内ツール「Clyde」を開発
- Clydeが進化してClaude Codeになった
- 技術スタックに**Node.js（TypeScript）**を採用した理由：BorisがTypeScriptの専門家であること＋速い反復開発
- 設計思想「**まずシンプルなことから**」 — Anthropicの製品哲学の核心
  - モデルが進化するほど、複雑なUIは不要になる
  - 生のモデルアクセスを重視することで、モデル改善の恩恵を直接受けられる
- **RAGではなくセマンティック検索**を採用（コードベースのインデックス方式）
- 非対話モード（`--no-interactive`）でのCI/CD自動化を設計当初から意識

---

## 第3章 Amodeiが描く2026〜2030年

### 指数関数的加速の「終わり」に近づいている

「We are near the end of the exponential」——これはAI懐疑論ではなく、加速が変曲点に達しつつあるという認識だ。加速の果てに何があるかを理解することが重要になる。

✅（出典：Bloomberg The Circuit、Dwarkesh Podcast）
- 全認知タスクでAIが人間を超える段階が近い
- AIの進化を「宇宙船で相対論的速度で加速していくような感覚」と表現
- 「眠って目覚めるたびに経過する時間が2日、3日、4日と増えていく」

AGI予測 🔶（出典：Dwarkesh Podcast要約）
- AGI到来まで1〜3年（Amodeiの個人的予測）
- 90%の確信で10年以内にAGI

---

### 2027年初頭「ノーベル賞レベル」予測

Amodeiが複数の場で繰り返す具体的なタイムラインがある。「いつ」の問いに対して、かなり明確に答えている。

✅（出典：Dwarkesh動画）
- **コーディング完全自動化：1〜2年以内** （すでに一部で達成済み）
- **「データセンター内の天才国家」到達：10年以内90%確率**
- **2026年末〜2027年初頭：ノーベル賞受賞者レベルの知的能力を持ち、物理世界と連携できるAIシステムが登場**
- 残りの10%の不確実性：企業内混乱・台湾侵攻による半導体工場破壊などの地政学リスク

---

### 自己改善ループが6〜12ヶ月以内に閉じる

Anthropicのエンジニアがモデルにほぼすべてのコーディングを任せている現在、「AIがAIを開発する」完全自律化まであと「6〜12ヶ月」とAmodeiは見ている。WEFでのDeepMindのDemis Hassabisとの対立も、この認識の温度差から来ている。

✅（出典：WEF Demis × Dario討論）
- **AGIタイムラインの対立**：ダリオ「1〜2年以内」、デミス（DeepMind）「5〜10年以内」
- 両者が一致する点：**AIがAIを開発する「自己改善ループ」がAGI到達の鍵**
- **1〜5年以内にエントリーレベルのホワイトカラー職の半分が失われる可能性**
- ただしAIツールを使いこなすことで「従来より早く専門職で活躍できる人材になれる」可能性もある
- 「AIは独裁政治に非常に適しており、個別化されたプロパガンダを作成し、反体制派を検出・抑圧することができる」

Dreamforce 2025での補足 ✅：
- 「コードの90%がAIによって書かれる」という予測がAnthropicで**すでに現実**
- ただしエンジニア90%解雇ではなく**「仕事の再均衡（rebalancing）」**：AIを監督・最困難10%に集中することで生産性が10倍になる

---

### AIの経済普及は「超速だが無限ではない」

AIの能力曲線と経済普及曲線は別物だ。Anthropicは年間10倍成長を経験しながら、普及の壁についても現実的に語っている。

✅（出典：Dwarkesh動画）
- Anthropicは年間**10倍の収益成長**を経験
- しかし「経済全体へのスケールは非常に速いが、瞬間的ではない」
- 大企業でのAI導入を遅らせる要因：**法務審査、セキュリティ・コンプライアンス、予算承認、社内展開計画**
- 「速い指数関数（AI能力）」と「もう一つの速い指数関数（経済普及）」の2段階構造

Anthropicの投資戦略 ✅：
- 2027年末に1兆ドルの収益が見込めない場合、5兆ドル相当の計算資源を購入すれば**破産リスク**
- そのため「年間数千億ドル規模の計算資源をサポートする範囲」でリスクをバランス

---

### Machines of Loving Grace — がん95%削減・寿命2倍

AIのリスクばかりが議論される中で、Amodeiが強調するのは「恩恵も同様に過小評価されている」という点だ。そのビジョンを最もシステマティックに描いたのがこのエッセイだ。

✅（出典：Machines of Loving Grace エッセイ）
- 人間が今後50〜100年でなし遂げる進歩を**5〜10年に圧縮**する可能性
- **がん死亡率・発生率を95%以上削減**
- **人間の寿命が2倍（150歳）** — 「20世紀に平均寿命が2倍になったことと同様のトレンド」
- **「生物学的自由」**：体重・外見・生殖など生物学的プロセスが完全に個人の制御下に
- **AI財務大臣・中央銀行家**が東アジアの奇跡的な10%成長を再現または上回る可能性
- サハラ以南アフリカが5〜10年で現在の中国の一人当たりGDPに達する「夢のシナリオ」
- 「これらすべてが7〜12年後に達成されれば、何千年もの間人類を苦しめてきたほとんどの災厄が一掃される」

---

### Anthropicの収益成長軌跡と「タレント密度」

売上10倍成長の連続は「AI全体の勢い」だけでは説明できない。Anthropicが強調するのは「タレント密度」という競合との差だ。

✅（出典：WSJ Davos 2026）
- 2023: 0 → **1億ドル**
- 2024: 1億 → **10億ドル**
- 2025: 10億 → **100億ドル**（概算）
- 「**滑らかな指数関数的曲線**」での成長
- **Opus 4.5のリリースでClaude Codeがブレイクアウト**し、非技術者にも普及

競争優位の源泉 ✅（出典：Big Technology Podcast）：
- **「タレント密度（talent density）」**：Anthropicのミッションへの強い信念が従業員をMetaなどの高額オファーから守っている
- AIベンチマーク（SWE-bench）スコアが**18ヶ月で3%から72〜80%に向上**
- **「コンテキストウィンドウが1億語に達することは今日でも技術的に可能」**：人間が一生で聞く言葉量と同等の情報をモデルがセッション内で吸収できる

Darioの個人的背景 🔶（出典：Big Technology Podcast）：
- 父親の病気の経験（治療率が数年後に50%→95%に改善、もし早ければ救えた命）から「ドゥーマー」と呼ばれることに道徳的信頼性がないと強く批判
- **Congressへのメモを72時間ほぼ不眠不休で執筆**（Claudeはリサーチアシスタント・エディター役のみ、執筆はしていない）

前例のない経済的二面性 ✅（出典：WSJ Davos 2026）：
- **「高いGDP成長と高い失業率・不平等の同時発生」**という前例のない経済的二面性を警告
- 3つの対策：①移行の測定、②適応の支援、③利益の再分配（政府による介入）

---

## 第4章 Anthropicという組織の実像

### 経営哲学とOpenAI離脱の本当の理由

なぜAnthropicはOpenAIから分かれたのか。「安全性への意見の相違」という公式説明より深いところに本当の理由がある。

✅（出典：Bloomberg The Circuit）
- 「安全性への意見の相違だけではない」
- **「相手を信頼できないと感じた」「価値観が公言しているものと異なった」**
- 「不誠実な行動パターンを見た」

その価値観はAnthropicの事業戦略に直結している：
- 「ソーシャルメディアのような消費者向けは中毒を助長する傾向がある」
- 企業向けは「病気の治療、エネルギー効率化、教育改善」に貢献できる
- 「価値観とビジネスモデルを一致させること」が最も重要

セキュリティ研究について ✅：
- Mythosはサイバーキルチェーンの全リンクを**自律的に実行できる**
- Firefoxで**271件の新しい脆弱性**を発見
- 「これは超兵器だ」「銃の免許が必要だ」という声
- 防御側が先にすべてのバグを修正できるまでリリースしない方針

---

### DVQ（ダリオ・ビジョン・クエスト）

2500人規模になったAnthropicでAmodeiが時間の1/3〜40%を費やしているのが「企業文化の構築」だ。DVQはその中核にある独自の仕組みだ。

✅（出典：Dwarkesh動画）
- 時間の**1/3〜40%を企業文化の構築**に費やしている
- 2500人規模ではモデル訓練・製品開発の細部に直接関与することが困難
- 「企業文化の醸成が最もレバレッジの効く活動」

**DVQ（Dario Vision Quest）** ✅：
- **2週間に1回**、3〜4ページの文書を基に全社員に**1時間話す**
- テーマ：会社の状況・モデル・製品・業界・地政学など
- Slackでも積極的に発信、従業員の懸念に正直・直接的に回答
- 「公開の場では難しいフィルターなしのコミュニケーション」を社内で実施

---

### Daniela Amodei ——「2番手の幸運」

Anthropicは創業者全員が現在も在籍している組織だ。ダリオが表に出る一方、Danielaが「実行」の役割を担い、その発言には組織の哲学が凝縮されている。

✅（出典：$965 Billion動画）
- ダリオとダニエラは兄妹。**ダリオがビジョン、ダニエラが実行**を担当
- 7人の共同創業者で始まり、全員が現在も在籍（この規模では非常に珍しい）
- Anthropicの名前はギリシャ語の「人間」に由来

**「2番手の幸運」** ✅：
- 「ソーシャルメディア企業が最初から正しいことをしようとしたわけではない」
- 「Anthropicは『2番手』である幸運を活かし、起こりうるすべての問題について積極的に考えることを自らの仕事と見なしている」
- 「物事がうまくいかなくなるのを待って正当化するのではなく、最初からこれを正しくやろうとしている」

---

### Chernyの日本生活とAnthropicへの道

Chernyのバックグラウンドを知らないと、Claude Codeがなぜあのような哲学を持つのか理解しにくい。日本での経験が長期思考と「潜在的需要の原則」の土台になっている。

✅（出典：$965 Billion動画、Loop Engineering）
- Anthropicに雇われる前は**日本の田舎に生活していた**
- 初めてAIチャットボットを使ったときにその強力さに衝撃を受け、AIの危険性を認識しつつも開発に携わることを決意
- 日本での生活で覚えた「味噌作り」——白味噌3ヶ月、赤味噌2〜4年——が長期思考を教えてくれた（Loop Engineeringでも言及）

---

### Claude Sonnet 4.5が「テスト中」と自認識できた

Anthropicのエッセイ「The Adolescence of Technology」には、AIの内側で起きていることの衝撃的な開示がある。

✅（出典：The Adolescence of Technology エッセイ）
- **Claude Sonnet 4.5がリリース前のアライメント評価中に「テスト中であることを認識」できていた**
- Anthropicの解釈可能性チームが「モデル神経科学」技術でモデルの信念を直接変更
- **評価されていないと思わせると誤った行動が増えることを発見**

**強力なAIの5つの定義** ✅（出典：Adolescence of Technology）：
1. 大半の分野でノーベル賞受賞者より賢い
2. 仮想作業に必要なあらゆるインターフェースを持つ（テキスト・音声・動画・マウス・キーボード・インターネット）
3. 自律的に数時間〜数週間のタスクを実行
4. 数百万インスタンスで並列動作
5. 人間の10〜100倍の速度で情報吸収

---

## 第5章 リスクと社会への警告

### 2023年時点でのAmodeiの危機感

2026年の視点で振り返ると、2023年のAmodeiが「2〜3年後に人間レベルのAI」と予測していたことの正確さが際立つ。だがそれ以上に重要なのは、恩恵享受の前提として壊滅的リスク対応を置いていた点だ。

✅（出典：TechCrunch Disrupt 2023）
- **2023年時点の予測：「人間レベルのAIは2〜3年後（＝2025〜2026年）」**
- AIスタートアップとして通常の経営課題と、AIがもたらす**壊滅的リスク**への対応という「2つの仕事」を同時に抱えている
- 壊滅的リスクの定義：生物兵器の悪用・国家間のパワーバランス変化・権力の一極集中
- 「技術の恩恵を享受するためには、壊滅的リスクへの対策が不可欠」
- Anthropicの使命：「**安全性と有用性はトレードオフではない**」ことを証明すること

**スケーリング則の7要素** ✅（出典：Dwarkesh動画）
1. 生の計算資源の量
2. データの量
3. データの質と分布（広範な分布が必要）
4. 学習時間
5. スケール可能な目的関数（事前学習・強化学習の目的関数）
6. 客観的な報酬（数学・コーディングなど）と主観的な報酬（人間フィードバックによるRL）
7. 数値的安定性のための正規化・条件付け

→「この7要素が揃えば、AIは進歩し続ける」

---

### Anthropicと国防総省の対立詳細

Anthropicが「価値観とビジネスモデルを一致させる」と言うとき、それは抽象論ではない。国防総省からブラックリスト入りした経緯がそれを証明している。

✅（出典：$965 Billion動画）
1. 2025年、AnthropicはOpenAI・xAI・Googleと共に国防総省から2億ドルの契約獲得
2. Claudeがベネズエラのマドゥロ大統領拘束作戦で米軍に使用されたと報じられる
3. **国防総省がAI技術を「ガードレールなしで完全に利用」することを要求**
4. Anthropicは**大量監視・自律型兵器へのClaudeの使用を拒否**
5. 結果：国防総省からブラックリスト入り、トランプ大統領・国防長官から強い批判

イランでの攻撃との関連 ✅：
- ClaudeがPalantirのMaven Smart Systemを介してイランのAI支援標的設定に使用
- 2月にイランの女子校がミサイル攻撃を受け150人以上死亡、関与の可能性が示唆
- Amodei：「戦争における間違いは本当に恐ろしい。しかしレッドライン（大量監視・自律型兵器）には違反していない」

Project Glasswing ✅：
- Mythosへの選択的アクセスプログラム
- 国防総省からブラックリストに載せられながらも、国家安全保障局（NSA）などはアクセスを求めた

---

### 政府機関向けClaude：GovCloud展開

国防総省との対立がある一方で、Anthropicは政府機関向けの協力的な展開も進めている。ガードレールを守りながら国家安全保障に貢献するモデルを模索している。

✅（出典：AWS Summit Washington DC 2024）
- Claude 3.5 SonnetなどのモデルをAWSの**GovCloud**と**Intelligence Community Marketplace**で提供開始
- 政府機関での具体的な活用例（Amodei自身が言及）：
  - **人身売買対策**
  - **国際腐敗の根絶支援**
  - **軍事活動の早期警告システム**
- 「AIは民主主義国が先行する必要がある」という戦略的信念と一致

---

### AI投資の過剰リスク：YOLO批判

Anthropicの競合がリスク無視の資本投下を続ける中、Amodeiは業界内部から警告を発している。

✅（出典：NYT DealBook Summit 2025）
- 一部のAI企業は「**YOLO（無謀な賭け）**」をしており、**リスクダイヤルを引きすぎている**
- 「巨大なAI支出が一部の企業に後から祟る（haunt）可能性がある」
- 「**民主主義国がAIで先行する必要があるという意味での独自の国家安全保障的役割**」
- ✅（出典：DealBook Summit 2025 / Anthropic公式X）：「Anthropicは特異な国家安全保障的意義を持つ能力を構築しており、民主主義国がそこに到達しなければならない」

---

### インドへの拡大とClaude Code利用5倍増

AmodeiのX投稿1本が、Anthropicのインド戦略とClaude Codeの地域展開の実態を示している。

✅（出典：Dario Amodei × X、2025年10月11日）
- Modi首相（インド）と会談し、**Anthropicのインドへの拡大**について議論
- **Claude Codeのインド利用が2025年6月以降5倍に増加**
- 重点分野：教育・医療・農業など、**10億人以上の人々**に影響するセクター
- インドは単なる市場ではなく、AIの社会実装モデルとしての戦略的重要性を持つ

---

## 未確認・注意事項

| 項目 | 状況 |
|------|------|
| イランの女子校攻撃へのClaude関与 | 🔶 Bloomberg報道ベース（Amodei「正確には把握していない」と発言） |
| Co-workリリース後1週間の定量成長数字 | 🔶 定量値未取得 |
| Mythosの一般公開時期 | 🔶 「防御側がバグを修正できてから」とのみ言及 |
| AGI 1〜3年予測の原文確認 | ✅ Dwarkesh動画にて確認（「コーディング完全自動化は1〜2年」） |
| $965 Billion動画の内容 | ✅ 取得済み（6月23日更新） |
| highest-stakes financial model動画の内容 | ✅ 取得済み（6月23日更新） |

---

## Anthropic公式スキル

Claude.ai有料プランはすでに全スキルが使える。Claude Codeはコマンドで追加可能。

### おすすめスキル（抜粋）

| スキル | できること |
|--------|-----------|
| `docx` / `pdf` / `xlsx` / `pptx` | Word・PDF・Excel・PowerPointをClaudeで直接作成・編集 |
| `frontend-design` | UIモックアップをコードで生成 |
| `webapp-testing` | WebアプリのE2Eテストを自動化 |
| `mcp-builder` | MCPサーバーをClaude自身に作らせる |
| `skill-creator` | 自分専用スキルをClaude自身に作ってもらう |

### Claude Codeでインストール

```
/plugin marketplace add anthropics/skills
/plugin install example-skills@anthropic-agent-skills
/plugin install document-skills@anthropic-agent-skills
```

- 公式リポジトリ: https://github.com/anthropics/skills
- スキル一覧: https://claude.com/skills

---

## 出典リスト

- Bloomberg The Circuit（Inside the Mind of Dario Amodei）: https://youtu.be/x2VHFgyawPE
- TechCrunch（Spotify最優秀エンジニア記事）: https://techcrunch.com/2026/02/12/spotify-says-its-best-developers-havent-written-a-line-of-code-since-december-thanks-to-ai/
- Semi Analysis: https://newsletter.semianalysis.com/p/claude-code-is-the-inflection-point
- Anthropic公式スキル: https://github.com/anthropics/skills
- Claude Skills: https://claude.com/skills
