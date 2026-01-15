<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsversion='3' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
    <title>Professional Ad Bot</title>
    <meta content='width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no' name='viewport'/>
    
    <script src='https://adsmone.com/cdn/ads.js?app_uid=5738' type='text/javascript'/>
    <script src='https://telegram.org/js/telegram-web-app.js' type='text/javascript'/>

    <b:skin><![CDATA[
        body { background: #f0f2f5; color: #1c1e21; font-family: 'Segoe UI', sans-serif; margin: 0; padding: 20px 0 100px 0; display: flex; flex-direction: column; align-items: center; }
        
        /* Dashboard Box - Premium Style */
        .dashboard-card { width: 90%; max-width: 400px; background: #ffffff; border-radius: 12px; padding: 20px; box-shadow: 0 2px 12px rgba(0,0,0,0.08); margin-bottom: 25px; border: 1px solid #e4e6eb; }
        .dash-row { display: flex; justify-content: space-between; margin-bottom: 15px; }
        .stat-box { flex: 1; }
        .label { font-size: 11px; color: #65676b; font-weight: 700; text-transform: uppercase; letter-spacing: 0.5px; }
        .value { font-size: 18px; font-weight: 700; display: block; margin-top: 2px; }
        .timer { color: #d63031; }

        .control-panel { width: 90%; max-width: 400px; background: #ffffff; border-radius: 12px; padding: 10px; box-shadow: 0 2px 12px rgba(0,0,0,0.08); display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        .action-btn { background: #f0f2f5; border: none; padding: 20px 10px; border-radius: 8px; cursor: pointer; font-size: 13px; font-weight: 600; color: #1c1e21; }
        .primary { background: #0084ff; color: #fff; grid-column: span 2; padding: 15px; font-size: 15px; }
        .primary:disabled { background: #bcc0c4; cursor: not-allowed; }
    ]]></b:skin>
</head>

<body>
    <div class='dashboard-card'>
        <div class='dash-row'>
            <div class='stat-box'>
                <span class='label'>Today&#39;s Add Watch</span>
                <span class='value' id='p-count'>0</span>
            </div>
            <div class='stat-box' style='text-align: right;'>
                <span class='label'>Rest Time</span>
                <span class='value timer' id='rest-timer'>00:00:00</span>
            </div>
        </div>
        <div class='dash-row' style='margin-bottom:0; padding-top:10px; border-top:1px solid #eee;'>
            <div class='stat-box'>
                <span class='label'>Hourly Limit</span>
                <span class='value' style='font-size:14px;'><span id='h-count'>0</span> / 20</span>
            </div>
            <div class='stat-box' style='text-align: right;'>
                <span class='label'>Safety Status</span>
                <span class='value' id='status-text' style='color:#2ecc71; font-size:14px;'>Secure</span>
            </div>
        </div>
    </div>

    <div class='control-panel'>
        <button class='action-btn primary' id='watch-btn' onclick='playAd()'>Watch Advertisement</button>
        <button class='action-btn' onclick='openWithdraw()'>💰 Withdraw</button>
        <button class='action-btn' onclick='alert("Coming Soon")'>📜 History</button>
    </div>

    <script type='text/javascript'>
    // <![CDATA[
        const tg = window.Telegram.WebApp;
        let data = { ads: 0, hourly: 0, lastHour: new Date().getHours(), lastResetDate: "" };

        const saved = localStorage.getItem('pro_bot_v2');
        if(saved) data = JSON.parse(saved);

        function updateUI() {
            // Check if hour changed to reset hourly limit
            const currentHour = new Date().getHours();
            if (data.lastHour !== currentHour) {
                data.hourly = 0;
                data.lastHour = currentHour;
            }

            document.getElementById('p-count').innerText = data.ads;
            document.getElementById('h-count').innerText = data.hourly;
            
            const btn = document.getElementById('watch-btn');
            const status = document.getElementById('status-text');

            if (data.hourly >= 20 || data.ads >= 100) {
                btn.disabled = true;
                btn.innerText = "Limit Reached";
                status.innerText = "Resting";
                status.style.color = "#d63031";
            } else {
                btn.disabled = false;
                btn.innerText = "Watch Advertisement";
                status.innerText = "Secure";
                status.style.color = "#2ecc71";
            }
            localStorage.setItem('pro_bot_v2', JSON.stringify(data));
        }

        function playAd() {
            if (typeof window.showAdsmone === 'function') {
                window.showAdsmone().then(() => { 
                    data.ads++; data.hourly++; updateUI(); 
                }).catch(() => { alert("Ad closed early."); });
            }
        }

        function runTimer() {
            const now = new Date();
            const bd = new Date(now.toLocaleString("en-US", {timeZone: "Asia/Dhaka"}));
            let target = new Date(bd); target.setHours(10, 0, 0, 0);
            if (bd >= target && data.lastResetDate !== bd.toDateString()) {
                data.ads = 0; data.hourly = 0; data.lastResetDate = bd.toDateString(); updateUI();
            }
            if(bd >= target) target.setDate(target.getDate() + 1);
            const diff = target - bd;
            const h = Math.floor(diff/3600000), m = Math.floor((diff%3600000)/60000), s = Math.floor((diff%60000)/1000);
            document.getElementById('rest-timer').innerText = `${h.toString().padStart(2,'0')}:${m.toString().padStart(2,'0')}:${s.toString().padStart(2,'0')}`;
        }

        updateUI();
        setInterval(runTimer, 1000);
        tg.expand();
    // ]]>
    </script>
</body>
</html>
