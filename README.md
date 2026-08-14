# stock-poweichen-data

台股策略日報系統的 `tracking.json` 公開鏡像。

## 這是什麼

`tracking.json` 是該系統的長期記憶：每日盤前預測、盤後機械化對答案結果、
命中率與信心校準所需的全部結構化紀錄。內容與
`https://stock.poweichen.com/data/tracking.json` 相同。

## 為什麼需要這份鏡像

盤前預測由 Anthropic 雲端排程 agent 產生，該環境的網路 egress 採白名單制，
讀不到 stock.poweichen.com 與證交所網域，但 `raw.githubusercontent.com` 放行。
此鏡像是雲端 agent 取得歷史紀錄、達成規格第二章「觀點連續性（貝葉斯更新）」
要求的唯一通道。

讀取網址：

```
https://raw.githubusercontent.com/Wyatt1982/stock-poweichen-data/main/tracking.json
```

## 這裡沒有什麼

本 repo 只放 `tracking.json`。持股明細與小道消息存於 `portfolio.enc.json`
（AES-GCM 加密，留在私有 repo 與自有網域），不會出現在這裡。
明文模板、建置工具、憑證一律不進本 repo。

## 免責

本資料為 AI 策略系統之自我追蹤紀錄，僅供參考，不構成投資建議。
