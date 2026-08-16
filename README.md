<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport"
      content="width=device-width, initial-scale=1.0,
               maximum-scale=1.0, user-scalable=no">

<title>DLS 26 League Manager</title>

<style>

/* =========================================================
   MOBILE-FIRST DLS 26
========================================================= */

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    -webkit-tap-highlight-color: transparent;
}

html {
    background: #070b16;
}

body {
    background:
        linear-gradient(180deg, #0b1224 0%, #070b16 100%);
    color: #fff;
    min-height: 100vh;
    width: 100%;
    overflow-x: hidden;
}

/* =========================================================
   APP HEADER
========================================================= */

header {
    background:
        linear-gradient(145deg, #101d40, #0c142b);
    padding: 20px 16px 18px;
    text-align: center;
    border-bottom: 1px solid #24355f;
}

header h1 {
    font-size: 22px;
    font-weight: 800;
    margin-bottom: 6px;
}

header p {
    color: #91a1c7;
    font-size: 11px;
    line-height: 1.5;
}

header p:last-child {
    color: #60a5fa;
    font-weight: bold;
    letter-spacing: 2px;
    margin-top: 5px;
}

/* =========================================================
   APP CONTAINER
========================================================= */

.container {
    width: 100%;
    max-width: 520px;
    margin: auto;
    padding: 10px;
}

/* =========================================================
   ADMIN BUTTON
========================================================= */

.admin-bar {
    margin-bottom: 10px;
}

.admin-btn {
    width: 100%;
    height: 46px;
    background: #151f35;
    color: #fff;
    border: 1px solid #304266;
    border-radius: 12px;
    font-size: 13px;
    font-weight: bold;
}

.admin-btn:active {
    transform: scale(.98);
}

/* =========================================================
   LEAGUE SELECTOR
========================================================= */

.tabs {
    display: flex;
    gap: 7px;
    overflow-x: auto;
    padding-bottom: 4px;
    margin-bottom: 12px;

    scrollbar-width: none;
    -webkit-overflow-scrolling: touch;
}

.tabs::-webkit-scrollbar {
    display: none;
}

.tab {
    flex: 0 0 auto;
    background: #111a30;
    color: #8e9bbb;
    border: 1px solid #263657;
    border-radius: 10px;
    padding: 10px 14px;
    min-height: 42px;
    font-size: 12px;
    font-weight: bold;
}

.tab small {
    font-size: 9px;
    opacity: .7;
}

.tab.active {
    background: #2563eb;
    border-color: #3b82f6;
    color: #fff;
}

/* =========================================================
   DASHBOARD STAT CARDS
========================================================= */

.stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 8px;
    margin-bottom: 10px;
}

.stat {
    background:
        linear-gradient(145deg, #141e35, #10182b);
    border: 1px solid #253657;
    border-radius: 13px;
    min-height: 82px;
    padding: 12px 8px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.stat strong {
    display: block;
    color: #60a5fa;
    font-size: 21px;
    font-weight: 800;
    margin-bottom: 5px;

    max-width: 100%;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

.stat span {
    color: #7f8dab;
    font-size: 10px;
    text-transform: uppercase;
    letter-spacing: .5px;
}

/* =========================================================
   MOBILE PANELS
========================================================= */

.panel {
    background:
        linear-gradient(145deg, #111a2d, #0d1526);
    border: 1px solid #223354;
    border-radius: 14px;
    padding: 13px;
    margin-bottom: 10px;
}

.panel h2 {
    font-size: 16px;
    margin-bottom: 12px;
}

/* =========================================================
   STANDINGS
========================================================= */

.standings-mobile {
    width: 100%;
}

.table-wrapper {
    width: 100%;
    overflow-x: auto;
    border-radius: 9px;
    -webkit-overflow-scrolling: touch;
}

table {
    width: 100%;
    min-width: 620px;
    border-collapse: collapse;
}

th {
    background: #1a2744;
    color: #91a3c8;
    font-size: 9px;
    padding: 9px 5px;
    text-align: center;
    position: sticky;
    top: 0;
}

td {
    padding: 10px 5px;
    border-bottom: 1px solid #202f4d;
    text-align: center;
    font-size: 11px;
}

td:nth-child(2) {
    text-align: left;
    font-weight: bold;
    min-width: 120px;
}

td:nth-child(2) small {
    display: block;
    color: #687897 !important;
    font-size: 8px !important;
    font-weight: normal;
    margin-top: 2px;
}

tr:hover {
    background: #151f35;
}

.position {
    color: #60a5fa;
    font-weight: bold;
}

.champion {
    color: #facc15;
}

.champion td:nth-child(2) {
    color: #facc15;
}

/* =========================================================
   MOBILE RESULT CARDS
========================================================= */

.match {
    background: #0b1324;
    border: 1px solid #1e3154;
    border-left: 3px solid #2563eb;
    border-radius: 11px;
    padding: 12px;
    margin-bottom: 8px;
}

.match-top {
    display: flex;
    justify-content: space-between;
    color: #7182a4;
    font-size: 9px;
    margin-bottom: 10px;
}

.score {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
    text-align: center;
    font-size: 13px;
    font-weight: bold;
    line-height: 1.4;
}

.score .score-number {
    color: #60a5fa;
    font-size: 19px;
    font-weight: 900;
}

.score .team {
    width: 38%;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

/* =========================================================
   FORMS
========================================================= */

.form-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 8px;
}

input,
select {
    width: 100%;
    height: 46px;
    padding: 0 12px;

    background: #080e1c;
    color: #fff;

    border: 1px solid #2b3d60;
    border-radius: 10px;

    outline: none;
    font-size: 13px;
}

input::placeholder {
    color: #667492;
}

input:focus,
select:focus {
    border-color: #3b82f6;
    box-shadow: 0 0 0 2px rgba(59,130,246,.12);
}

/* =========================================================
   BUTTONS
========================================================= */

button {
    border: none;
    border-radius: 10px;
    min-height: 44px;
    padding: 10px 14px;
    cursor: pointer;
    font-size: 12px;
    font-weight: bold;
}

button:active {
    transform: scale(.98);
}

.primary {
    background: #2563eb;
    color: white;
}

.success {
    background: #16a34a;
    color: white;
}

.danger {
    background: #dc2626;
    color: white;
}

.secondary {
    background: #374151;
    color: white;
}

.button-row {
    display: flex;
    gap: 8px;
    margin-top: 10px;
}

.button-row button {
    flex: 1;
}

/* =========================================================
   ADMIN AREA
========================================================= */

#adminArea {
    display: none;
}

.admin-heading {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-bottom: 14px;
}

.admin-heading h2 {
    margin-bottom: 4px;
}

.admin-status {
    color: #4ade80;
    font-size: 10px;
}

#adminArea > .panel {
    background: #0d1526;
}

#adminArea .panel .panel {
    background: #101a2e;
    border-color: #243656;
    margin-bottom: 9px;
}

/* =========================================================
   TEAM CARDS
========================================================= */

.league-card {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 10px;

    background: #0a1221;
    border: 1px solid #243656;
    border-radius: 10px;

    padding: 11px;
    margin-bottom: 7px;
}

.league-card h3 {
    color: #60a5fa;
    font-size: 13px;
    margin-bottom: 3px;
}

.league-card small {
    color: #7887a5;
    font-size: 10px;
}

.league-card button {
    min-width: 70px;
    min-height: 38px;
    padding: 8px;
    font-size: 10px;
}

/* =========================================================
   EMPTY STATES
========================================================= */

.empty {
    text-align: center;
    color: #687896;
    padding: 25px 10px;
    font-size: 12px;
}

/* =========================================================
   PASSWORD MODAL
========================================================= */

.modal {
    position: fixed;
    inset: 0;

    background: rgba(2,5,12,.88);

    display: none;
    align-items: center;
    justify-content: center;

    padding: 15px;
    z-index: 9999;
}

.modal-box {
    width: 100%;
    max-width: 380px;

    background:
        linear-gradient(145deg, #121d34, #0c1426);

    border: 1px solid #304568;
    border-radius: 16px;

    padding: 20px;

    box-shadow: 0 20px 60px rgba(0,0,0,.7);
}

.modal-box h2 {
    font-size: 19px;
    margin-bottom: 7px;
}

.modal-box p {
    color: #8492af;
    font-size: 11px;
    line-height: 1.5;
    margin-bottom: 15px;
}

.password-error {
    color: #f87171;
    font-size: 11px;
    margin-top: 8px;
    display: none;
}

.close-modal {
    background: #374151;
    color: white;
}

/* =========================================================
   SMALL PHONES
========================================================= */

@media (max-width: 360px) {

    header h1 {
        font-size: 19px;
    }

    .container {
        padding: 8px;
    }

    .panel {
        padding: 11px;
    }

    .stat {
        min-height: 75px;
    }

    .stat strong {
        font-size: 18px;
    }

    .score {
        font-size: 11px;
    }

    .score .score-number {
        font-size: 17px;
    }
}

/* =========================================================
   TABLET / COMPUTER
========================================================= */

@media (min-width: 700px) {

    .container {
        max-width: 1100px;
        padding: 20px;
    }

    header h1 {
        font-size: 28px;
    }

    .admin-btn {
        width: auto;
    }

    .admin-bar {
        display: flex;
        justify-content: flex-end;
    }

    .stats {
        grid-template-columns:
            repeat(4, 1fr);
    }

    .form-grid {
        grid-template-columns:
            repeat(2, 1fr);
    }

    .admin-heading {
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }
}

</style>
</head>

<body>

<header>

    <h1>⚽ DLS 26</h1>

    <p>League Manager</p>

    <p>TRIXARQ</p>

</header>


<div class="container">

    <!-- ADMIN -->

    <div class="admin-bar">

        <button
            class="admin-btn"
            onclick="openAdminLogin()">

            🔐 Administrator

        </button>

    </div>


    <!-- LEAGUES -->

    <div
        class="tabs"
        id="leagueTabs">
    </div>


    <!-- PUBLIC DASHBOARD -->

    <section id="dashboardSection">


        <!-- STAT CARDS -->

        <div class="stats">

            <div class="stat">

                <strong id="teamCount">
                    0
                </strong>

                <span>
                    Teams
                </span>

            </div>


            <div class="stat">

                <strong id="matchCount">
                    0
                </strong>

                <span>
                    Matches
                </span>

            </div>


            <div class="stat">

                <strong id="leaderName">
                    -
                </strong>

                <span>
                    Leader
                </span>

            </div>


            <div class="stat">

                <strong id="leaderPoints">
                    0
                </strong>

                <span>
                    Points
                </span>

            </div>

        </div>


        <!-- STANDINGS -->

        <div class="panel">

            <h2>
                🏆 League Standings
            </h2>

            <div class="table-wrapper">

                <table>

                    <thead>

                        <tr>

                            <th>#</th>

                            <th>TEAM</th>

                            <th>P</th>

                            <th>W</th>

                            <th>D</th>

                            <th>L</th>

                            <th>GF</th>

                            <th>GA</th>

                            <th>GD</th>

                            <th>PTS</th>

                        </tr>

                    </thead>

                    <tbody
                        id="standingsBody">
                    </tbody>

                </table>

            </div>

        </div>


        <!-- RESULTS -->

        <div class="panel">

            <h2>
                ⚽ Recent Results
            </h2>

            <div id="resultsList">
            </div>

        </div>

    </section>


    <!-- =====================================================
         ADMIN
    ====================================================== -->

    <section id="adminArea">

        <div class="panel">


            <div class="admin-heading">

                <div>

                    <h2>
                        🔐 Admin Panel
                    </h2>

                    <span class="admin-status">
                        ● Administrator access enabled
                    </span>

                </div>


                <button
                    class="danger"
                    onclick="logoutAdmin()">

                    🔒 Lock Admin

                </button>

            </div>


            <!-- CREATE LEAGUE -->

            <div class="panel">

                <h2>
                    ➕ Create League
                </h2>

                <div class="form-grid">

                    <input
                        id="leagueName"
                        type="text"
                        placeholder="League name">

                    <input
                        id="leagueSeason"
                        type="text"
                        placeholder="Season e.g. Season 1">

                </div>

                <div class="button-row">

                    <button
                        class="primary"
                        onclick="createLeague()">

                        Create League

                    </button>

                </div>

            </div>


            <!-- ADD TEAM -->

            <div class="panel">

                <h2>
                    👥 Add Team
                </h2>

                <div class="form-grid">

                    <input
                        id="teamName"
                        type="text"
                        placeholder="Team name">

                    <input
                        id="teamManager"
                        type="text"
                        placeholder="Manager / Player">

                </div>

                <div class="button-row">

                    <button
                        class="success"
                        onclick="addTeam()">

                        Add Team

                    </button>

                </div>

            </div>


            <!-- MATCH RESULT -->

            <div class="panel">

                <h2>
                    ⚽ Enter Result
                </h2>

                <div class="form-grid">

                    <select id="homeTeam">

                        <option value="">
                            Home team
                        </option>

                    </select>


                    <select id="awayTeam">

                        <option value="">
                            Away team
                        </option>

                    </select>


                    <input
                        id="homeScore"
                        type="number"
                        min="0"
                        inputmode="numeric"
                        placeholder="Home score">


                    <input
                        id="awayScore"
                        type="number"
                        min="0"
                        inputmode="numeric"
                        placeholder="Away score">


                    <input
                        id="matchDate"
                        type="date">

                </div>


                <div class="button-row">

                    <button
                        class="primary"
                        onclick="addResult()">

                        ⚽ Save Result

                    </button>

                </div>

            </div>


            <!-- TEAMS -->

            <div class="panel">

                <h2>
                    👥 Current Teams
                </h2>

                <div id="teamList">
                </div>

            </div>


            <!-- DATA -->

            <div class="panel">

                <h2>
                    ⚙️ Data Management
                </h2>

                <p style="
                    color:#7887a5;
                    font-size:10px;
                    line-height:1.5;
                ">

                    These actions affect all
                    saved league data.

                </p>


                <div class="button-row">

                    <button
                        class="danger"
                        onclick="deleteCurrentLeague()">

                        Delete League

                    </button>


                    <button
                        class="secondary"
                        onclick="clearEverything()">

                        Clear Everything

                    </button>

                </div>

            </div>

        </div>

    </section>

</div>


<!-- =========================================================
     PASSWORD MODAL
========================================================= -->

<div
    class="modal"
    id="adminModal">

    <div class="modal-box">

        <h2>
            🔐 Admin Login
        </h2>

        <p>
            Enter the administrator password
            to manage the league.
        </p>


        <input
            id="adminPassword"
            type="password"
            placeholder="Administrator password"
            onkeydown="
                if(event.key === 'Enter')
                loginAdmin()
            ">


        <div
            class="password-error"
            id="passwordError">

            Incorrect password.

        </div>


        <div class="button-row">

            <button
                class="primary"
                onclick="loginAdmin()">

                Login

            </button>


            <button
                class="close-modal"
                onclick="closeAdminLogin()">

                Cancel

            </button>

        </div>

    </div>

</div>


<script>

/* =========================================================
   ADMIN PASSWORD
========================================================= */

const ADMIN_PASSWORD = "35786491";

let adminLoggedIn = false;


/* =========================================================
   DATABASE
========================================================= */

let database =
    JSON.parse(
        localStorage.getItem("dls26_database")
    ) || {
        leagues: []
    };

let currentLeagueId = null;


/* =========================================================
   ADMIN LOGIN
========================================================= */

function openAdminLogin() {

    document.getElementById(
        "adminModal"
    ).style.display = "flex";

    document.getElementById(
        "adminPassword"
    ).value = "";

    document.getElementById(
        "passwordError"
    ).style.display = "none";

    setTimeout(() => {

        document.getElementById(
            "adminPassword"
        ).focus();

    }, 100);
}


function closeAdminLogin() {

    document.getElementById(
        "adminModal"
    ).style.display = "none";
}


function loginAdmin() {

    const password =
        document.getElementById(
            "adminPassword"
        ).value;

    if (password === ADMIN_PASSWORD) {

        adminLoggedIn = true;

        closeAdminLogin();

        document.getElementById(
            "adminArea"
        ).style.display = "block";

        render();

        window.scrollTo({
            top: document.body.scrollHeight,
            behavior: "smooth"
        });

    } else {

        document.getElementById(
            "passwordError"
        ).style.display = "block";

        document.getElementById(
            "adminPassword"
        ).value = "";

        document.getElementById(
            "adminPassword"
        ).focus();
    }
}


/* =========================================================
   LOGOUT
========================================================= */

function logoutAdmin() {

    adminLoggedIn = false;

    document.getElementById(
        "adminArea"
    ).style.display = "none";

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


/* =========================================================
   SAVE DATABASE
========================================================= */

function saveDatabase() {

    localStorage.setItem(
        "dls26_database",
        JSON.stringify(database)
    );
}


/* =========================================================
   CURRENT LEAGUE
========================================================= */

function getCurrentLeague() {

    if (!database.leagues.length) {
        return null;
    }

    if (!currentLeagueId) {

        currentLeagueId =
            database.leagues[0].id;
    }

    return database.leagues.find(
        league =>
            league.id === currentLeagueId
    );
}


/* =========================================================
   CREATE LEAGUE
========================================================= */

function createLeague() {

    if (!adminLoggedIn) {
        alert(
            "Administrator access required."
        );
        return;
    }

    const name =
        document.getElementById(
            "leagueName"
        ).value.trim();

    const season =
        document.getElementById(
            "leagueSeason"
        ).value.trim();

    if (!name) {

        alert(
            "Please enter a league name."
        );

        return;
    }

    const league = {

        id: Date.now(),

        name: name,

        season:
            season || "Season 1",

        teams: [],

        matches: []

    };

    database.leagues.push(league);

    currentLeagueId = league.id;

    saveDatabase();

    document.getElementById(
        "leagueName"
    ).value = "";

    document.getElementById(
        "leagueSeason"
    ).value = "";

    render();
}


/* =========================================================
   ADD TEAM
========================================================= */

function addTeam() {

    if (!adminLoggedIn) {

        alert(
            "Administrator access required."
        );

        return;
    }

    const league =
        getCurrentLeague();

    if (!league) {

        alert(
            "Create a league first."
        );

        return;
    }

    const name =
        document.getElementById(
            "teamName"
        ).value.trim();

    const manager =
        document.getElementById(
            "teamManager"
        ).value.trim();

    if (!name) {

        alert(
            "Enter a team name."
        );

        return;
    }

    if (
        league.teams.some(
            team =>
                team.name.toLowerCase() ===
                name.toLowerCase()
        )
    ) {

        alert(
            "This team already exists."
        );

        return;
    }

    league.teams.push({

        id: Date.now(),

        name: name,

        manager:
            manager || "Unknown"

    });

    saveDatabase();

    document.getElementById(
        "teamName"
    ).value = "";

    document.getElementById(
        "teamManager"
    ).value = "";

    render();
}


/* =========================================================
   ADD RESULT
========================================================= */

function addResult() {

    if (!adminLoggedIn) {

        alert(
            "Administrator access required."
        );

        return;
    }

    const league =
        getCurrentLeague();

    if (!league) {

        alert(
            "Create a league first."
        );

        return;
    }

    const homeId =
        Number(
            document.getElementById(
                "homeTeam"
            ).value
        );

    const awayId =
        Number(
            document.getElementById(
                "awayTeam"
            ).value
        );

    const homeScore =
        Number(
            document.getElementById(
                "homeScore"
            ).value
        );

    const awayScore =
        Number(
            document.getElementById(
                "awayScore"
            ).value
        );

    const date =
        document.getElementById(
            "matchDate"
        ).value;

    if (!homeId || !awayId) {

        alert(
            "Select both teams."
        );

        return;
    }

    if (homeId === awayId) {

        alert(
            "A team cannot play against itself."
        );

        return;
    }

    if (
        document.getElementById(
            "homeScore"
        ).value === "" ||

        document.getElementById(
            "awayScore"
        ).value === ""
    ) {

        alert(
            "Enter both scores."
        );

        return;
    }

    league.matches.push({

        id: Date.now(),

        homeId,

        awayId,

        homeScore,

        awayScore,

        date:
            date ||
            new Date()
                .toISOString()
                .split("T")[0]

    });

    saveDatabase();

    document.getElementById(
        "homeScore"
    ).value = "";

    document.getElementById(
        "awayScore"
    ).value = "";

    render();
}


/* =========================================================
   STANDINGS
========================================================= */

function calculateStandings(league) {

    const table = {};

    league.teams.forEach(team => {

        table[team.id] = {

            id: team.id,

            name: team.name,

            manager: team.manager,

            played: 0,

            wins: 0,

            draws: 0,

            losses: 0,

            gf: 0,

            ga: 0,

            gd: 0,

            points: 0

        };

    });


    league.matches.forEach(match => {

        const home =
            table[match.homeId];

        const away =
            table[match.awayId];

        if (!home || !away)
            return;

        home.played++;

        away.played++;

        home.gf += match.homeScore;

        home.ga += match.awayScore;

        away.gf += match.awayScore;

        away.ga += match.homeScore;


        if (
            match.homeScore >
            match.awayScore
        ) {

            home.wins++;

            away.losses++;

            home.points += 3;

        }

        else if (
            match.homeScore <
            match.awayScore
        ) {

            away.wins++;

            home.losses++;

            away.points += 3;

        }

        else {

            home.draws++;

            away.draws++;

            home.points++;

            away.points++;

        }

    });


    Object.values(table)
        .forEach(team => {

            team.gd =
                team.gf - team.ga;

        });


    return Object.values(table).sort(
        (a, b) => {

            if (b.points !== a.points)
                return b.points - a.points;

            if (b.gd !== a.gd)
                return b.gd - a.gd;

            if (b.gf !== a.gf)
                return b.gf - a.gf;

            return a.name.localeCompare(
                b.name
            );
        }
    );
}


/* =========================================================
   LEAGUE TABS
========================================================= */

function renderTabs() {

    const container =
        document.getElementById(
            "leagueTabs"
        );

    container.innerHTML = "";

    database.leagues.forEach(
        league => {

            const button =
                document.createElement(
                    "button"
                );

            button.className =
                "tab " +
                (
                    league.id ===
                    currentLeagueId
                        ? "active"
                        : ""
                );

            button.innerHTML =
                `${escapeHTML(
                    league.name
                )}
                <small>
                    (${escapeHTML(
                        league.season
                    )})
                </small>`;

            button.onclick = () => {

                currentLeagueId =
                    league.id;

                render();
            };

            container.appendChild(
                button
            );

        }
    );
}


/* =========================================================
   STANDINGS DISPLAY
========================================================= */

function renderStandings(league) {

    const body =
        document.getElementById(
            "standingsBody"
        );

    body.innerHTML = "";

    if (
        !league ||
        !league.teams.length
    ) {

        body.innerHTML = `
            <tr>
                <td
                    colspan="10"
                    class="empty">

                    No teams yet.

                </td>
            </tr>
        `;

        return;
    }

    const standings =
        calculateStandings(league);

    standings.forEach(
        (team, index) => {

            const row =
                document.createElement(
                    "tr"
                );

            if (index === 0) {

                row.classList.add(
                    "champion"
                );
            }

            row.innerHTML = `

                <td class="position">
                    ${index + 1}
                </td>

                <td>
                    ${escapeHTML(
                        team.name
                    )}

                    <small>
                        ${escapeHTML(
                            team.manager
                        )}
                    </small>
                </td>

                <td>
                    ${team.played}
                </td>

                <td>
                    ${team.wins}
                </td>

                <td>
                    ${team.draws}
                </td>

                <td>
                    ${team.losses}
                </td>

                <td>
                    ${team.gf}
                </td>

                <td>
                    ${team.ga}
                </td>

                <td>
                    ${
                        team.gd > 0
                            ? "+"
                            : ""
                    }${team.gd}
                </td>

                <td>
                    <strong>
                        ${team.points}
                    </strong>
                </td>

            `;

            body.appendChild(row);

        }
    );
}


/* =========================================================
   RESULTS
========================================================= */

function renderResults(league) {

    const container =
        document.getElementById(
            "resultsList"
        );

    container.innerHTML = "";

    if (
        !league ||
        !league.matches.length
    ) {

        container.innerHTML = `
            <div class="empty">
                No match results yet.
            </div>
        `;

        return;
    }

    [...league.matches]
        .reverse()
        .forEach(match => {

            const home =
                league.teams.find(
                    team =>
                        team.id ===
                        match.homeId
                );

            const away =
                league.teams.find(
                    team =>
                        team.id ===
                        match.awayId
                );

            if (!home || !away)
                return;

            const div =
                document.createElement(
                    "div"
                );

            div.className = "match";

            div.innerHTML = `

                <div class="match-top">

                    <span>
                        ${escapeHTML(
                            match.date
                        )}
                    </span>

                    <span>
                        DLS 26
                    </span>

                </div>

                <div class="score">

                    <span class="team">
                        ${escapeHTML(
                            home.name
                        )}
                    </span>

                    <span>
                        <span class="score-number">
                            ${match.homeScore}
                        </span>

                        -

                        <span class="score-number">
                            ${match.awayScore}
                        </span>
                    </span>

                    <span class="team">
                        ${escapeHTML(
                            away.name
                        )}
                    </span>

                </div>

            `;

            container.appendChild(div);

        });
}


/* =========================================================
   TEAM LIST
========================================================= */

function renderTeams(league) {

    const container =
        document.getElementById(
            "teamList"
        );

    container.innerHTML = "";

    if (
        !league ||
        !league.teams.length
    ) {

        container.innerHTML = `
            <div class="empty">
                No teams added.
            </div>
        `;

        return;
    }

    league.teams.forEach(
        team => {

            const card =
                document.createElement(
                    "div"
                );

            card.className =
                "league-card";

            card.innerHTML = `

                <div>

                    <h3>
                        ${escapeHTML(
                            team.name
                        )}
                    </h3>

                    <small>
                        Manager:
                        ${escapeHTML(
                            team.manager
                        )}
                    </small>

                </div>

                <button
                    class="danger"
                    onclick="removeTeam(
                        ${team.id}
                    )">

                    Remove

                </button>

            `;

            container.appendChild(card);

        }
    );
}


/* =========================================================
   TEAM SELECTORS
========================================================= */

function renderTeamSelectors(league) {

    const home =
        document.getElementById(
            "homeTeam"
        );

    const away =
        document.getElementById(
            "awayTeam"
        );

    home.innerHTML = `
        <option value="">
            Home team
        </option>
    `;

    away.innerHTML = `
        <option value="">
            Away team
        </option>
    `;

    if (!league)
        return;

    league.teams.forEach(
        team => {

            home.innerHTML += `
                <option
                    value="${team.id}">
                    ${escapeHTML(
                        team.name
                    )}
                </option>
            `;

            away.innerHTML += `
                <option
                    value="${team.id}">
                    ${escapeHTML(
                        team.name
                    )}
                </option>
            `;

        }
    );
}


/* =========================================================
   STATS
========================================================= */

function renderStats(league) {

    document.getElementById(
        "teamCount"
    ).textContent =
        league
            ? league.teams.length
            : 0;

    document.getElementById(
        "matchCount"
    ).textContent =
        league
            ? league.matches.length
            : 0;

    if (!league) {

        document.getElementById(
            "leaderName"
        ).textContent = "-";

        document.getElementById(
            "leaderPoints"
        ).textContent = "0";

        return;
    }

    const standings =
        calculateStandings(league);

    if (!standings.length) {

        document.getElementById(
            "leaderName"
        ).textContent = "-";

        document.getElementById(
            "leaderPoints"
        ).textContent = "0";

        return;
    }

    document.getElementById(
        "leaderName"
    ).textContent =
        standings[0].name;

    document.getElementById(
        "leaderPoints"
    ).textContent =
        standings[0].points;
}


/* =========================================================
   REMOVE TEAM
========================================================= */

function removeTeam(teamId) {

    if (!adminLoggedIn) {

        alert(
            "Administrator access required."
        );

        return;
    }

    const league =
        getCurrentLeague();

    if (!league)
        return;

    const team =
        league.teams.find(
            t => t.id === teamId
        );

    if (!team)
        return;

    if (!confirm(
        `Remove ${team.name}? Existing matches involving this team will also be removed.`
    )) {

        return;
    }

    league.teams =
        league.teams.filter(
            t => t.id !== teamId
        );

    league.matches =
        league.matches.filter(
            match =>
                match.homeId !== teamId &&
                match.awayId !== teamId
        );

    saveDatabase();

    render();
}


/* =========================================================
   DELETE LEAGUE
========================================================= */

function deleteCurrentLeague() {

    if (!adminLoggedIn) {

        alert(
            "Administrator access required."
        );

        return;
    }

    const league =
        getCurrentLeague();

    if (!league) {

        alert(
            "There is no league to delete."
        );

        return;
    }

    if (!confirm(
        `Delete ${league.name}?`
    )) {

        return;
    }

    database.leagues =
        database.leagues.filter(
            l => l.id !== league.id
        );

    currentLeagueId =
        database.leagues.length
            ? database.leagues[0].id
            : null;

    saveDatabase();

    render();
}


/* =========================================================
   CLEAR EVERYTHING
========================================================= */

function clearEverything() {

    if (!adminLoggedIn) {

        alert(
            "Administrator access required."
        );

        return;
    }

    if (!confirm(
        "This will delete ALL leagues, teams and results. Continue?"
    )) {

        return;
    }

    database = {
        leagues: []
    };

    currentLeagueId = null;

    saveDatabase();

    render();
}


/* =========================================================
   ESCAPE HTML
========================================================= */

function escapeHTML(value) {

    return String(value)
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#039;");
}


/* =========================================================
   MAIN RENDER
========================================================= */

function render() {

    renderTabs();

    const league =
        getCurrentLeague();

    renderStats(league);

    renderStandings(league);

    renderResults(league);

    renderTeams(league);

    renderTeamSelectors(league);
}


/* =========================================================
   START
========================================================= */

render();

</script>

</body>
</html>
