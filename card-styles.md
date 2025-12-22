# アカウントカード スタイル比較表

## ベース仕様（mock.html）

### カード全体
| 項目 | mobile | desktop |
|------|--------|---------|
| カード幅 | 144px | 160px |
| padding | 16px 8px | 16px 8px |
| gap | 12px | 14px |
| border-radius | 10px | 10px |
| box-shadow | 8px 6px 18px rgba(99,55,90,0.13) | ← |

### プロフィール画像
| 項目 | mobile | desktop |
|------|--------|---------|
| サイズ | 84px | 90px |

### アカウント名
| 項目 | mobile | desktop |
|------|--------|---------|
| font-size | 12px | 15px |
| font-weight | 600 | 600 |
| text-align | center | center |
| 行数 | 1行 | 1行 |
| overflow | ellipsis | ellipsis |

### メタ情報
| 項目 | mobile | desktop |
|------|--------|---------|
| gap（行間） | 4px | 6px |

### フォロワー数
| 項目 | mobile | desktop |
|------|--------|---------|
| font-size | 10px | 13px |
| font-weight | 500 | 500 |

### ジャンル
| 項目 | mobile | desktop |
|------|--------|---------|
| font-size | 9px | 12px |
| font-weight | 500 | 500 |

### 日付
| 項目 | mobile | desktop |
|------|--------|---------|
| font-size | 10px | 13px |
| font-weight | 500 | 500 |
| letter-spacing | 0.5px | 0.65px |

### アイコン
| 項目 | mobile | desktop |
|------|--------|---------|
| サイズ | 10px | 13px |
| stroke-width | 1.5 | 1.5 |

---

## バリエーション（ベースからの変更点のみ）

### v1: mock_v1.html
**アカウント名2行表示（中央揃え）**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| font-size | 11px | 13px | 12px→11px / 15px→13px |
| 行数 | 2行 | 2行 | 1行→2行 |
| line-height | 1.4 | 1.4 | 新規追加 |
| min-height | 30.8px | 36.4px | 新規追加（2行分確保） |
| overflow | line-clamp:2 | line-clamp:2 | ellipsis→line-clamp |
| メタgap | 2px | 4px | 4px→2px / 6px→4px |

---

### v2: mock_v2.html
**v1 + アカウント名左揃え**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| text-align | left | left | center→left |

※その他はv1と同じ

---

### v3: mock_v3.html
**v1 + 日付→投稿数に変更 + フォロワー数を日本語単位表示 + ジャンルフォント統一**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| 3行目 | 投稿数 | 投稿数 | 日付→投稿数に置き換え |
| アイコン | 鉛筆 | 鉛筆 | カレンダー→編集アイコン |
| フォーマット | X,XXX投稿 | X,XXX投稿 | カンマ区切り+単位「投稿」 |
| letter-spacing | なし | なし | 0.5px/0.65px→削除 |
| フォロワー数 | 日本語単位 | 日本語単位 | 1万未満: カンマ区切り、1万以上: X.X万、1億以上: X.X億 |
| ジャンルfont-size | 10px | 13px | 9px→10px / 12px→13px（他メタ情報と統一） |

※その他はv1と同じ

---

### v4: mock_v4.html
**v3 + 単位（万/億/投稿）のフォントサイズ縮小**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| 単位フォント | 0.8em | 0.8em | 数字の80%サイズで表示 |
| 対象 | 万/億/投稿 | 万/億/投稿 | spanタグで単位を分離 |

※その他はv3と同じ

---

### v5: mock_v5.html
**v4 + アカウント名〜フォロワー間の余白縮小**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| 名前margin-bottom | -4px | -6px | 余白を12px→8px / 14px→8pxに縮小 |

※その他はv4と同じ

---

### v6: mock_v6.html
**v5 + プロフィール画像サイズ縮小（約10%）**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| 画像サイズ | 76px | 82px | 84px→76px / 90px→82px（約10%縮小） |

※その他はv5と同じ

---

### v7: mock_v7.html
**v6 + モバイル最適化（カード幅拡大・メタ情報フォント+1px）**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| カード幅 | 168px | 160px | 144px→168px（mobileのみ） |
| grid | minmax(168px, 168px) | minmax(160px, 160px) | mobileのみ変更 |
| フォロワーfont-size | 11px | 13px | 10px→11px（mobileのみ） |
| ジャンルfont-size | 10px | 12px | 9px→10px（mobileのみ） |
| 投稿数font-size | 11px | 13px | 10px→11px（mobileのみ） |
| アイコンサイズ | 11px | 13px | 10px→11px（mobileのみ） |

※desktopはv6と同じ

---

### v8: mock_v8.html
**v7 + モバイルフォントさらに+1px（視認性向上）**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| アカウント名font-size | 12px | 13px | 11px→12px（mobileのみ） |
| フォロワーfont-size | 12px | 13px | 11px→12px（mobileのみ） |
| ジャンルfont-size | 11px | 12px | 10px→11px（mobileのみ） |
| 投稿数font-size | 12px | 13px | 11px→12px（mobileのみ） |
| アイコンサイズ | 12px | 13px | 11px→12px（mobileのみ） |

※desktopはv7と同じ

---

### v9: mock_v9.html
**v8 + モバイルフォントをデスクトップと統一**

| 項目 | mobile | desktop | 変更内容 |
|------|--------|---------|---------|
| アカウント名font-size | 13px | 13px | 12px→13px（統一） |
| フォロワーfont-size | 13px | 13px | 12px→13px（統一） |
| ジャンルfont-size | 12px | 12px | 11px→12px（統一） |
| 投稿数font-size | 13px | 13px | 12px→13px（統一） |
| アイコンサイズ | 13px | 13px | 12px→13px（統一） |

※モバイルとデスクトップで同じフォントサイズを使用

---

## 更新履歴
- 2024/12/22: 初版作成（ベース、v1、v2）
- 2024/12/22: v3追加（日付→投稿数）
- 2024/12/22: v3更新（フォロワー数を日本語単位表示に変更）
- 2024/12/22: v4追加（単位フォントサイズを0.8emに縮小）
- 2024/12/22: v4更新（ジャンルフォントをベースサイズ9px/12pxに戻す）
- 2024/12/22: v5追加（アカウント名〜フォロワー間の余白縮小）
- 2024/12/22: v6追加（プロフィール画像サイズ約10%縮小）
- 2024/12/22: v7追加（モバイル最適化: カード幅拡大、メタ情報フォント+1px）
- 2024/12/22: v8追加（モバイルメタ情報フォントさらに+1px）
- 2024/12/22: v9追加（モバイルフォントをデスクトップと統一）
