<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Jump baby shop 童裝記帳系統</title>
    <style>
        /* --- 韓系奶油風 核心變數 --- */
        :root {
            --bg-cream: #FDFBF7;
            --bg-card: #FFFFFF;
            --primary-latte: #E6D5C3;
            --primary-dark: #6C5441;
            --accent-peach: #F3E1D3;
            --accent-warm: #D9A079;
            --text-main: #4A3E3D;
            --text-muted: #9E918A;
            --danger: #DE7C7C;
            --success: #6C5441; /* 正數使用深咖啡色 */
            --shadow-soft: 0 8px 24px rgba(108, 84, 65, 0.05);
            --border-radius: 16px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-cream);
            color: var(--text-main);
            padding-top: 60px;
            padding-bottom: 80px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* --- 頂部快選列 Quick Toolbar --- */
        .top-navbar {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            height: 60px;
            background-color: var(--bg-card);
            display: flex;
            justify-content: space-around;
            align-items: center;
            box-shadow: 0 2px 10px rgba(108, 84, 65, 0.05);
            z-index: 100;
            border-bottom: 1px solid var(--accent-peach);
        }

        .nav-btn {
            background: none;
            border: none;
            color: var(--text-muted);
            font-size: 15px;
            font-weight: 600;
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .nav-btn.active {
            background-color: var(--primary-latte);
            color: var(--primary-dark);
        }

        /* --- 頁面容器與切換 --- */
        .app-page {
            display: none;
            padding: 16px;
            flex: 1;
            max-width: 600px;
            margin: 0 auto;
            width: 100%;
        }

        .app-page.active {
            display: block;
        }

        h2.shop-title {
            text-align: center;
            font-size: 18px;
            color: var(--primary-dark);
            margin-bottom: 16px;
            letter-spacing: 1px;
        }

        /* --- 膠囊橫向滑動元件 --- */
        .capsule-scroll {
            display: flex;
            overflow-x: auto;
            white-space: nowrap;
            padding: 8px 4px;
            gap: 10px;
            scrollbar-width: none;
        }
        .capsule-scroll::-webkit-scrollbar {
            display: none;
        }

        .capsule-btn {
            background-color: var(--bg-card);
            border: 1px solid var(--primary-latte);
            color: var(--text-main);
            padding: 8px 16px;
            border-radius: 30px;
            font-size: 14px;
            cursor: pointer;
            flex-shrink: 0;
            box-shadow: var(--shadow-soft);
        }
        .capsule-btn.active {
            background-color: var(--primary-dark);
            color: #FFFFFF;
            border-color: var(--primary-dark);
        }

        /* --- 頁面1: 月曆頁面樣式 --- */
        .calendar-container {
            background: var(--bg-card);
            border-radius: var(--border-radius);
            padding: 16px;
            box-shadow: var(--shadow-soft);
            margin-bottom: 16px;
        }

        .calendar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
            font-weight: bold;
            color: var(--primary-dark);
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 8px;
            text-align: center;
        }

        .weekday {
            font-size: 12px;
            color: var(--text-muted);
            font-weight: 600;
            padding-bottom: 8px;
        }

        .calendar-day {
            aspect-ratio: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
            position: relative;
            cursor: pointer;
            border-radius: 50%;
        }

        /* 當日與選中日期的深色圓形 */
        .calendar-day.today::after {
            content: '';
            position: absolute;
            width: 32px;
            height: 32px;
            border: 2px solid var(--primary-dark);
            border-radius: 50%;
            z-index: 1;
        }
        .calendar-day.selected::after {
            content: '';
            position: absolute;
            width: 32px;
            height: 32px;
            background-color: var(--primary-dark);
            border-radius: 50%;
            z-index: 1;
        }
        .calendar-day.selected {
            color: #FFFFFF !important;
        }
        .calendar-day span {
            position: relative;
            z-index: 2;
        }
        .calendar-day.empty {
            cursor: default;
        }

        /* 每日收支列表方框 (四邊圓弧) */
        .daily-records-box {
            background: var(--bg-card);
            border-radius: var(--border-radius);
            padding: 16px;
            box-shadow: var(--shadow-soft);
            min-height: 150px;
        }
        .box-title {
            font-size: 14px;
            font-weight: bold;
            color: var(--primary-dark);
            margin-bottom: 12px;
            border-left: 4px solid var(--primary-latte);
            padding-left: 8px;
        }

        .record-list {
            list-style: none;
        }
        .record-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px dashed var(--accent-peach);
            font-size: 14px;
        }
        .record-item:last-child {
            border-bottom: none;
        }
        .record-info {
            flex: 1;
        }
        .record-amount {
            font-weight: 600;
            margin-right: 12px;
        }
        .amt-income { color: var(--success); }
        .amt-expense { color: var(--danger); }
        
        .delete-btn {
            background: none;
            border: none;
            font-size: 16px;
            cursor: pointer;
            padding: 4px;
        }

        /* 右下角浮動新增按鈕 */
        .fab-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 56px;
            height: 56px;
            border-radius: 50%;
            background-color: var(--primary-dark);
            color: #FFFFFF;
            font-size: 28px;
            border: none;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            z-index: 90;
        }

        /* --- 底部滑出記帳面板 Bottom Sheet --- */
        .bottom-sheet {
            position: fixed;
            bottom: -100%;
            left: 0;
            right: 0;
            height: 85vh;
            background-color: var(--bg-cream);
            border-top-left-radius: 24px;
            border-top-right-radius: 24px;
            box-shadow: 0 -4px 20px rgba(0,0,0,0.15);
            z-index: 200;
            transition: bottom 0.4s cubic-bezier(0.25, 1, 0.5, 1);
            display: flex;
            flex-direction: column;
        }
        .bottom-sheet.open {
            bottom: 0;
        }
        .sheet-overlay {
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(0,0,0,0.4);
            z-index: 199;
            display: none;
        }
        .sheet-header {
            padding: 12px;
            display: flex;
            justify-content: center;
            background: var(--bg-card);
            border-top-left-radius: 24px;
            border-top-right-radius: 24px;
            border-bottom: 1px solid var(--accent-peach);
            position: relative;
        }
        .close-sheet {
            position: absolute;
            right: 16px;
            top: 12px;
            background: none;
            border: none;
            font-size: 20px;
            color: var(--text-muted);
        }

        .sheet-body {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            padding-bottom: 100px;
        }

        /* 記帳子區塊樣式 */
        .form-section {
            background: var(--bg-card);
            border-radius: var(--border-radius);
            padding: 14px;
            margin-bottom: 14px;
            box-shadow: var(--shadow-soft);
        }
        .section-title {
            font-size: 14px;
            font-weight: bold;
            color: var(--primary-dark);
            margin-bottom: 10px;
        }

        .grid-inputs {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }
        .input-group {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
        .input-group label {
            font-size: 12px;
            color: var(--text-main);
        }
        .input-group input[type="number"], .input-group input[type="text"] {
            border: 1px solid var(--primary-latte);
            border-radius: 8px;
            padding: 8px;
            font-size: 14px;
            background-color: var(--bg-cream);
            color: var(--text-main);
            outline: none;
        }

        /* 複選與單選排版 */
        .options-list {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        .option-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: var(--bg-cream);
            padding: 8px 12px;
            border-radius: 8px;
            cursor: pointer;
        }
        .option-item input {
            accent-color: var(--primary-dark);
        }

        /* 支出頁分類區塊 */
        .expense-sub-boxes {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            margin-top: 10px;
        }
        .sub-box-item {
            background: var(--bg-cream);
            border: 1px solid var(--primary-latte);
            padding: 12px;
            border-radius: 8px;
            text-align: center;
            font-size: 13px;
            cursor: pointer;
        }
        .sub-box-item.active {
            background: var(--accent-peach);
            border-color: var(--accent-warm);
            font-weight: bold;
        }

        /* 簡易計算機呈現 */
        .calc-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
            margin-top: 8px;
        }
        .calc-btn {
            background: var(--bg-cream);
            border: 1px solid var(--primary-latte);
            padding: 12px;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            text-align: center;
        }
        .calc-display {
            grid-column: span 4;
            background: #fff;
            border: 1px solid var(--primary-latte);
            padding: 10px;
            text-align: right;
            font-size: 18px;
            font-weight: bold;
            border-radius: 8px;
            margin-bottom: 4px;
            min-height: 42px;
        }

        /* 底部固定懸浮總價欄 Sticky Footer */
        .sticky-footer {
            position: absolute;
            bottom: 0; left: 0; right: 0;
            height: 70px;
            background: var(--bg-card);
            border-top: 1px solid var(--primary-latte);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 16px;
            z-index: 210;
        }
        .footer-total {
            font-size: 15px;
            font-weight: bold;
        }
        .footer-total span {
            font-size: 20px;
            color: var(--primary-dark);
        }
        .ok-btn {
            background-color: var(--primary-dark);
            color: #fff;
            border: none;
            padding: 10px 28px;
            border-radius: 20px;
            font-weight: bold;
            cursor: pointer;
        }

        /* 後台設定入口與區域 */
        .setting-toggle {
            text-align: center;
            font-size: 12px;
            color: var(--text-muted);
            text-decoration: underline;
            margin-top: 12px;
            cursor: pointer;
        }
        .admin-section {
            display: none;
            border-top: 2px dashed var(--primary-latte);
            margin-top: 16px;
            padding-top: 16px;
        }

        /* --- 頁面2: 總紀錄頁面樣式 --- */
        .all-records-list {
            margin-top: 16px;
        }
        .day-group {
            background: var(--bg-card);
            border-radius: var(--border-radius);
            padding: 14px;
            margin-bottom: 12px;
            box-shadow: var(--shadow-soft);
        }
        .day-group-title {
            font-size: 13px;
            font-weight: bold;
            color: var(--text-muted);
            margin-bottom: 6px;
            border-bottom: 1px solid var(--bg-cream);
            padding-bottom: 4px;
        }
        .page2-footer {
            position: fixed;
            bottom: 0; left: 0; right: 0;
            height: 60px;
            background: var(--bg-card);
            box-shadow: 0 -2px 10px rgba(0,0,0,0.05);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 20px;
            z-index: 80;
            border-top: 1px solid var(--accent-peach);
        }

        /* --- 頁面3: 報表頁面樣式 --- */
        .report-card {
            background: var(--bg-card);
            border-radius: var(--border-radius);
            padding: 16px;
            margin-top: 16px;
            box-shadow: var(--shadow-soft);
            text-align: center;
        }
        .chart-title {
            font-size: 15px;
            font-weight: bold;
            color: var(--primary-dark);
            margin-bottom: 12px;
        }
        /* CSS / SVG 純手工輕量圖表 */
        .pie-chart-svg {
            width: 160px;
            height: 160px;
            transform: rotate(-90deg);
            border-radius: 50%;
        }
        .chart-legend {
            display: flex;
            justify-content: center;
            gap: 16px;
            margin-top: 12px;
            font-size: 12px;
        }
        .legend-item { display: flex; align-items: center; gap: 4px; }
        .legend-color { width: 12px; height: 12px; border-radius: 3px; }

        .analysis-box {
            background: var(--bg-cream);
            border-radius: 8px;
            padding: 12px;
            margin-top: 14px;
            font-size: 14px;
            text-align: left;
        }
        .analysis-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 6px;
        }
        .analysis-val {
            font-weight: bold;
            color: var(--primary-dark);
        }

        /* 長條圖客流量 */
        .bar-chart-container {
            display: flex;
            align-items: flex-end;
            justify-content: space-between;
            height: 120px;
            padding: 10px 10px 0 10px;
            border-bottom: 2px solid var(--primary-latte);
            margin-top: 16px;
        }
        .bar-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            flex: 1;
        }
        .bar-pillar {
            width: 60%;
            background-color: var(--accent-warm);
            border-top-left-radius: 4px;
            border-top-right-radius: 4px;
            transition: height 0.5s ease;
            min-height: 2px;
        }
        .bar-label {
            font-size: 10px;
            color: var(--text-muted);
            margin-top: 4px;
        }
        .bar-val {
            font-size: 9px;
            margin-bottom: 2px;
        }
    </style>
</head>
<body>

    <div class="top-navbar">
        <button class="nav-btn active" onclick="switchPage('calendar-page', this)">月曆</button>
        <button class="nav-btn" onclick="switchPage('records-page', this)">總紀錄</button>
        <button class="nav-btn" onclick="switchPage('reports-page', this)">報表</button>
    </div>

    <div id="calendar-page" class="app-page active">
        <h2 class="shop-title">Jump baby shop</h2>
        
        <div class="calendar-container">
            <div class="calendar-header">
                <span id="calendar-month-year">2026 年 6.月</span>
            </div>
            <div class="calendar-grid" id="calendar-grid-days">
                </div>
        </div>

        <div class="daily-records-box">
            <div class="box-title" id="selected-date-label">當日收支紀錄</div>
            <ul class="record-list" id="daily-record-list-ui">
                </ul>
        </div>

        <button class="fab-btn" onclick="openBottomSheet()">+</button>
    </div>

    <div id="records-page" class="app-page">
        <div class="capsule-scroll" id="week-capsules-container">
            </div>

        <div class="all-records-list" id="all-records-container-ui">
            </div>

        <div class="page2-footer">
            <span style="font-weight: bold; font-size:14px;">區間淨利總計:</span>
            <span id="page2-total-amount-display" style="font-size: 18px; font-weight: bold;">$0</span>
        </div>
    </div>

    <div id="reports-page" class="app-page">
        <div class="capsule-scroll" style="justify-content: center;">
            <button class="capsule-btn" id="btn-report-day" onclick="switchReportType('day')">日報表</button>
            <button class="capsule-btn active" id="btn-report-month" onclick="switchReportType('month')">月報表</button>
            <button class="capsule-btn" id="btn-report-year" onclick="switchReportType('year')">年報表</button>
        </div>

        <div class="report-card">
            <div class="chart-title" id="report-chart-title">本月收支結構</div>
            <div style="display: flex; justify-content: center; position: relative;">
                <svg class="pie-chart-svg" viewBox="0 0 32 32">
                    <circle r="16" cx="16" cy="16" fill="#F3E1D3" />
                    <circle id="pie-slice-income" r="16" cx="16" cy="16" fill="transparent" stroke="#6C5441" stroke-width="32" stroke-dasharray="0 100" />
                </svg>
            </div>
            <div class="chart-legend">
                <div class="legend-item"><div class="legend-color" style="background:#6C5441;"></div>收入</div>
                <div class="legend-item"><div class="legend-color" style="background:#F3E1D3;"></div>支出</div>
            </div>

            <div class="analysis-box">
                <div class="analysis-row">
                    <span>總收入金額:</span>
                    <span class="analysis-val" id="rep-total-income">$0</span>
                </div>
                <div class="analysis-row">
                    <span>來客總數 (收入筆數):</span>
                    <span class="analysis-val" id="rep-customer-count">0 人</span>
                </div>
                <div class="analysis-row" style="border-top:1px dashed #E6D5C3; padding-top:4px; margin-top:4px;">
                    <span>客單價分析 (總收÷來客):</span>
                    <span class="analysis-val" id="rep-avg-price" style="color:#D9A079;">$0</span>
                </div>
            </div>
        </div>

        <div class="report-card" style="margin-bottom: 40px;">
            <div class="chart-title">每月客流量趨勢 (來客數)</div>
            <div class="bar-chart-container" id="bar-chart-flow">
                </div>
        </div>
    </div>


    <div class="sheet-overlay" id="sheet-overlay" onclick="closeBottomSheet()"></div>
    <div class="bottom-sheet" id="bottom-sheet">
        <div class="sheet-header">
            <div class="capsule-scroll" style="padding:0;">
                <button class="capsule-btn active" id="sheet-tab-income" onclick="switchSheetTab('income')">收入頁面</button>
                <button class="capsule-btn" id="sheet-tab-expense" onclick="switchSheetTab('expense')">支出頁面</button>
            </div>
            <button class="close-sheet" onclick="closeBottomSheet()">×</button>
        </div>

        <div class="sheet-body">
            <div style="font-size:13px; color:var(--text-muted); margin-bottom:10px; text-align:center;">
                記帳日期：<span id="sheet-selected-date-str" style="font-weight:bold; color:var(--primary-dark);">2026-06-10</span>
            </div>

            <div id="sheet-income-form">
                <div class="form-section">
                    <div class="section-title">基礎服飾類別金額 (單選填寫)</div>
                    <div class="grid-inputs">
                        <div class="input-group"><label>上衣 $</label><input type="number" id="inc-core-上衣" class="inc-core-calc" placeholder="0" oninput="calcIncomeTotal()"></div>
                        <div class="input-group"><label>褲子 $</label><input type="number" id="inc-core-褲子" class="inc-core-calc" placeholder="0" oninput="calcIncomeTotal()"></div>
                        <div class="input-group"><label>裙子 $</label><input type="number" id="inc-core-裙子" class="inc-core-calc" placeholder="0" oninput="calcIncomeTotal()"></div>
                        <div class="input-group"><label>套裝 $</label><input type="number" id="inc-core-套裝" class="inc-core-calc" placeholder="0" oninput="calcIncomeTotal()"></div>
                    </div>
                </div>

                <div class="form-section">
                    <div class="section-title">小禮物項目區 (可複選)</div>
                    <div class="options-list" id="container-inc-gift">
                        </div>
                </div>

                <div class="form-section">
                    <div class="section-title">包材區 (可複選)</div>
                    <div class="options-list" id="container-inc-pack">
                        </div>
                </div>

                <div class="form-section">
                    <div class="section-title">行銷與折扣區</div>
                    <div class="options-list">
                        <label class="option-item">
                            <span>無折扣</span>
                            <input type="radio" name="inc-discount" value="0" checked onclick="calcIncomeTotal()">
                        </label>
                        <label class="option-item">
                            <span>滿899免運 (折$60)</span>
                            <input type="radio" name="inc-discount" value="60" onclick="calcIncomeTotal()">
                        </label>
                        <label class="option-item">
                            <span>親友價 95 折</span>
                            <input type="radio" name="inc-discount" value="95%" onclick="calcIncomeTotal()">
                        </label>
                        <label class="option-item">
                            <span>折扣 10 元</span>
                            <input type="radio" name="inc-discount" value="10" onclick="calcIncomeTotal()">
                        </label>
                        <label class="option-item">
                            <span>折扣 20 元</span>
                            <input type="radio" name="inc-discount" value="20" onclick="calcIncomeTotal()">
                        </label>
                        <label class="option-item">
                            <span>折扣 30 元</span>
                            <input type="radio" name="inc-discount" value="30" onclick="calcIncomeTotal()">
                        </label>
                        <div class="input-group" style="margin-top:8px;">
                            <label>其他折讓金額 $</label>
                            <input type="number" id="inc-discount-other" placeholder="0" oninput="calcIncomeTotal()">
                        </div>
                    </div>
                </div>

                <div class="setting-toggle" onclick="toggleAdminSection()">⚙️ 開啟/關閉後台選項項目設定</div>
                <div class="admin-section" id="admin-setting-block">
                    <h4 style="font-size:13px; margin-bottom:6px;">新增自訂選項</h4>
                    <div class="grid-inputs" style="margin-bottom:8px;">
                        <div class="input-group">
                            <label>區域選擇</label>
                            <select id="adm-target-zone" style="padding:8px; border-radius:8px; border:1px solid var(--primary-latte);">
                                <option value="gift">小禮物項目區</option>
                                <option value="pack">包材區</option>
                            </select>
                        </div>
                        <div class="input-group"><label>項目名稱</label><input type="text" id="adm-item-name" placeholder="例如: 襪子"></div>
                        <div class="input-group"><label>金額 $</label><input type="number" id="adm-item-price" placeholder="30"></div>
                        <div class="input-group" style="justify-content: flex-end;"><button class="ok-btn" style="padding:8px; font-size:12px;" onclick="addCustomOption()">新增</button></div>
                    </div>
                    <p style="font-size:11px; color:var(--text-muted);">* 註：系統內建基礎選項亦可在程式碼或由此處動態調整。</p>
                </div>
            </div>

            <div id="sheet-expense-form" style="display:none;">
                <div class="capsule-scroll">
                    <button class="capsule-btn active" id="exp-cat-進貨" onclick="switchExpenseCat('進貨')">進貨</button>
                    <button class="capsule-btn" id="exp-cat-設備" onclick="switchExpenseCat('設備')">設備</button>
                    <button class="capsule-btn" id="exp-cat-工作室營運" onclick="switchExpenseCat('工作室營運')">工作室營運</button>
                    <button class="capsule-btn" id="exp-cat-行銷與雜支" onclick="switchExpenseCat('行銷與雜支')">行銷與雜支</button>
                </div>

                <div class="form-section" style="margin-top:12px;">
                    <div class="section-title">選擇明細項目</div>
                    <div class="expense-sub-boxes" id="expense-sub-boxes-container">
                        </div>
                    <div class="input-group" style="margin-top:10px; display:none;" id="exp-other-input-group">
                        <label>其他項目說明 (Text)</label>
                        <input type="text" id="exp-other-text" placeholder="請輸入說明">
                    </div>
                </div>

                <div class="form-section">
                    <div class="section-title">金額輸入計算機</div>
                    <div class="calc-display" id="calc-screen">0</div>
                    <div class="calc-container">
                        <button class="calc-btn" onclick="pressCalc('7')">7</button>
                        <button class="calc-btn" onclick="pressCalc('8')">8</button>
                        <button class="calc-btn" onclick="pressCalc('9')">9</button>
                        <button class="calc-btn" style="background:var(--accent-peach);" onclick="pressCalc('+')">+</button>
                        
                        <button class="calc-btn" onclick="pressCalc('4')">4</button>
                        <button class="calc-btn" onclick="pressCalc('5')">5</button>
                        <button class="calc-btn" onclick="pressCalc('6')">6</button>
                        <button class="calc-btn" style="background:var(--accent-peach);" onclick="pressCalc('-')">-</button>
                        
                        <button class="calc-btn" onclick="pressCalc('1')">1</button>
                        <button class="calc-btn" onclick="pressCalc('2')">2</button>
                        <button class="calc-btn" onclick="pressCalc('3')">3</button>
                        <button class="calc-btn" style="background:var(--primary-latte);" onclick="pressCalc('C')">C</button>
                        
                        <button class="calc-btn" style="grid-column: span 2;" onclick="pressCalc('0')">0</button>
                        <button class="calc-btn" style="grid-column: span 2; background:var(--accent-warm);" onclick="pressCalc('=')">=</button>
                    </div>
                </div>
            </div>

        </div>

        <div class="sticky-footer">
            <div class="footer-total">
                即時總計: $<span id="sheet-sticky-total">0</span>
            </div>
            <button class="ok-btn" onclick="submitAccountingRecord()">OK</button>
        </div>
    </div>

    <script>
        /* ================= 全局核心資料結構 ================= */
        let configData = {
            gift: [
                { name: "小髮飾", price: 20 },
                { name: "髮帶", price: 20 },
                { name: "小車車", price: 30 },
                { name: "圍兜", price: 40 },
                { name: "襪子", price: 35 }
            ],
            pack: [
                { name: "破壞袋", price: 4 },
                { name: "紙箱", price: 15 },
                { name: "緞帶", price: 4 },
                { name: "防塵袋", price: 5 },
                { name: "名片", price: 2 },
                { name: "Logo貼紙", price: 2 }
            ]
        };

        const expenseCategoryMap = {
            "進貨": ["破壞袋", "防塵袋", "緞帶", "紙箱", "名片", "貼紙", "其他"],
            "設備": ["展示架", "衣架", "燈光設備", "其他"],
            "工作室營運": ["房租", "水電費", "文具", "其他"],
            "行銷與雜支": ["廣告費用", "活動費用", "其他"]
        };

        let accountingRecords = [];
        let currentDateInstance = new Date();
        let selectedDateStr = "";
        let currentSheetTab = "income";
        let currentExpenseCat = "進貨";
        let currentExpenseSub = "";
        let calcInputBuffer = "0";

        /* ================= 初始化啟動 ================= */
        window.addEventListener('load', () => {
            if(localStorage.getItem('jump_baby_config')) {
                configData = JSON.parse(localStorage.getItem('jump_baby_config'));
            }
            if(localStorage.getItem('jump_baby_records')) {
                accountingRecords = JSON.parse(localStorage.getItem('jump_baby_records'));
            }

            const y = currentDateInstance.getFullYear();
            const m = String(currentDateInstance.getMonth() + 1).padStart(2, '0');
            const d = String(currentDateInstance.getDate()).padStart(2, '0');
            selectedDateStr = `${y}-${m}-${d}`;

            initCalendar();
            renderDailyRecords();
            initSheetOptions();
            initWeekCapsules();
            updateReportUI();
        });

        /* ================= 系統共用邏輯與頁面切換 ================= */
        function switchPage(pageId, btnEl) {
            document.querySelectorAll('.app-page').forEach(p => p.classList.remove('active'));
            document.querySelectorAll('.top-navbar .nav-btn').forEach(b => b.classList.remove('active'));
            
            document.getElementById(pageId).classList.add('active');
            btnEl.classList.add('active');

            if(pageId === 'records-page') {
                renderWeekRecords();
            } else if(pageId === 'reports-page') {
                updateReportUI();
            } else if(pageId === 'calendar-page') {
                initCalendar();
                renderDailyRecords();
            }
        }

        function saveToLocalStorage() {
            localStorage.setItem('jump_baby_config', JSON.stringify(configData));
            localStorage.setItem('jump_baby_records', JSON.stringify(accountingRecords));
        }

        /* ================= 頁面1：月曆核心渲染機制 ================= */
        function initCalendar() {
            const year = currentDateInstance.getFullYear();
            const month = currentDateInstance.getMonth();
            
            document.getElementById('calendar-month-year').innerText = `${year} 年 ${month + 1} 月`;

            const gridContainer = document.getElementById('calendar-grid-days');
            gridContainer.innerHTML = '';

            const weekDays = ['日', '一', '二', '三', '四', '五', '六'];
            weekDays.forEach(wd => {
                const el = document.createElement('div');
                el.className = 'weekday';
                el.innerText = wd;
                gridContainer.appendChild(el);
            });

            const firstDayIndex = new Date(year, month, 1).getDay();
            const totalDays = new Date(year, month + 1, 0).getDate();

            for (let i = 0; i < firstDayIndex; i++) {
                const emptyCell = document.createElement('div');
                emptyCell.className = 'calendar-day empty';
                gridContainer.appendChild(emptyCell);
            }

            const todayObj = new Date();
            const todayStr = `${todayObj.getFullYear()}-${String(todayObj.getMonth()+1).padStart(2,'0')}-${String(todayObj.getDate()).padStart(2,'0')}`;

            for (let day = 1; day <= totalDays; day++) {
                const dayCell = document.createElement('div');
                dayCell.className = 'calendar-day';
                
                const thisDateStr = `${year}-${String(month + 1).padStart(2, '0')}-${String(day).padStart(2, '0')}`;
                dayCell.dataset.date = thisDateStr;

                const span = document.createElement('span');
                span.innerText = day;
                dayCell.appendChild(span);

                if (thisDateStr === todayStr) {
                    dayCell.classList.add('today');
                }
                if (thisDateStr === selectedDateStr) {
                    dayCell.classList.add('selected');
                }

                dayCell.onclick = function() {
                    document.querySelectorAll('.calendar-day').forEach(c => c.classList.remove('selected'));
                    this.classList.add('selected');
                    selectedDateStr = this.dataset.date;
                    renderDailyRecords();
                };

                gridContainer.appendChild(dayCell);
            }
        }

        function renderDailyRecords() {
            document.getElementById('selected-date-label').innerText = `${selectedDateStr} 收支明細`;
            const listUi = document.getElementById('daily-record-list-ui');
            listUi.innerHTML = '';

            const dayRecords = accountingRecords.filter(r => r.date === selectedDateStr);

            if(dayRecords.length === 0) {
                listUi.innerHTML = `<li style="color:var(--text-muted); font-size:13px; text-align:center; padding: 20px 0;">當日尚無任何記帳紀錄 🍵</li>`;
                return;
            }

            dayRecords.forEach(rec => {
                const li = document.createElement('li');
                li.className = 'record-item';
                
                const typeSign = rec.type === 'income' ? '+' : '-';
                const typeClass = rec.type === 'income' ? 'amt-income' : 'amt-expense';

                li.innerHTML = `
                    <div class="record-info">
                        <strong style="color:var(--primary-dark);">${rec.type === 'income'?'[入]':'[支]'} ${rec.desc}</strong>
                    </div>
                    <span class="record-amount ${typeClass}">${typeSign}$${rec.amount}</span>
                    <button class="delete-btn" onclick="deleteRecordItem(${rec.id})">🗑️</button>
                `;
                listUi.appendChild(li);
            });
        }

        function deleteRecordItem(id) {
            if(confirm("確定要刪除這筆記帳紀錄嗎？")) {
                accountingRecords = accountingRecords.filter(r => r.id !== id);
                saveToLocalStorage();
                renderDailyRecords();
                updateReportUI();
            }
        }

        /* ================= 底部滑出記帳面板邏輯 (Bottom Sheet) ================= */
        function openBottomSheet() {
            document.getElementById('sheet-selected-date-str').innerText = selectedDateStr;
            document.getElementById('sheet-overlay').style.display = 'block';
            document.getElementById('bottom-sheet').classList.add('open');
            resetIncomeFormFields();
            resetExpenseFormFields();
            switchSheetTab(currentSheetTab);
        }

        function closeBottomSheet() {
            document.getElementById('sheet-overlay').style.display = 'none';
            document.getElementById('bottom-sheet').classList.remove('open');
        }

        function switchSheetTab(tab) {
            currentSheetTab = tab;
            document.getElementById('sheet-tab-income').classList.remove('active');
            document.getElementById('sheet-tab-expense').classList.remove('active');
            
            if(tab === 'income') {
                document.getElementById('sheet-tab-income').classList.add('active');
                document.getElementById('sheet-income-form').style.display = 'block';
                document.getElementById('sheet-expense-form').style.display = 'none';
                calcIncomeTotal();
            } else {
                document.getElementById('sheet-tab-expense').classList.add('active');
                document.getElementById('sheet-income-form').style.display = 'none';
                document.getElementById('sheet-expense-form').style.display = 'block';
                switchExpenseCat(currentExpenseCat);
                calcExpenseTotal();
            }
        }

        /* ----- 收入頁面核心處理與後台渲染 ----- */
        function initSheetOptions() {
            const giftContainer = document.getElementById('container-inc-gift');
            giftContainer.innerHTML = '';
            configData.gift.forEach((g, index) => {
                giftContainer.innerHTML += `
                    <label class="option-item">
                        <span>${g.name} ($${g.price})</span>
                        <input type="checkbox" class="inc-gift-cb" data-price="${g.price}" data-name="${g.name}" onchange="calcIncomeTotal()">
                    </label>
                `;
            });

            const packContainer = document.getElementById('container-inc-pack');
            packContainer.innerHTML = '';
            configData.pack.forEach((p, index) => {
                packContainer.innerHTML += `
                    <label class="option-item">
                        <span>${p.name} ($${p.price})</span>
                        <input type="checkbox" class="inc-pack-cb" data-price="${p.price}" data-name="${p.name}" onchange="calcIncomeTotal()">
                    </label>
                `;
            });
        }

        function calcIncomeTotal() {
            if(currentSheetTab !== 'income') return;

            let subtotal = 0;
            
            document.querySelectorAll('.inc-core-calc').forEach(input => {
                const val = parseFloat(input.value) || 0;
                subtotal += val;
            });

            document.querySelectorAll('.inc-gift-cb:checked').forEach(cb => {
                subtotal -= parseFloat(cb.dataset.price) || 0;
            });

            document.querySelectorAll('.inc-pack-cb:checked').forEach(cb => {
                subtotal -= parseFloat(cb.dataset.price) || 0;
            });

            let finalTotal = subtotal;
            const checkedDiscount = document.querySelector('input[name="inc-discount"]:checked');
            if(checkedDiscount) {
                const discVal = checkedDiscount.value;
                if(discVal === '95%') {
                    finalTotal = subtotal * 0.95;
                } else {
                    finalTotal -= parseFloat(discVal) || 0;
                }
            }

            const otherDisc = parseFloat(document.getElementById('inc-discount-other').value) || 0;
            finalTotal -= otherDisc;

            if(finalTotal < 0) finalTotal = 0;
            finalTotal = Math.round(finalTotal);

            document.getElementById('sheet-sticky-total').innerText = finalTotal;
            return finalTotal;
        }

        function resetIncomeFormFields() {
            document.querySelectorAll('.inc-core-calc').forEach(i => i.value = '');
            document.querySelectorAll('.inc-gift-cb').forEach(c => c.checked = false);
            document.querySelectorAll('.inc-pack-cb').forEach(c => c.checked = false);
            const firstDisc = document.querySelector('input[name="inc-discount"]');
            if(firstDisc) firstDisc.checked = true;
            document.getElementById('inc-discount-other').value = '';
        }

        function toggleAdminSection() {
            const block = document.getElementById('admin-setting-block');
            block.style.display = block.style.display === 'block' ? 'none' : 'block';
        }

        function addCustomOption() {
            const zone = document.getElementById('adm-target-zone').value;
            const name = document.getElementById('adm-item-name').value.trim();
            const price = parseFloat(document.getElementById('adm-item-price').value) || 0;

            if(!name) { alert("請輸入項目名稱"); return; }

            configData[zone].push({ name: name, price: price });
            saveToLocalStorage();
            initSheetOptions();
            
            document.getElementById('adm-item-name').value = '';
            document.getElementById('adm-item-price').value = '';
            alert("新增成功！");
        }

        /* ----- 支出頁面核心處理 ----- */
        function switchExpenseCat(catName) {
            currentExpenseCat = catName;
            const cats = ["進貨", "設備", "工作室營運", "行銷與雜支"];
            cats.forEach(c => {
                const btn = document.getElementById(`exp-cat-${c}`);
                if(btn) {
                    if(c === catName) btn.classList.add('active');
                    else btn.classList.remove('active');
                }
            });

            const subContainer = document.getElementById('expense-sub-boxes-container');
            subContainer.innerHTML = '';
            
            const subItems = expenseCategoryMap[catName] || [];
            subItems.forEach((sub, idx) => {
                const itemDiv = document.createElement('div');
                itemDiv.className = 'sub-box-item';
                if(idx === 0) {
                    itemDiv.classList.add('active');
                    currentExpenseSub = sub;
                }
                itemDiv.innerText = sub;
                itemDiv.onclick = function() {
                    document.querySelectorAll('.sub-box-item').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    currentExpenseSub = sub;
                    
                    const otherGroup = document.getElementById('exp-other-input-group');
                    if(sub === '其他') {
                        otherGroup.style.display = 'block';
                    } else {
                        otherGroup.style.display = 'none';
                    }
                };
                subContainer.appendChild(itemDiv);
            });

            document.getElementById('exp-other-input-group').style.display = 'none';
        }

        function pressCalc(val) {
            const screen = document.getElementById('calc-screen');
            
            if (val === 'C') {
                calcInputBuffer = "0";
            } else if (val === '=') {
                try {
                    let sanitized = calcInputBuffer.replace(/[^0-9+\-*/.]/g, '');
                    let res = Function(`"use strict"; return (${sanitized})`)();
                    calcInputBuffer = String(res || 0);
                } catch(e) {
                    calcInputBuffer = "錯誤";
                }
            } else {
                if (calcInputBuffer === "0" && val !== '+' && val !== '-') {
                    calcInputBuffer = val;
                } else {
                    calcInputBuffer += val;
                }
            }
            screen.innerText = calcInputBuffer;
            calcExpenseTotal();
        }

        function calcExpenseTotal() {
            if(currentSheetTab !== 'expense') return;
            let val = parseFloat(calcInputBuffer) || 0;
            if(val < 0) val = 0;
            document.getElementById('sheet-sticky-total').innerText = Math.round(val);
        }

        function resetExpenseFormFields() {
            calcInputBuffer = "0";
            document.getElementById('calc-screen').innerText = "0";
            document.getElementById('exp-other-text').value = '';
            currentExpenseCat = "進貨";
            currentExpenseSub = "破壞袋";
        }

        /* ----- 送出與儲存記帳資料 ----- */
        function submitAccountingRecord() {
            const finalAmt = parseFloat(document.getElementById('sheet-sticky-total').innerText) || 0;
            
            if(finalAmt <= 0) {
                if(!confirm("目前金額為 0，確定要送出此筆紀錄嗎？")) return;
            }

            let description = "";
            
            if(currentSheetTab === 'income') {
                let itemsParts = [];
                document.querySelectorAll('.inc-core-calc').forEach(i => {
                    if(parseFloat(i.value) > 0) itemsParts.push(`${i.id.replace('inc-core-','')}`);
                });
                document.querySelectorAll('.inc-gift-cb:checked').forEach(cb => {
                    itemsParts.push(cb.dataset.name);
                });
                document.querySelectorAll('.inc-pack-cb:checked').forEach(cb => {
                    itemsParts.push(cb.dataset.name);
                });
                
                description = itemsParts.length > 0 ? itemsParts.join('+') : "童裝服飾收入";
            } else {
                if(currentExpenseSub === '其他') {
                    const extraTxt = document.getElementById('exp-other-text').value.trim();
                    description = `[${currentExpenseCat}] 其他-${extraTxt || '未分類'}`;
                } else {
                    description = `[${currentExpenseCat}] ${currentExpenseSub}`;
                }
            }

            const newRecord = {
                id: Date.now(),
                date: selectedDateStr,
                type: currentSheetTab,
                desc: description,
                amount: finalAmt
            };

            accountingRecords.push(newRecord);
            saveToLocalStorage();
            
            closeBottomSheet();
            renderDailyRecords();
            updateReportUI();
            
            alert("記帳完成！❤️");
        }

        /* ================= 頁面2：總紀錄頁面 (週滑動膠囊) ================= */
        let currentWeekOffset = 0;

        function initWeekCapsules() {
            const container = document.getElementById('week-capsules-container');
            container.innerHTML = '';

            for(let offset = -2; offset <= 2; offset++) {
                const btn = document.createElement('button');
                btn.className = `capsule-btn ${offset === currentWeekOffset ? 'active' : ''}`;
                
                let label = "";
                if(offset === 0) label = "本週紀錄";
                else if(offset === -1) label = "上一週";
                else if(offset === 1) label = "下一週";
                else if(offset < 0) label = `前 ${Math.abs(offset)} 週`;
                else label = `後 ${offset} 週`;

                btn.onclick = function() {
                    currentWeekOffset = offset;
                    document.querySelectorAll('#week-capsules-container .capsule-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    renderWeekRecords();
                };
                btn.innerText = label;
                container.appendChild(btn);
            }
        }

        function getTargetDateRange(offset) {
            const today = new Date();
            const dayOfWeek = today.getDay();
            
            const startOfWeek = new Date(today);
            startOfWeek.setDate(today.getDate() - dayOfWeek + (offset * 7));
            
            const endOfWeek = new Date(startOfWeek);
            endOfWeek.setDate(startOfWeek.getDate() + 6);

            return { start: startOfWeek, end: endOfWeek };
        }

        function renderWeekRecords() {
            const container = document.getElementById('all-records-container-ui');
            container.innerHTML = '';

            const range = getTargetDateRange(currentWeekOffset);
            
            const filteredRecords = accountingRecords.filter(r => {
                const rDate = new Date(r.date);
                rDate.setHours(0,0,0,0);
                const s = new Date(range.start).setHours(0,0,0,0);
                const e = new Date(range.end).setHours(0,0,0,0);
                return rDate >= s && rDate <= e;
            });

            const groups = {};
            filteredRecords.forEach(r => {
                if(!groups[r.date]) groups[r.date] = [];
                groups[r.date].push(r);
            });

            const sortedDates = Object.keys(groups).sort((a,b) => new Date(b) - new Date(a));

            if(sortedDates.length === 0) {
                container.innerHTML = `<div style="text-align:center; color:var(--text-muted); padding:40px 0; font-size:14px;">該區間無收支記帳明細</div>`;
                document.getElementById('page2-total-amount-display').innerText = "$0";
                document.getElementById('page2-total-amount-display').style.color = "var(--primary-dark)";
                return;
            }

            let rangeNetProfit = 0;

            sortedDates.forEach(dStr => {
                const dayDiv = document.createElement('div');
                dayDiv.className = 'day-group';
                
                let html = `<div class="day-group-title">${dStr}</div><ul class="record-list">`;
                
                groups[dStr].forEach(rec => {
                    const isInc = rec.type === 'income';
                    rangeNetProfit += isInc ? rec.amount : -rec.amount;

                    html += `
                        <li class="record-item" style="padding: 6px 0;">
                            <div class="record-info"><span>${isInc?'[入]':'[支]'} ${rec.desc}</span></div>
                            <span class="record-amount ${isInc?'amt-income':'amt-expense'}">
                                ${isInc?'+':'-'}$${rec.amount}
                            </span>
                        </li>
                    `;
                });
                html += `</ul>`;
                dayDiv.innerHTML = html;
                container.appendChild(dayDiv);
            });

            const totalDisplay = document.getElementById('page2-total-amount-display');
            if(rangeNetProfit >= 0) {
                totalDisplay.innerText = `+$${rangeNetProfit}`;
                totalDisplay.style.color = "var(--success)";
            } else {
                totalDisplay.innerText = `-$${Math.abs(rangeNetProfit)}`;
                totalDisplay.style.color = "var(--danger)";
            }
        }

        /* ================= 頁面3：報表與客單、客流分析 ================= */
        let currentReportType = 'month';

        function switchReportType(type) {
            currentReportType = type;
            document.getElementById('btn-report-day').classList.remove('active');
            document.getElementById('btn-report-month').classList.remove('active');
            document.getElementById('btn-report-year').classList.remove('active');
            document.getElementById(`btn-report-${type}`).classList.add('active');
            updateReportUI();
        }

        function updateReportUI() {
            const today = new Date();
            const yStr = String(today.getFullYear());
            const mStr = String(today.getMonth() + 1).padStart(2, '0');
            const dStr = `${yStr}-${mStr}-${String(today.getDate()).padStart(2, '0')}`;

            let titleText = "";
            let targetRecords = [];

            if(currentReportType === 'day') {
                titleText = `今日收支結構 (${yStr}-${mStr}-${today.getDate()})`;
                targetRecords = accountingRecords.filter(r => r.date === dStr);
            } else if(currentReportType === 'month') {
                titleText = `本月收支結構 (${yStr}年${mStr}月)`;
                targetRecords = accountingRecords.filter(r => r.date.startsWith(`${yStr}-${mStr}`));
            } else {
                titleText = `今年收支結構 (${yStr}年度)`;
                targetRecords = accountingRecords.filter(r => r.date.startsWith(yStr));
            }

            document.getElementById('report-chart-title').innerText = titleText;

            let totalIncome = 0;
            let totalExpense = 0;
            let customerCount = 0;

            targetRecords.forEach(r => {
                if(r.type === 'income') {
                    totalIncome += r.amount;
                    customerCount++;
                } else {
                    totalExpense += r.amount;
                }
            });

            document.getElementById('rep-total-income').innerText = `$${totalIncome}`;
            document.getElementById('rep-customer-count').innerText = `${customerCount} 人`;
            const avgPrice = customerCount > 0 ? Math.round(totalIncome / customerCount) : 0;
            document.getElementById('rep-avg-price').innerText = `$${avgPrice}`;

            const totalSum = totalIncome + totalExpense;
            const sliceIncome = document.getElementById('pie-slice-income');
            
            if(totalSum === 0) {
                sliceIncome.setAttribute('stroke-dasharray', `0 100`);
            } else {
                const incomePercentage = Math.round((totalIncome / totalSum) * 100);
                sliceIncome.setAttribute('stroke-dasharray', `${incomePercentage} 100`);
            }

            renderCustomerFlowChart(yStr);
        }

        function renderCustomerFlowChart(currentYear) {
            const chartContainer = document.getElementById('bar-chart-flow');
            chartContainer.innerHTML = '';

            const monthlyCounts = Array(12).fill(0);

            accountingRecords.forEach(r => {
                if(r.type === 'income' && r.date.startsWith(currentYear)) {
                    const parts = r.date.split('-');
                    const monthIdx = parseInt(parts[1], 10) - 1;
                    if(monthIdx >= 0 && monthIdx < 12) {
                        monthlyCounts[monthIdx]++;
                    }
                }
            });

            const maxCount = Math.max(...monthlyCounts, 5);

            for(let m = 1; m <= 12; m++) {
                const count = monthlyCounts[m-1];
                const heightPercent = (count / maxCount) * 100;

                const barItem = document.createElement('div');
                barItem.className = 'bar-item';
                barItem.innerHTML = `
                    <span class="bar-val" style="color:${count>0?'var(--primary-dark)':'var(--text-muted)'}">${count}</span>
                    <div class="bar-pillar" style="height: ${heightPercent}%;"></div>
                    <span class="bar-label">${m}月</span>
                `;
                chartContainer.appendChild(barItem);
            }
        }
    </script>
</body>
</html>
