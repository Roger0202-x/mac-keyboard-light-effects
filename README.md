# Mac Keyboard Light Effects for Codex

這是一個可重複安裝的 Codex Skill，會在 Apple Silicon MacBook 上建立原生的 macOS 選單列 App，用來控制內建鍵盤背光。

## 功能

- 呼吸燈：鍵盤背光在 0% 到 100% 之間自然明暗
- 三種呼吸速度：4、6、8 秒
- 音樂律動鍵盤燈：依麥克風取得的即時音量調整亮度
- 通知閃燈：macOS 顯示通知橫幅時，鍵盤背光雙閃提醒
- 測試通知閃燈
- 直接控制背光，不顯示 macOS 鍵盤亮度調整畫面
- 不包含打字反應功能，也不監控鍵盤輸入

## 最簡單的安裝方式

把下面這段文字貼給 Codex：

```text
請下載並安裝這個 Codex Skill：https://github.com/Roger0202-x/mac-keyboard-light-effects/raw/refs/heads/main/mac-keyboard-light-effects.skill.zip

安裝完成後，使用 $mac-keyboard-light-effects 幫我檢查相容性，並安裝鍵盤呼吸燈、音樂律動與通知閃燈。
```

## 手動安裝 Skill

1. [下載 Skill ZIP](https://github.com/Roger0202-x/mac-keyboard-light-effects/raw/refs/heads/main/mac-keyboard-light-effects.skill.zip)。
2. 解壓縮後，將 `mac-keyboard-light-effects` 資料夾放入 `~/.codex/skills/`。
3. 重新開啟 Codex。
4. 輸入：

```text
使用 $mac-keyboard-light-effects 幫我檢查相容性，並安裝鍵盤呼吸燈、音樂律動與通知閃燈。
```

## 相容性

- Apple Silicon MacBook
- 具備內建鍵盤背光
- 安裝時需要 Xcode Command Line Tools 提供的 `clang`
- 通知閃燈第一次啟用時，macOS 可能要求「輔助使用」權限
- 音樂律動第一次啟用時，macOS 會要求「麥克風」權限
- 使用 Apple 私有的 CoreBrightness 介面，未來 macOS 更新可能需要調整

## 隱私

- 不讀取通知文字內容
- 麥克風只轉換成即時音量，不錄音、不儲存、不轉成文字
- 不記錄按鍵
- 不需要「輸入監控」權限
- 不需要「完整磁碟存取」權限
- 所有處理都在本機執行

## 移除

在選單列結束 App，然後刪除：

```text
/Applications/鍵盤呼吸燈.app
```

第三方授權資訊位於 `references/THIRD_PARTY_NOTICES.txt`。
