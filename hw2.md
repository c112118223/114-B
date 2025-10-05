
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#8FAADC', 'fontFamily': 'Noto Sans TC'}}}%%
gantt
    title 系統開發專案時程
    dateFormat  YYYY-MM-DD
    axisFormat  %m/%d
    todayMarker off

    section 企劃階段
    研擬計畫          :a1, 2025-10-01, 1d
    任務分配          :a2, after a1, 4d

    section 硬體階段
    取得硬體          :a3, after a1, 17d
    安裝硬體          :a5, after a3, 10d

    section 軟體階段
    程式開發          :a4, after a2, 70d
    程式測試          :a6, after a4, 30d
    撰寫使用手冊      :a7, after a5, 25d
    轉換檔案          :a8, after a5, 20d

    section 系統整合
    系統測試          :a9, after a6, 25d
    使用者訓練        :a10, after a7 a8, 20d
    使用者測試        :a11, after a9 a10, 25d

```


```mermaid
flowchart TD
    A[1 研擬計畫<br>1天] --> B[2 任務分配<br>4天]
    A --> C[3 取得硬體<br>17天]
    B --> D[4 程式開發<br>70天]
    C --> E[5 安裝硬體<br>10天]
    D --> F[6 程式測試<br>30天]
    E --> G[7 撰寫使用手冊<br>25天]
    E --> H[8 轉換檔案<br>20天]
    F --> I[9 系統測試<br>25天]
    G --> J[10 使用者訓練<br>20天]
    H --> J
    I --> K[11 使用者測試<br>25天]
    J --> K
```


| 任務 | 描述 | 前置 | 工期(天) | 最早開始 | 最早完成 | 最晚開始 | 最晚完成 |
|------|------|------|-----------|-----------|-----------|-----------|-----------|
| 1 | 研擬計畫 | - | 1 | 0 | 1 | 0 | 1 |
| 2 | 任務分配 | 1 | 4 | 1 | 5 | 1 | 5 |
| 4 | 程式開發 | 2 | 70 | 5 | 75 | 5 | 75 |
| 6 | 程式測試 | 4 | 30 | 75 | 105 | 75 | 105 |
| 9 | 系統測試 | 6 | 25 | 105 | 130 | 105 | 130 |
| 11 | 使用者測試 | 9 | 25 | 130 | 155 | 130 | 155 |

**➡ 關鍵路徑：**
> 1 → 2 → 4 → 6 → 9 → 11  


