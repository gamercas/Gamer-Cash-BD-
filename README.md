<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GamerCash BD | AI Earning Master</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body { background: #070b14; color: white; font-family: 'Inter', sans-serif; overflow-x: hidden; }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(10px); border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 15px; }
        .neon-border { border: 1px solid #3b82f6; box-shadow: 0 0 10px #3b82f644; }
        .page { display: none; padding-bottom: 100px; }
        .active { display: block; animation: slideUp 0.3s ease-out; }
        @keyframes slideUp { from { transform: translateY(20px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        .nav-active { color: #3b82f6 !important; text-shadow: 0 0 10px #3b82f6; }
    </style>
</head>
<body>

    <div id="security-overlay" class="fixed inset-0 bg-black z-[100] hidden flex-col items-center justify-center text-center p-6">
        <i class="fas fa-user-shield text-6xl text-red-500 mb-4"></i>
        <h1 class="text-2xl font-bold text-red-500">Access Denied!</h1>
        <p id="security-msg" class="text-gray-400 mt-2">VPN or Cheat Detected. Please disable VPN or stop cheating to continue.</p>
    </div>

    <header class="p-6 flex justify-between items-center sticky top-0 bg-[#070b14]/90 z-40">
        <div>
            <h1 class="text-xl font-black text-blue-500 italic">GAMERCASH BD</h1>
            <p class="text-[10px] text-gray-500">ID: gamer-cash-bd-4bc97</p>
        </div>
        <div class="glass px-4 py-2 flex items-center gap-2">
            <i class="fas fa-wallet text-yellow-500"></i>
            <span id="balance" class="font-bold text-lg">1250</span>
        </div>
    </header>

    <main class="px-5">
        <div id="home" class="page active space-y-5">
            <div class="glass p-5 flex justify-around text-center">
                <div><p class="text-xs text-gray-500 italic">Earnings</p><p class="text-xl font-bold text-blue-400">৳ 540</p></div>
                <div class="border-l border-white/10 px-6"><p class="text-xs text-gray-500 italic">Tasks Done</p><p class="text-xl font-bold text-green-400">45/200</p></div>
            </div>
            
            <div class="grid grid-cols-2 gap-4">
                <div onclick="showPage('tasks')" class="glass p-6 text-center cursor-pointer border-b-2 border-blue-500">
                    <i class="fas fa-layer-group text-3xl mb-2 text-blue-500"></i>
                    <p class="font-bold">Tasks</p>
                </div>
                <div onclick="showPage('spin')" class="glass p-6 text-center cursor-pointer border-b-2 border-purple-500">
                    <i class="fas fa-dharmachakra text-3xl mb-2 text-purple-500"></i>
                    <p class="font-bold">Mega Spin</p>
                </div>
            </div>
        </div>

        <div id="tasks" class="page space-y-4">
            <div class="bg-blue-600/10 p-3 rounded-lg text-sm text-blue-400 flex items-center gap-2">
                <i class="fas fa-info-circle"></i> Don't skip ads! AI is watching your timer.
            </div>
            <div id="task-container" class="space-y-3">
                </div>
        </div>

        <div id="wallet" class="page space-y-5">
            <h2 class="text-xl font-bold">Withdraw Methods</h2>
            <div class="grid grid-cols-2 gap-3">
                <div class="glass p-4 text-center cursor-pointer hover:neon-border" onclick="selectMethod('bKash')">bKash</div>
                <div class="glass p-4 text-center cursor-pointer hover:neon-border" onclick="selectMethod('Free Fire')">Free Fire UID</div>
            </div>
            <div id="withdraw-box" class="glass p-5 space-y-4 hidden">
                <p id="method-title" class="text-blue-500 font-bold">Withdraw via bKash</p>
                <input type="text" id="acc-num" placeholder="Enter details..." class="w-full bg-white/5 p-3 rounded-lg outline-none border border-white/10">
                <button onclick="processWithdraw()" class="w-full bg-blue-600 py-3 rounded-lg font-bold">Confirm Withdraw</button>
            </div>
        </div>

        <div id="profile" class="page space-y-5">
            <div class="glass p-6 text-center">
                <div class="w-20 h-20 bg-blue-600 rounded-full mx-auto mb-3 flex items-center justify-center text-3xl">G</div>
                <h3 class="font-bold">Gamer Master</h3>
                <p class="text-sm text-gray-500">animetixb@gmail.com</p>
            </div>
            <div class="glass p-5">
                <p class="text-sm text-gray-400 mb-2">Invite Link:</p>
                <div class="bg-black/40 p-3 rounded flex justify-between items-center">
                    <code class="text-blue-400">gamercash.bd/ref?id=4bc97</code>
                    <i class="fas fa-copy cursor-pointer"></i>
                </div>
            </div>
        </div>
    </main>

    <nav class="fixed bottom-0 left-0 right-0 bg-[#070b14]/90 border-t border-white/10 p-4 flex justify-around z-50">
        <button onclick="showPage('home')" id="nav-home" class="text-gray-500 nav-active flex flex-col items-center"><i class="fas fa-home"></i><span class="text-[10px]">Home</span></button>
        <button onclick="showPage('tasks')" id="nav-tasks" class="text-gray-500 flex flex-col items-center"><i class="fas fa-tasks"></i><span class="text-[10px]">Tasks</span></button>
        <button onclick="showPage('wallet')" id="nav-wallet" class="text-gray-500 flex flex-col items-center"><i class="fas fa-wallet"></i><span class="text-[10px]">Wallet</span></button>
        <button onclick="showPage('profile')" id="nav-profile" class="text-gray-500 flex flex-col items-center"><i class="fas fa-user"></i><span class="text-[10px]">Profile</span></button>
    </nav>

    <script>
        let balance = 1250;
        let lastClickTime = 0;

        // 1. AI Security: VPN Detection (Simulated) & Anti-Cheat
        function checkSecurity() {
            // Anti-Rapid Click (Cheat Detection)
            let currentTime = new Date().getTime();
            if (currentTime - lastClickTime < 500) { // 500ms gap mandatory
                showSecurityAlert("Slow down! Anti-Cheat triggered.");
                return false;
            }
            lastClickTime = currentTime;
            return true;
        }

        function showSecurityAlert(msg) {
            document.getElementById('security-overlay').style.display = 'flex';
            document.getElementById('security-msg').innerText = msg;
        }

        // 2. Navigation Logic
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            
            document.querySelectorAll('nav button').forEach(b => b.classList.remove('nav-active'));
            document.getElementById('nav-' + pageId).classList.add('nav-active');
        }

        // 3. Task System (Anti-Skip)
        const tasks = [
            { id: 1, type: 'Start.io', reward: 4 },
            { id: 2, type: 'AdMob', reward: 4 }
        ];

        function renderTasks() {
            const container = document.getElementById('task-container');
            tasks.forEach(t => {
                container.innerHTML += `
                    <div class="glass p-4 flex justify-between items-center">
                        <span>${t.type} Task #${t.id}</span>
                        <button onclick="startTask(this, ${t.reward})" class="bg-blue-600 px-4 py-2 rounded text-sm font-bold">Start</button>
                    </div>
                `;
            });
        }

        function startTask(btn, reward) {
            if(!checkSecurity()) return;

            let originalText = btn.innerText;
            btn.disabled = true;
            let timer = 10; // 10 second mandatory wait (Anti-Skip)
            
            let countdown = setInterval(() => {
                btn.innerText = `Wait ${timer}s`;
                timer--;
                if(timer < 0) {
                    clearInterval(countdown);
                    btn.innerText = "Claim!";
                    btn.onclick = () => {
                        balance += reward;
                        document.getElementById('balance').innerText = balance;
                        btn.parentElement.style.opacity = '0.5';
                        btn.innerText = "Completed";
                        btn.onclick = null;
                        alert("AI Verified: Token Added!");
                    }
                }
            }, 1000);
        }

        // 4. Wallet Logic
        function selectMethod(m) {
            document.getElementById('withdraw-box').classList.remove('hidden');
            document.getElementById('method-title').innerText = "Withdraw via " + m;
        }

        function processWithdraw() {
            let acc = document.getElementById('acc-num').value;
            if(acc.length < 5) return alert("Enter valid details!");
            if(balance < 500) return alert("Minimum 500 required!");
            
            balance -= 500;
            document.getElementById('balance').innerText = balance;
            alert("Request sent to admin: animetixb@gmail.com. Status: Pending");
        }

        renderTasks();
    </script>
</body>
</html>
