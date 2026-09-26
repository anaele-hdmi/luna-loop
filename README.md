# ルナ・ループ（Lunar Loop）

地球の低軌道から月を回って帰ってくる、スマホ向けの軌道シミュレータ。

- 物理は実物: 地球と月の重力、有限時間の噴射、大気抵抗と揚力。表示されるkm・km/s・Gは実物理の値
- 表示はデフォルメ: 天体は実寸の3倍、距離はべき乗で圧縮
- 1ファイル（`index.html`）。three.js は CDN（jsDelivr）から読み込む。ビルド不要

## 遊び方
1. 上の1行が「次にやること」。光っているボタンを使う
2. 『▶▶ 次へ』で次の場面まで早送り。点火地点では自動で止まる
3. 噴射を長押しして、スローになったら針が緑に入ったところで離す
4. TLI → 巡航 → LOI →（月を好きなだけ周回）→ TEI → 帰還・再突入 → パラシュートで着水

操作モード: A 長押し（おすすめ）／B 引っ張り（上級。噴射量と時刻を計画して自動実行）

## ローカルで動かす
```
python3 -m http.server 8000
# http://localhost:8000
```

## 公開（GitHub Pages）
ビルド不要の静的サイト。Settings → Pages → Build and deployment で Source を「Deploy from a branch」、Branch を `main` / `/ (root)` にして Save。
公開URL: https://anaele-hdmi.github.io/luna-loop/

設計と検証の記録は [PLAN.md](PLAN.md)。
