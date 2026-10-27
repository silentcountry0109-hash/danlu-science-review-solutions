# 國中自然複習講義｜練習題詳解（網頁版）

典陸教育集團《國中自然複習講義》1上～3下（翰林 112 版，34 章）練習題詳解。
單一靜態頁面 `index.html`，手機、平板、電腦都可閱讀；題號與講義學用版、教用版一致。

## 部署到 GitHub Pages

1. 在 GitHub 建立一個新的空 repository（例如 `danlu-science-review-solutions`，不要勾選建立 README）。
2. 在這個資料夾執行：
   ```bash
   git remote add origin https://github.com/<帳號>/<repository>.git
   git push -u origin main
   ```
3. GitHub 上該 repository → Settings → Pages → Build and deployment：Source 選「Deploy from a branch」，Branch 選 `main`、資料夾 `/ (root)`，按 Save。
4. 約一分鐘後上線。目前網址：**https://danlu-science-review-solutions.danlu-education.com/**
   （自訂網域：Namecheap 的 danlu-education.com 加 CNAME 記錄 `danlu-science-review-solutions` → `silentcountry0109-hash.github.io`，repository 的 `CNAME` 檔記錄網域；舊網址 silentcountry0109-hash.github.io/danlu-science-review-solutions/ 會自動轉址。）

## 網址錨點（做 QR Code 用）

| 錨點 | 開啟 |
|---|---|
| `#1a` `#1b` `#2a` `#2b` `#3a` `#3b` | 1上、1下、2上、2下、3上、3下 |
| `#3b-4` | 3下 第四章 |
| `#3b-4-k2` | 3下 第四章 知識點 2（自動展開） |
| `#3b-4-q12` | 3下 第四章 第 12 題 |

每冊學用合併本封面的 QR Code 指向 `https://danlu-science-review-solutions.danlu-education.com/#1a` 等，掃描後直接開啟該冊。

## 更新內容

詳解資料來自專案資料夾 `配套/<冊>/CH*/`（layout.json、new.json、old.json）。修改後在專案根執行：

```bash
python3 模板/配套/build_web.py <本資料夾路徑>
git add index.html && git commit -m "更新詳解" && git push
```

---
專 業 升 國 中 · 升 高 中 · 升 大 學　｜　典陸教育集團
