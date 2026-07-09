<EDUSINOPAYE>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>Turnamen Ganda Americano Pro</title>
    <style>
        /* ===== RESET & BASE ===== */
        * {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
        }
        body {
            background: #f4f7fc;
            padding: 15px;
            display: flex;
            justify-content: center;
            transition: background 0.3s, color 0.3s;
        }
        body.dark {
            background: #1a202c;
            color: #e2e8f0;
        }
        .container {
            max-width: 860px;
            width: 100%;
            background: white;
            padding: 20px;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: background 0.3s;
        }
        body.dark .container {
            background: #2d3748;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        /* ===== TYPOGRAPHY ===== */
        h1 {
            font-size: 24px;
            color: #1a2b4c;
            border-bottom: 3px solid #e2e8f0;
            padding-bottom: 10px;
            margin-top: 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        body.dark h1 {
            color: #f7fafc;
            border-bottom-color: #4a5568;
        }
        h2 {
            font-size: 18px;
            color: #2d3748;
            margin-top: 25px;
            border-left: 5px solid #3182ce;
            padding-left: 12px;
        }
        body.dark h2 {
            color: #e2e8f0;
        }

        /* ===== UTILITY ===== */
        .flex-row {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            align-items: center;
            margin: 10px 0;
        }
        .flex-between {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 8px;
        }
        .gap-8 {
            gap: 8px;
        }
        .mt-10 {
            margin-top: 10px;
        }
        .mb-10 {
            margin-bottom: 10px;
        }
        .w-full {
            width: 100%;
        }
        .text-center {
            text-align: center;
        }

        /* ===== INPUTS ===== */
        input[type="text"],
        input[type="number"] {
            padding: 12px 14px;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            font-size: 16px;
            flex: 1 1 180px;
            transition: 0.2s;
            background: white;
            color: #1a202c;
        }
        body.dark input[type="text"],
        body.dark input[type="number"] {
            background: #4a5568;
            border-color: #4a5568;
            color: #f7fafc;
        }
        input:focus {
            border-color: #3182ce;
            outline: none;
            box-shadow: 0 0 0 3px rgba(49, 130, 206, 0.2);
        }
        input:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }

        /* ===== BUTTONS ===== */
        .btn {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            transition: 0.2s;
            background: #edf2f7;
            color: #2d3748;
            touch-action: manipulation;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }
        .btn-primary {
            background: #3182ce;
            color: white;
        }
        .btn-primary:hover {
            background: #2b6cb0;
        }
        .btn-success {
            background: #38a169;
            color: white;
        }
        .btn-success:hover {
            background: #2f855a;
        }
        .btn-danger {
            background: #e53e3e;
            color: white;
        }
        .btn-danger:hover {
            background: #c53030;
        }
        .btn-warning {
            background: #dd6b20;
            color: white;
        }
        .btn-warning:hover {
            background: #c05621;
        }
        .btn-purple {
            background: #805ad5;
            color: white;
        }
        .btn-purple:hover {
            background: #6b46c1;
        }
        .btn-sm {
            padding: 8px 14px;
            font-size: 14px;
        }
        .btn-outline {
            background: transparent;
            border: 2px solid #3182ce;
            color: #3182ce;
        }
        .btn-outline:hover {
            background: #3182ce;
            color: white;
        }
        body.dark .btn-outline {
            border-color: #63b3ed;
            color: #63b3ed;
        }
        body.dark .btn-outline:hover {
            background: #63b3ed;
            color: #1a202c;
        }
        .btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        /* ===== PLAYER TAGS ===== */
        .player-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            padding: 10px 0;
        }
        .player-tag {
            background: #ebf8ff;
            color: #2b6cb0;
            padding: 6px 14px;
            border-radius: 20px;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
            border: 1px solid #bee3f8;
            font-size: 15px;
        }
        body.dark .player-tag {
            background: #2b6cb0;
            color: #ebf8ff;
            border-color: #3182ce;
        }
        .player-tag .remove {
            cursor: pointer;
            font-weight: bold;
            color: #e53e3e;
            background: none;
            border: none;
            font-size: 18px;
            padding: 0 4px;
            line-height: 1;
        }
        body.dark .player-tag .remove {
            color: #fc8181;
        }

        /* ===== CARDS ===== */
        .card {
            background: #f7fafc;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 15px;
        }
        body.dark .card {
            background: #3a4a5f;
        }
        .card-blue {
            background: #f0f5ff;
            border-left: 6px solid #3182ce;
        }
        body.dark .card-blue {
            background: #2d3b4f;
            border-left-color: #63b3ed;
        }

        .round-card {
            background: #f7fafc;
            border-radius: 12px;
            padding: 12px 15px;
            margin-bottom: 15px;
            border-left: 6px solid #3182ce;
        }
        body.dark .round-card {
            background: #3a4a5f;
            border-left-color: #63b3ed;
        }
        .round-title {
            font-weight: 700;
            font-size: 17px;
            color: #1a202c;
            margin-bottom: 10px;
        }
        body.dark .round-title {
            color: #f7fafc;
        }

        /* ===== MATCH ITEMS ===== */
        .match-item {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 8px 12px;
            background: white;
            padding: 10px 12px;
            border-radius: 8px;
            margin-bottom: 8px;
            border: 1px solid #e2e8f0;
            transition: 0.2s;
        }
        body.dark .match-item {
            background: #4a5568;
            border-color: #4a5568;
        }
        .match-item.completed {
            background: #f0fff4;
            border-color: #38a169;
        }
        body.dark .match-item.completed {
            background: #2f4a3a;
            border-color: #48bb78;
        }
        .match-item.match-bye {
            background: #fffff0;
            border-color: #f6e05e;
        }
        body.dark .match-item.match-bye {
            background: #4a4530;
            border-color: #d69e2e;
        }

        .team {
            display: flex;
            align-items: center;
            gap: 4px;
            font-weight: 500;
            font-size: 14px;
            flex-wrap: wrap;
        }
        .team span {
            background: #edf2f7;
            padding: 2px 10px;
            border-radius: 12px;
        }
        body.dark .team span {
            background: #5a6a7a;
            color: #f7fafc;
        }
        .team .bye {
            background: #fefcbf;
            color: #975a16;
        }
        body.dark .team .bye {
            background: #5a4f1a;
            color: #f6e05e;
        }
        .vs {
            font-weight: bold;
            color: #718096;
            margin: 0 4px;
        }
        body.dark .vs {
            color: #a0aec0;
        }

        .score-input {
            display: flex;
            align-items: center;
            gap: 6px;
            flex-wrap: wrap;
            margin-left: auto;
        }
        .score-input input {
            width: 55px;
            padding: 6px;
            text-align: center;
            font-size: 15px;
        }
        .match-status {
            font-size: 13px;
            font-weight: 600;
            color: #38a169;
        }
        body.dark .match-status {
            color: #68d391;
        }

        /* ===== RANKING TABLE ===== */
        table.ranking {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
            font-size: 14px;
        }
        table.ranking th {
            background: #2d3748;
            color: white;
            padding: 8px 10px;
            text-align: left;
        }
        body.dark table.ranking th {
            background: #1a202c;
        }
        table.ranking td {
            padding: 8px 10px;
            border-bottom: 1px solid #e2e8f0;
        }
        body.dark table.ranking td {
            border-bottom-color: #4a5568;
        }
        table.ranking tr:hover td {
            background: #f7fafc;
        }
        body.dark table.ranking tr:hover td {
            background: #3a4a5f;
        }
        .rank-num {
            font-weight: 700;
            color: #4a5568;
        }
        body.dark .rank-num {
            color: #a0aec0;
        }
        .medal {
            font-size: 18px;
            margin-right: 3px;
        }

        /* ===== INFO BADGES ===== */
        .info-badge {
            background: #ebf8ff;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 13px;
        }
        body.dark .info-badge {
            background: #2b6cb0;
            color: #ebf8ff;
        }
        .empty-state {
            color: #718096;
            font-style: italic;
            padding: 10px 0;
        }
        body.dark .empty-state {
            color: #a0aec0;
        }

        /* ===== FOOTER ===== */
        .footer-actions {
            margin-top: 25px;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            border-top: 2px solid #e2e8f0;
            padding-top: 20px;
        }
        body.dark .footer-actions {
            border-top-color: #4a5568;
        }

        /* ===== DARK MODE TOGGLE ===== */
        .dark-toggle {
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            padding: 4px 10px;
            border-radius: 30px;
            transition: 0.2s;
        }
        .dark-toggle:hover {
            background: #edf2f7;
        }
        body.dark .dark-toggle:hover {
            background: #4a5568;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 600px) {
            .container {
                padding: 12px;
            }
            .match-item {
                flex-direction: column;
                align-items: stretch;
            }
            .score-input {
                justify-content: center;
                margin-top: 5px;
                margin-left: 0;
            }
            .btn {
                padding: 10px 16px;
                font-size: 15px;
                width: 100%;
                justify-content: center;
            }
            .flex-row .btn {
                width: auto;
                flex: 1;
            }
            .flex-between {
                flex-direction: column;
                align-items: stretch;
            }
            .dark-toggle {
                font-size: 28px;
                padding: 8px 16px;
            }
        }
    </style>
</head>
<body>

    <div class="container" id="app">

        <!-- ===== HEADER ===== -->
        <h1>
            <span>🏸 Turnamen Gando (Americano)</span>
            <button class="dark-toggle" onclick="toggleDarkMode()" title="Mode Gelap">🌙</button>
        </h1>

        <!-- ===== INPUT PLAYER ===== -->
        <div class="card card-blue">
            <div class="flex-row">
                <input type="text" id="playerNameInput" placeholder="Nama pemain" onkeypress="if(event.keyCode==13) addPlayer()">
                <button class="btn btn-primary" onclick="addPlayer()">➕ Tambah</button>
                <button class="btn btn-warning" onclick="clearPlayers()">🗑️ Reset</button>
            </div>

            <div class="player-list" id="playerListContainer"></div>

            <div class="flex-between">
                <div style="font-size:14px; display:flex; gap:15px; flex-wrap:wrap;">
                    <span>Total: <strong id="playerCount">0</strong> pemain</span>
                    <span id="playerParity"></span>
                    <span class="info-badge">🔹 Ganjil pakai BYE</span>
                </div>
                <div style="display:flex; gap:8px; flex-wrap:wrap;">
                    <button class="btn btn-success btn-sm" onclick="generateSchedule()">📋 Buat Jadwal</button>
                    <button class="btn btn-warning btn-sm" onclick="regenerateSchedule()" title="Reset skor & generate ulang">🔄 Ulang</button>
                </div>
            </div>
        </div>

        <!-- ===== SCHEDULE ===== -->
        <h2>📅 Jadwal</h2>
        <div id="scheduleContainer"><div class="empty-state">Belum ada jadwal.</div></div>

        <!-- ===== RANKING ===== -->
        <div class="flex-between">
            <h2 style="margin-top:10px;">🏆 Klasemen</h2>
            <div style="display:flex; gap:8px; flex-wrap:wrap;">
                <button class="btn btn-purple btn-sm" onclick="shareRanking()">📤 Share</button>
                <button class="btn btn-outline btn-sm" onclick="exportHistory()">📁 History</button>
            </div>
        </div>
        <div id="rankingContainer"><div class="empty-state">Belum ada data.</div></div>

        <!-- ===== HISTORY ===== -->
        <div id="historyContainer" style="margin-top:10px;"></div>

        <!-- ===== FOOTER ===== -->
        <div class="footer-actions">
            <button class="btn btn-danger" onclick="resetAllData()" style="flex:1;">⚠️ Hapus Semua</button>
            <button class="btn btn-primary" onclick="saveHistory()" style="flex:1;">💾 Simpan Riwayat</button>
            <span style="font-size:12px; color:#718096; align-self:center;">Auto-save di HP</span>
        </div>
    </div>

    <script>
        // ================================================================
        //  STATE
        // ================================================================
        let state = { players: [], schedule: [] };
        let historyData = [];
        const STORAGE_KEY = 'badminton_americano_pro';
        const HISTORY_KEY = 'badminton_history_pro';

        // ================================================================
        //  PERSISTENCE
        // ================================================================
        function loadState() {
            try {
                const raw = localStorage.getItem(STORAGE_KEY);
                if (raw) { const p = JSON.parse(raw);
                    state.players = p.players || [];
                    state.schedule = p.schedule || []; }
            } catch (e) {}
            try {
                const h = localStorage.getItem(HISTORY_KEY);
                if (h) historyData = JSON.parse(h);
            } catch (e) {}
        }

        function saveState() {
            localStorage.setItem(STORAGE_KEY, JSON.stringify({ players: state.players, schedule: state.schedule }));
        }

        function saveHistoryToStorage() {
            localStorage.setItem(HISTORY_KEY, JSON.stringify(historyData));
        }

        // ================================================================
        //  RENDER
        // ================================================================
        function render() {
            renderPlayers();
            renderSchedule();
            renderRanking();
            renderHistory();
            saveState();
            updateDarkToggleIcon();
        }

        // ----- PLAYERS -----
        function renderPlayers() {
            const c = document.getElementById('playerListContainer');
            const count = document.getElementById('playerCount');
            const parity = document.getElementById('playerParity');

            if (state.players.length === 0) {
                c.innerHTML = '<span class="empty-state">Belum ada pemain.</span>';
            } else {
                c.innerHTML = state.players.map((name, idx) =>
                    `<div class="player-tag">
                        ${name}
                        <button class="remove" data-index="${idx}">✕</button>
                    </div>`
                ).join('');
                c.querySelectorAll('.remove').forEach(btn => {
                    btn.addEventListener('click', function() {
                        const idx = parseInt(this.dataset.index);
                        if (state.schedule.length > 0 && !confirm('Hapus pemain akan reset jadwal. Lanjutkan?'))
                            return;
                        state.schedule = [];
                        state.players.splice(idx, 1);
                        render();
                    });
                });
            }

            count.textContent = state.players.length;
            if (state.players.length % 2 !== 0) {
                parity.innerHTML = '<span style="color:#dd6b20; font-weight:600;">⚡ Ganjil (pakai BYE)</span>';
            } else if (state.players.length > 0) {
                parity.innerHTML = '<span style="color:#38a169; font-weight:600;">✅ Genap</span>';
            } else {
                parity.innerHTML = '';
            }
        }

        // ----- SCHEDULE -----
        function renderSchedule() {
            const container = document.getElementById('scheduleContainer');
            if (!state.schedule || state.schedule.length === 0) {
                container.innerHTML = '<div class="empty-state">Belum ada jadwal.</div>';
                return;
            }

            let html = '';
            state.schedule.forEach((round, rIdx) => {
                html +=
                    `<div class="round-card"><div class="round-title">🏸 Putaran ${round.round}</div>`;
                round.matches.forEach((match, mIdx) => {
                    const id = `r${rIdx}m${mIdx}`;
                    match.id = id;

                    // Cek BYE
                    const hasByeA = match.teamA.includes('BYE');
                    const hasByeB = match.teamB.includes('BYE');
                    const hasBye = hasByeA || hasByeB;

                    // Jika kedua tim BYE (istirahat total)
                    if (hasByeA && hasByeB) {
                        const restPlayers = match.teamA.filter(p => p !== 'BYE');
                        html +=
                            `<div class="match-item match-bye">🔄 Istirahat untuk ${restPlayers.join(', ')}</div>`;
                        return;
                    }

                    // Jika salah satu BYE → walkover
                    if (hasBye) {
                        const activeTeam = hasByeA ? match.teamB : match.teamA;
                        const activeStr = activeTeam.join(' & ');
                        html +=
                            `<div class="match-item match-bye">⏸️ Walkover : <strong>${activeStr}</strong> (istirahat)</div>`;
                        return;
                    }

                    const isPlayed = (match.scoreA !== null && match.scoreB !== null);
                    const scoreA = match.scoreA !== null ? match.scoreA : '';
                    const scoreB = match.scoreB !== null ? match.scoreB : '';
                    const completedClass = isPlayed ? 'completed' : '';

                    html += `
                        <div class="match-item ${completedClass}" data-match-id="${id}">
                            <div class="team">🏸 <span>${match.teamA.join(' & ')}</span></div>
                            <div class="vs">vs</div>
                            <div class="team"><span>${match.teamB.join(' & ')}</span> 🏸</div>
                            <div class="score-input">
                                <input type="number" min="0" max="30" placeholder="Skor" value="${scoreA}" class="score-a" data-id="${id}">
                                <span style="font-weight:bold;">-</span>
                                <input type="number" min="0" max="30" placeholder="Skor" value="${scoreB}" class="score-b" data-id="${id}">
                                <button class="btn btn-sm btn-primary save-score" data-id="${id}">Simpan</button>
                                ${isPlayed ? '<span class="match-status">✅ Selesai</span>' : ''}
                            </div>
                        </div>`;
                });
                html += `</div>`;
            });
            container.innerHTML = html;

            // Event listeners
            container.querySelectorAll('.save-score').forEach(btn => {
                btn.addEventListener('click', function() {
                    const id = this.dataset.id;
                    const parent = this.closest('.match-item');
                    const a = parent.querySelector('.score-a');
                    const b = parent.querySelector('.score-b');
                    const valA = parseInt(a.value);
                    const valB = parseInt(b.value);
                    if (isNaN(valA) || isNaN(valB) || valA < 0 || valB < 0) {
                        alert('Skor harus angka >= 0');
                        return;
                    }
                    if (valA > 30 || valB > 30) {
                        alert('Skor maksimal 30 (aturan bulutangkis)');
                        return;
                    }
                    if (valA === 0 && valB === 0) {
                        alert('Kedua skor tidak boleh 0!');
                        return;
                    }
                    updateScore(id, valA, valB);
                });
            });
            container.querySelectorAll('.score-a, .score-b').forEach(inp => {
                inp.addEventListener('keypress', function(e) {
                    if (e.key === 'Enter') {
                        const btn = this.closest('.match-item').querySelector('.save-score');
                        if (btn) btn.click();
                    }
                });
            });
        }

        // ----- RANKING -----
        function renderRanking() {
            const container = document.getElementById('rankingContainer');
            const stats = calculateRanking();
            if (stats.length === 0) {
                container.innerHTML = '<div class="empty-state">Belum ada data.</div>';
                return;
            }
            let html =
                `<table class="ranking"><thead><tr><th>#</th><th>Pemain</th><th>Main</th><th>Menang</th><th>Kalah</th><th>Selisih</th><th>Total Poin</th></tr></thead><tbody>`;
            stats.forEach((p, idx) => {
                const medal = idx === 0 ? '🥇' : idx === 1 ? '🥈' : idx === 2 ? '🥉' : '';
                html += `<tr><td><span class="rank-num">${idx+1}</span> ${medal}</td>
                         <td><strong>${p.name}</strong></td>
                         <td>${p.played}</td>
                         <td style="color:#38a169;">${p.won}</td>
                         <td style="color:#e53e3e;">${p.lost}</td>
                         <td>${p.diff}</td>
                         <td>${p.pointsFor}</td></tr>`;
            });
            html += `</tbody></table>`;
            container.innerHTML = html;
        }

        // ----- HISTORY -----
        function renderHistory() {
            const container = document.getElementById('historyContainer');
            if (!historyData || historyData.length === 0) {
                container.innerHTML = '';
                return;
            }
            let html =
                `<div style="background:#f7fafc; border-radius:12px; padding:12px; margin-top:10px; max-height:250px; overflow-y:auto;">
                    <div style="font-weight:600; margin-bottom:8px;">📜 Riwayat Turnamen</div>`;
            historyData.slice().reverse().forEach((entry, idx) => {
                const date = new Date(entry.date).toLocaleDateString('id-ID', { day: 'numeric', month: 'short',
                    year: 'numeric', hour: '2-digit', minute: '2-digit' });
                const top = entry.ranking && entry.ranking.length > 0 ? entry.ranking[0].name : '-';
                html += `<div style="font-size:13px; border-bottom:1px solid #e2e8f0; padding:6px 0; display:flex; justify-content:space-between; flex-wrap:wrap;">
                            <span>🏆 ${date} — Juara: <strong>${top}</strong> (${entry.players ? entry.players.length : 0} pemain)</span>
                            <button class="btn btn-sm btn-outline" onclick="loadHistory(${historyData.length - 1 - idx})">📂 Muat</button>
                        </div>`;
            });
            html += `</div>`;
            container.innerHTML = html;
        }

        // ================================================================
        //  LOGIC : PLAYER MANAGEMENT
        // ================================================================
        function addPlayer() {
            const input = document.getElementById('playerNameInput');
            const name = input.value.trim();
            if (!name) { alert('Masukkan nama.'); return; }
            if (state.players.includes(name)) { alert('Nama sudah ada.'); return; }
            if (state.schedule.length > 0 && !confirm('Tambah pemain akan reset jadwal. Lanjutkan?')) return;
            state.schedule = [];
            state.players.push(name);
            input.value = '';
            input.focus();
            render();
        }

        function clearPlayers() {
            if (state.players.length === 0) return;
            if (!confirm('Hapus semua pemain?')) return;
            state.players = [];
            state.schedule = [];
            render();
        }

        // ================================================================
        //  LOGIC : SCHEDULE (AMERICANO CORRECT)
        // ================================================================
        function generateSchedule() {
            const n = state.players.length;
            if (n < 3) { alert('Minimal 3 pemain.'); return; }

            let working = [...state.players];
            const isOdd = working.length % 2 !== 0;
            if (isOdd) working.push('BYE');
            const total = working.length;
            const rounds = total - 1;
            const newSchedule = [];
            let arr = [...working];

            for (let round = 0; round < rounds; round++) {
                // Buat pairing (circle method)
                const pairs = [];
                const mid = total / 2;
                for (let i = 0; i < mid; i++) {
                    pairs.push([arr[i], arr[total - 1 - i]]);
                }

                // Ubah pairing menjadi match (2 pairing per match)
                const matches = [];
                for (let j = 0; j < pairs.length; j += 2) {
                    if (j + 1 < pairs.length) {
                        matches.push({
                            teamA: pairs[j],
                            teamB: pairs[j + 1],
                            scoreA: null,
                            scoreB: null,
                            id: `r${round}m${Math.floor(j/2)}`
                        });
                    } else {
                        // Sisa pairing ganjil → istirahat (BYE)
                        matches.push({
                            teamA: pairs[j],
                            teamB: ['BYE', 'BYE'],
                            scoreA: null,
                            scoreB: null,
                            id: `r${round}m${Math.floor(j/2)}`
                        });
                    }
                }
                newSchedule.push({ round: round + 1, matches });

                // Rotasi untuk round berikutnya (circle method)
                let last = arr.pop();
                arr.splice(1, 0, last);
            }

            state.schedule = newSchedule;
            render();
        }

        function regenerateSchedule() {
            if (state.schedule.length > 0 && !confirm('Generate ulang jadwal? Semua skor akan hilang.')) return;
            // Reset skor
            state.schedule.forEach(round => {
                round.matches.forEach(match => {
                    match.scoreA = null;
                    match.scoreB = null;
                });
            });
            // Generate ulang dari awal (pakai pemain yang sama)
            state.schedule = [];
            generateSchedule();
        }

        // ================================================================
        //  LOGIC : SCORE
        // ================================================================
        function updateScore(matchId, scoreA, scoreB) {
            let found = false;
            for (let r of state.schedule) {
                for (let m of r.matches) {
                    if (m.id === matchId) {
                        // Cegah BYE
                        if (m.teamA.includes('BYE') || m.teamB.includes('BYE')) {
                            alert('Ini walkover, tidak perlu skor.');
                            return;
                        }
                        m.scoreA = scoreA;
                        m.scoreB = scoreB;
                        found = true;
                        break;
                    }
                }
                if (found) break;
            }
            if (!found) { alert('Pertandingan tidak ditemukan.'); return; }
            render();
        }

        // ================================================================
        //  LOGIC : RANKING
        // ================================================================
        function calculateRanking() {
            const statsMap = {};
            state.players.forEach(p => {
                statsMap[p] = { name: p, played: 0, won: 0, lost: 0, pointsFor: 0, pointsAgainst: 0, diff: 0 };
            });

            state.schedule.forEach(round => {
                round.matches.forEach(match => {
                    if (match.teamA.includes('BYE') || match.teamB.includes('BYE')) return;
                    if (match.scoreA === null || match.scoreB === null) return;

                    const a = match.teamA;
                    const b = match.teamB;
                    const sA = match.scoreA;
                    const sB = match.scoreB;

                    const updatePlayer = (name, pf, pa, isWin) => {
                        if (!statsMap[name]) return;
                        statsMap[name].played += 1;
                        statsMap[name].pointsFor += pf;
                        statsMap[name].pointsAgainst += pa;
                        if (isWin) statsMap[name].won += 1;
                        else statsMap[name].lost += 1;
                    };

                    if (sA === sB) {
                        // Seri: kedua tim dapat poin
                        a.forEach(p => { statsMap[p].played += 1;
                            statsMap[p].pointsFor += sA;
                            statsMap[p].pointsAgainst += sB; });
                        b.forEach(p => { statsMap[p].played += 1;
                            statsMap[p].pointsFor += sB;
                            statsMap[p].pointsAgainst += sA; });
                    } else {
                        const aWon = sA > sB;
                        const bWon = sB > sA;
                        a.forEach(p => updatePlayer(p, sA, sB, aWon));
                        b.forEach(p => updatePlayer(p, sB, sA, bWon));
                    }
                });
            });

            const result = Object.values(statsMap);
            result.forEach(p => { p.diff = p.pointsFor - p.pointsAgainst; });
            result.sort((a, b) => b.won - a.won || b.diff - a.diff || b.pointsFor - a.pointsFor);
            return result;
        }

        // ================================================================
        //  LOGIC : HISTORY
        // ================================================================
        function saveHistory() {
            if (state.players.length === 0) { alert('Tidak ada pemain untuk disimpan.'); return; }
            const ranking = calculateRanking();
            const entry = {
                date: new Date().toISOString(),
                players: [...state.players],
                schedule: JSON.parse(JSON.stringify(state.schedule)),
                ranking: ranking
            };
            historyData.push(entry);
            saveHistoryToStorage();
            render();
            alert('✅ Riwayat tersimpan!');
        }

        function loadHistory(index) {
            if (index < 0 || index >= historyData.length) return;
            const entry = historyData[index];
            if (!confirm(`Muat riwayat dari ${new Date(entry.date).toLocaleDateString('id-ID')}? Data saat ini akan diganti.`))
                return;
            state.players = [...entry.players];
            state.schedule = JSON.parse(JSON.stringify(entry.schedule));
            render();
        }

        function exportHistory() {
            if (historyData.length === 0) { alert('Belum ada riwayat.'); return; }
            const text = historyData.map((entry, i) => {
                const date = new Date(entry.date).toLocaleDateString('id-ID');
                const top = entry.ranking && entry.ranking.length > 0 ? entry.ranking[0].name : '-';
                return `${i+1}. ${date} — Juara: ${top} (${entry.players.length} pemain)`;
            }).join('\n');
            if (navigator.share) {
                navigator.share({ title: 'Riwayat Turnamen', text }).catch(() => {});
            } else {
                navigator.clipboard.writeText('Riwayat Turnamen:\n' + text).then(() => alert('Riwayat disalin!'));
            }
        }

        // ================================================================
        //  LOGIC : SHARE RANKING
        // ================================================================
        function shareRanking() {
            const stats = calculateRanking();
            if (stats.length === 0) { alert('Belum ada data klasemen.'); return; }
            let text = '🏸 Klasemen Turnamen Americano\n\n';
            stats.forEach((p, i) => {
                const medal = i === 0 ? '🥇' : i === 1 ? '🥈' : i === 2 ? '🥉' : '';
                text += `${medal} ${i+1}. ${p.name} — ${p.won}W/${p.lost}L  (selisih ${p.diff})  poin ${p.pointsFor}\n`;
            });
            if (navigator.share) {
                navigator.share({ title: 'Klasemen Badminton', text }).catch(() => {});
            } else {
                navigator.clipboard.writeText(text).then(() => alert('📋 Klasemen disalin ke clipboard!'));
            }
        }

        // ================================================================
        //  LOGIC : RESET
        // ================================================================
        function resetAllData() {
            if (!confirm('Yakin hapus semua data (termasuk riwayat)?')) return;
            state.players = [];
            state.schedule = [];
            historyData = [];
            saveHistoryToStorage();
            render();
        }

        // ================================================================
        //  DARK MODE
        // ================================================================
        function toggleDarkMode() {
            document.body.classList.toggle('dark');
            updateDarkToggleIcon();
            localStorage.setItem('darkMode', document.body.classList.contains('dark') ? 'true' : 'false');
        }

        function updateDarkToggleIcon() {
            const btn = document.querySelector('.dark-toggle');
            if (document.body.classList.contains('dark')) {
                btn.textContent = '☀️';
            } else {
                btn.textContent = '🌙';
            }
        }

        function loadDarkMode() {
            if (localStorage.getItem('darkMode') === 'true') {
                document.body.classList.add('dark');
                updateDarkToggleIcon();
            }
        }

        // ================================================================
        //  INIT
        // ================================================================
        loadState();
        loadDarkMode();
        render();

        console.log('🏸 Turnamen Americano Pro siap!');
        console.log(`📋 ${state.players.length} pemain, ${state.schedule.length} putaran.`);
    </script>

</body>
</html># americano-badminton
