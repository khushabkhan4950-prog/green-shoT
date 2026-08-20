<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Green Shot - Friend Hero</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
  font-family:Arial,sans-serif;
}

body{
  background:#050b07;
  color:white;
  min-height:100vh;
}

button{
  border:0;
  cursor:pointer;
}

.screen{
  display:none;
  min-height:100vh;
}

.active{
  display:flex;
}

/* ================= HOME ================= */

#home{
  flex-direction:column;
  justify-content:center;
  align-items:center;
  padding:20px;
  background:
    radial-gradient(circle,#174b25,#050b07 70%);
}

.logo{
  font-size:44px;
  font-weight:bold;
  color:#39ff69;
  text-shadow:0 0 20px #39ff69;
  text-align:center;
}

.subtitle{
  color:#aaa;
  margin:8px 0 25px;
  text-align:center;
}

.profile{
  width:410px;
  max-width:95%;
  background:#101c14;
  border:1px solid #35ff65;
  border-radius:20px;
  padding:20px;
  margin-bottom:18px;
}

.profile h2{
  color:#35ff65;
  margin-bottom:12px;
}

.row{
  display:flex;
  justify-content:space-between;
  padding:9px 0;
  border-bottom:1px solid #293c2e;
}

.id{
  color:#45c7ff;
}

.level{
  color:#ffd83d;
}

.menu{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  justify-content:center;
}

.btn{
  padding:13px 18px;
  border-radius:10px;
  font-weight:bold;
}

.green{
  background:#25f45b;
  color:#001507;
}

.blue{
  background:#168cff;
  color:white;
}

.orange{
  background:#ffad22;
  color:#291700;
}

.purple{
  background:#a855f7;
  color:white;
}

.dark{
  background:#252525;
  color:white;
  border:1px solid #555;
}

/* ================= HOUSES ================= */

#houses{
  flex-direction:column;
  align-items:center;
  padding:30px 15px;
  background:#07100a;
}

.title{
  text-align:center;
  margin-bottom:6px;
}

.sub{
  color:#999;
  text-align:center;
  margin-bottom:25px;
}

.houseGrid{
  width:100%;
  max-width:1000px;
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.house{
  min-height:350px;
  padding:23px;
  border-radius:22px;
  display:flex;
  flex-direction:column;
  justify-content:space-between;
}

.greenHouse{
  background:linear-gradient(145deg,#092e18,#126b2b);
  border:2px solid #31ff63;
}

.goldHouse{
  background:linear-gradient(145deg,#281a05,#9b5b08);
  border:2px solid #ffb52e;
}

.blueHouse{
  background:linear-gradient(145deg,#091c35,#124f91);
  border:2px solid #3ea9ff;
}

.houseIcon{
  text-align:center;
  font-size:60px;
}

.house h2{
  text-align:center;
  margin:8px 0;
}

.house p{
  text-align:center;
  color:#ddd;
}

.houseInfo{
  background:#0004;
  padding:10px;
  border-radius:10px;
  margin-top:12px;
}

.houseInfo div{
  display:flex;
  justify-content:space-between;
  padding:4px;
}

.house button{
  width:100%;
  padding:12px;
  border-radius:10px;
  margin-top:8px;
  font-weight:bold;
}

/* ================= FRIEND ================= */

#friend{
  flex-direction:column;
  align-items:center;
  justify-content:center;
  padding:20px;
  background:
    radial-gradient(circle,#182b4a,#050b07);
}

.friendBox{
  width:450px;
  max-width:95%;
  background:#101b25;
  border:1px solid #35aaff;
  border-radius:22px;
  padding:25px;
}

.friendBox h2{
  color:#45b7ff;
  margin-bottom:18px;
}

.myID{
  background:#07131c;
  border:1px solid #23678e;
  border-radius:10px;
  padding:13px;
  margin-bottom:15px;
}

.myID span{
  color:#999;
}

.myID b{
  display:block;
  color:#45c7ff;
  font-size:22px;
  margin-top:5px;
}

.friendBox input{
  width:100%;
  padding:13px;
  background:#070b0e;
  color:white;
  border:1px solid #555;
  border-radius:9px;
  margin:8px 0 12px;
  font-size:16px;
}

/* FRIEND CARD */

.friendCard{
  display:none;
  margin-top:18px;
  background:#0b2013;
  border:1px solid #35ff65;
  border-radius:16px;
  padding:17px;
}

.friendHero{
  display:flex;
  align-items:center;
  gap:15px;
}

.friendAvatar{
  width:75px;
  height:75px;
  border-radius:50%;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:45px;
  background:linear-gradient(
    135deg,
    #f2bd91,
    #75442f
  );
  border:3px solid #35ff65;
}

.friendInfo{
  flex:1;
}

.friendInfo h3{
  color:#35ff65;
}

.friendInfo p{
  color:#aaa;
  margin-top:4px;
}

/* ================= IDENTITY ================= */

#identity{
  flex-direction:column;
  align-items:center;
  justify-content:center;
  background:#07100a;
  padding:20px;
}

.idBox{
  width:410px;
  max-width:95%;
  background:#111d15;
  border:1px solid #35ff65;
  border-radius:20px;
  padding:25px;
}

.idBox h2{
  color:#35ff65;
  margin-bottom:20px;
}

.field{
  margin:13px 0;
}

.field label{
  display:block;
  color:#aaa;
  margin-bottom:6px;
}

.field input,
.field select{
  width:100%;
  padding:12px;
  border-radius:8px;
  border:1px solid #555;
  background:#080b09;
  color:white;
}

/* ================= GAME ================= */

#game{
  position:relative;
  flex-direction:column;
  overflow:hidden;
}

.gameTop{
  height:65px;
  background:#050805;
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:0 12px;
  z-index:20;
}

.gameArea{
  position:relative;
  flex:1;
  overflow:hidden;
  background:#102719;
}

/* FRIEND TAG */

.friendTag{
  position:absolute;
  top:15px;
  left:50%;
  transform:translateX(-50%);
  background:#071b0d;
  border:1px solid #35ff65;
  padding:9px 15px;
  border-radius:20px;
  z-index:10;
  font-size:13px;
  display:none;
}

/* HERO */

.hero{
  position:absolute;
  bottom:30px;
  width:75px;
  height:120px;
  text-align:center;
  transition:left .1s;
}

.myHero{
  left:45%;
}

.friendHeroGame{
  left:65%;
  bottom:75px;
  display:none;
}

.heroFace{
  width:45px;
  height:45px;
  border-radius:50%;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:30px;
  background:
    linear-gradient(
      135deg,
      #f2bf95,
      #74452f
    );
  border:2px solid #111;
}

.heroHair{
  width:45px;
  height:15px;
  background:#21140d;
  border-radius:50% 50% 20% 20%;
  margin:-43px auto 28px;
  position:relative;
  z-index:2;
}

.heroBody{
  width:58px;
  height:65px;
  margin:auto;
  background:#168cff;
  border-radius:12px 12px 5px 5px;
  border:2px solid #07101a;
}

.friendHeroGame .heroBody{
  background:#a855f7;
}

.heroName{
  font-size:11px;
  margin-top:4px;
  color:#fff;
  white-space:nowrap;
}

/* ENEMY */

.enemy{
  position:absolute;
  width:55px;
  height:80px;
}

.enemyHead{
  width:34px;
  height:34px;
  border-radius:50%;
  background:#df9a70;
  margin:auto;
}

.enemyBody{
  width:45px;
  height:48px;
  background:#e72d36;
  border-radius:9px;
  margin:auto;
}

/* BULLET */

.bullet{
  position:absolute;
  width:7px;
  height:22px;
  background:#ffe63b;
  border-radius:10px;
  box-shadow:0 0 12px #ffe63b;
}

/* CONTROLS */

.gameControls{
  height:110px;
  background:#050805;
  display:flex;
  justify-content:center;
  align-items:center;
  gap:20px;
}

.control{
  width:85px;
  height:65px;
  background:#252525;
  color:white;
  border-radius:15px;
  font-size:25px;
}

.fire{
  width:95px;
  height:75px;
  border-radius:50%;
  background:#35ff65;
  color:#001507;
  font-size:24px;
  box-shadow:0 0 20px #35ff65;
}

/* ================= PROFILE POPUP ================= */

#profilePopup{
  position:fixed;
  inset:0;
  background:#000b;
  display:none;
  align-items:center;
  justify-content:center;
  z-index:100;
}

.profilePopupBox{
  width:390px;
  max-width:92%;
  background:#101c14;
  border:2px solid #35ff65;
  border-radius:20px;
  padding:24px;
}

.profilePopupBox h2{
  color:#35ff65;
  margin-bottom:15px;
}

.profileLine{
  display:flex;
  justify-content:space-between;
  padding:10px 0;
  border-bottom:1px solid #293c2e;
}

/* ================= SETTINGS ================= */

#settingsPopup{
  position:fixed;
  inset:0;
  background:#000b;
  display:none;
  align-items:center;
  justify-content:center;
  z-index:90;
}

.settingsBox{
  width:380px;
  max-width:92%;
  background:#111d15;
  border:2px solid #35ff65;
  border-radius:20px;
  padding:24px;
}

.settingsBox h2{
  color:#35ff65;
  margin-bottom:18px;
}

/* TOAST */

#toast{
  position:fixed;
  bottom:25px;
  left:50%;
  transform:translateX(-50%);
  background:#25f45b;
  color:#001507;
  padding:12px 20px;
  border-radius:10px;
  font-weight:bold;
  display:none;
  z-index:200;
}

@media(max-width:800px){

  .houseGrid{
    grid-template-columns:1fr;
    max-width:450px;
  }

  .logo{
    font-size:35px;
  }

  .gameTop{
    font-size:12px;
  }
}
</style>
</head>

<body>

<!-- ================= HOME ================= -->

<section id="home" class="screen active">

  <div class="logo">
    🟢 GREEN SHOT
  </div>

  <div class="subtitle">
    Friend + Hero Multiplayer
  </div>

  <div class="profile">

    <h2>👤 MY PLAYER</h2>

    <div class="row">
      <span>Name</span>
      <b id="homeName"></b>
    </div>

    <div class="row">
      <span>Player ID</span>
      <b class="id" id="homeID"></b>
    </div>

    <div class="row">
      <span>School</span>
      <b id="homeSchool"></b>
    </div>

    <div class="row">
      <span>Level</span>
      <b class="level" id="homeLevel"></b>
    </div>

  </div>

  <div class="menu">

    <button
      class="btn green"
      onclick="openHouses()">
      🎮 START GAME
    </button>

    <button
      class="btn blue"
      onclick="openFriend()">
      👥 FIND FRIEND
    </button>

    <button
      class="btn orange"
      onclick="openIdentity()">
      🆔 CHANGE ID
    </button>

    <button
      class="btn purple"
      onclick="openProfilePopup()">
      👤 PROFILE
    </button>

  </div>

</section>


<!-- ================= HOUSES ================= -->

<section id="houses" class="screen">

  <h1 class="title">
    🏠 CHOOSE GAME HOUSE
  </h1>

  <p class="sub">
    ہر House کا اپنا رنگ اور mode ہے
  </p>

  <div class="houseGrid">

    <div class="house greenHouse">

      <div>

        <div class="houseIcon">
          🟢
        </div>

        <h2>Green Arena</h2>

        <p>Normal Battle</p>

        <div class="houseInfo">

          <div>
            <span>Color</span>
            <b>Green</b>
          </div>

          <div>
            <span>Speed</span>
            <b>Fast</b>
          </div>

        </div>

      </div>

      <button
        class="green"
        onclick="enterGame(1)">
        ▶ ENTER
      </button>

      <button
        class="green"
        onclick="openSettings(1)">
        ⚙ SETTINGS
      </button>

    </div>


    <div class="house goldHouse">

      <div>

        <div class="houseIcon">
          🟠
        </div>

        <h2>Golden Arena</h2>

        <p>Hard Battle</p>

        <div class="houseInfo">

          <div>
            <span>Color</span>
            <b>Gold</b>
          </div>

          <div>
            <span>Speed</span>
            <b>Very Fast</b>
          </div>

        </div>

      </div>

      <button
        class="orange"
        onclick="enterGame(2)">
        ▶ ENTER
      </button>

      <button
        class="orange"
        onclick="openSettings(2)">
        ⚙ SETTINGS
      </button>

    </div>


    <div class="house blueHouse">

      <div>

        <div class="houseIcon">
          🔵
        </div>

        <h2>Blue Arena</h2>

        <p>Easy Battle</p>

        <div class="houseInfo">

          <div>
            <span>Color</span>
            <b>Blue</b>
          </div>

          <div>
            <span>Speed</span>
            <b>Slow</b>
          </div>

        </div>

      </div>

      <button
        class="blue"
        onclick="enterGame(3)">
        ▶ ENTER
      </button>

      <button
        class="blue"
        onclick="openSettings(3)">
        ⚙ SETTINGS
      </button>

    </div>

  </div>

  <button
    class="back"
    onclick="goHome()">
    ← HOME
  </button>

</section>


<!-- ================= FRIEND SCREEN ================= -->

<section id="friend" class="screen">

  <div class="friendBox">

    <h2>
      👥 FIND FRIEND + HERO
    </h2>

    <div class="myID">

      <span>Your Player ID</span>

      <b id="friendMyID"></b>

    </div>

    <label>
      Friend کا Player ID
    </label>

    <input
      id="friendID"
      placeholder="مثلاً GS-002030">

    <button
      class="btn blue"
      style="width:100%"
      onclick="findFriend()">
      🔎 FIND FRIEND
    </button>


    <!-- FRIEND CARD -->

    <div
      id="friendCard"
      class="friendCard">

      <div class="friendHero">

        <div
          class="friendAvatar"
          id="friendAvatar">
          🦸
        </div>

        <div class="friendInfo">

          <h3 id="friendName">
            Friend
          </h3>

          <p id="friendDetails">
            Player
          </p>

        </div>

      </div>

      <button
        class="btn green"
        style="width:100%;margin-top:15px"
        onclick="playWithFriend()">
        🤝 PLAY TOGETHER
      </button>

    </div>


    <button
      class="back"
      onclick="goHome()">
      ← HOME
    </button>

  </div>

</section>


<!-- ================= IDENTITY ================= -->

<section id="identity" class="screen">

  <div class="idBox">

    <h2>
      🆔 PLAYER ID
    </h2>

    <div class="field">

      <label>
        Your Name
      </label>

      <input
        id="editName">

    </div>


    <div class="field">

      <label>
        School
      </label>

      <input
        id="editSchool">

    </div>


    <div class="field">

      <label>
        Current Player ID
      </label>

      <input
        id="editID"
        readonly>

    </div>


    <button
      class="btn orange"
      style="width:100%"
      onclick="changeID()">
      🔄 CHANGE ID
    </button>


    <button
      class="btn green"
      style="width:100%;margin-top:8px"
      onclick="saveIdentity()">
      ✓ SAVE
    </button>


    <button
      class="back"
      onclick="goHome()">
      ← BACK
    </button>

  </div>

</section>


<!-- ================= GAME ================= -->

<section id="game" class="screen">

  <div class="gameTop">

    <b id="gameName">
      🟢 Green Arena
    </b>

    <span>
      🎯 <b id="score">0</b>
      ❤️ <b id="health">100</b>
    </span>

    <button
      class="btn dark"
      onclick="openProfilePopup()">
      👤
    </button>

  </div>


  <div
    id="gameArea"
    class="gameArea">


    <!-- FRIEND TAG -->

    <div
      id="friendTag"
      class="friendTag">
    </div>


    <!-- MY HERO -->

    <div
      id="myHero"
      class="hero myHero">

      <div class="heroFace">
        🧑
      </div>

      <div class="heroHair"></div>

      <div class="heroBody"></div>

      <div
        class="heroName"
        id="myHeroName">
        You
      </div>

    </div>


    <!-- FRIEND HERO -->

    <div
      id="friendHeroGame"
      class="hero friendHeroGame">

      <div
        class="heroFace"
        id="friendGameFace">
        🦸
      </div>

      <div class="heroHair"></div>

      <div class="heroBody"></div>

      <div
        class="heroName"
        id="friendHeroName">
        Friend
      </div>

    </div>

  </div>


  <div class="gameControls">

    <button
      class="control"
      onclick="moveLeft()">
      ◀
    </button>

    <button
      class="fire"
      onclick="fire()">
      🎯
    </button>

    <button
      class="control"
      onclick="moveRight()">
      ▶
    </button>

  </div>

</section>


<!-- ================= PROFILE POPUP ================= -->

<div id="profilePopup">

  <div class="profilePopupBox">

    <h2>
      👤 MY PROFILE
    </h2>

    <div class="profileLine">
      <span>Name</span>
      <b id="popName"></b>
    </div>

    <div class="profileLine">
      <span>Player ID</span>
      <b id="popID"></b>
    </div>

    <div class="profileLine">
      <span>School</span>
      <b id="popSchool"></b>
    </div>

    <div class="profileLine">
      <span>Level</span>
      <b id="popLevel"></b>
    </div>

    <button
      class="btn green"
      style="width:100%;margin-top:18px"
      onclick="closeProfilePopup()">
      ✕ CLOSE
    </button>

  </div>

</div>


<!-- ================= SETTINGS ================= -->

<div id="settingsPopup">

  <div class="settingsBox">

    <h2 id="settingsTitle">
      ⚙ House Settings
    </h2>

    <div class="field">

      <label>
        🎨 Color
      </label>

      <select id="settingColor">

        <option value="green">
          Green
        </option>

        <option value="gold">
          Gold
        </option>

        <option value="blue">
          Blue
        </option>

      </select>

    </div>


    <div class="field">

      <label>
        🎯 Difficulty
      </label>

      <select id="settingDifficulty">

        <option>
          Easy
        </option>

        <option>
          Normal
        </option>

        <option>
          Hard
        </option>

      </select>

    </div>


    <button
      class="btn green"
      style="width:100%"
      onclick="saveSettings()">
      ✓ SAVE
    </button>


    <button
      class="btn dark"
      style="width:100%;margin-top:8px"
      onclick="closeSettings()">
      ✕ CLOSE
    </button>

  </div>

</div>


<div id="toast"></div>


<script>

/* =========================
   PLAYER DATA
========================= */

let myName =
  localStorage.getItem("gs_name")
  || "Player";

let mySchool =
  localStorage.getItem("gs_school")
  || "My School";

let myID =
  localStorage.getItem("gs_id")
  || createID();

let myLevel =
  Number(
    localStorage.getItem("gs_level")
  ) || 1;


/* =========================
   ID GENERATOR
========================= */

function createID(){

  return "GS-" +
    String(
      Math.floor(
        Math.random()*1000000
      )
    ).padStart(6,"0");

}


/* =========================
   DEMO FRIEND DATABASE
========================= */

const friends = [

  {
    id:"GS-002030",
    name:"Ronaldo Hero",
    school:"Future School",
    level:12,
    hero:"⚽",
    heroColor:"purple"
  },

  {
    id:"GS-003003",
    name:"Football King",
    school:"City School",
    level:8,
    hero:"🦸",
    heroColor:"blue"
  },

  {
    id:"GS-004040",
    name:"Green Warrior",
    school:"Smart School",
    level:15,
    hero:"🥷",
    heroColor:"green"
  },

  {
    id:"GS-005050",
    name:"Golden Player",
    school:"Public School",
    level:20,
    hero:"👑",
    heroColor:"gold"
  }

];


let selectedFriend = null;


/* =========================
   PROFILE
========================= */

function updateHome(){

  document.getElementById(
    "homeName"
  ).textContent = myName;

  document.getElementById(
    "homeID"
  ).textContent = myID;

  document.getElementById(
    "homeSchool"
  ).textContent = mySchool;

  document.getElementById(
    "homeLevel"
  ).textContent = myLevel;

}


updateHome();


/* =========================
   SCREEN SYSTEM
========================= */

function hideAll(){

  document
    .querySelectorAll(".screen")
    .forEach(s=>{
      s.classList.remove("active");
    });

}


function goHome(){

  stopGame();

  hideAll();

  document
    .getElementById("home")
    .classList.add("active");

  updateHome();

}


/* =========================
   HOUSES
========================= */

function openHouses(){

  hideAll();

  document
    .getElementById("houses")
    .classList.add("active");

}


/* =========================
   FRIEND
========================= */

function openFriend(){

  hideAll();

  document
    .getElementById("friend")
    .classList.add("active");

  document.getElementById(
    "friendMyID"
  ).textContent = myID;

  document.getElementById(
    "friendCard"
  ).style.display = "none";

}


function findFriend(){

  const id =
    document
      .getElementById("friendID")
      .value
      .trim()
      .toUpperCase();


  if(!id){

    showToast(
      "⚠ Friend ID لکھیں"
    );

    return;

  }


  if(id === myID){

    showToast(
      "❌ یہ آپ کا اپنا ID ہے"
    );

    return;

  }


  selectedFriend =
    friends.find(
      f => f.id === id
    );


  if(!selectedFriend){

    showToast(
      "❌ Friend نہیں ملا"
    );

    document.getElementById(
      "friendCard"
    ).style.display = "none";

    return;

  }


  document.getElementById(
    "friendCard"
  ).style.display = "block";


  document.getElementById(
    "friendName"
  ).textContent =
    selectedFriend.hero +
    " " +
    selectedFriend.name;


  document.getElementById(
    "friendDetails"
  ).textContent =
    "ID: " +
    selectedFriend.id +
    " • Level: " +
    selectedFriend.level +
    " • " +
    selectedFriend.school;


  document.getElementById(
    "friendAvatar"
  ).textContent =
    selectedFriend.hero;


  showToast(
    "✓ Friend Found"
  );

}


/* =========================
   PLAY TOGETHER
========================= */

function playWithFriend(){

  if(!selectedFriend){

    showToast(
      "پہلے Friend تلاش کریں"
    );

    return;

  }


  showToast(
    "🤝 Match Room Created!"
  );


  setTimeout(()=>{

    enterGame(1);

  },700);

}


/* =========================
   IDENTITY
========================= */

function openIdentity(){

  hideAll();

  document
    .getElementById("identity")
    .classList.add("active");


  document.getElementById(
    "editName"
  ).value = myName;


  document.getElementById(
    "editSchool"
  ).value = mySchool;


  document.getElementById(
    "editID"
  ).value = myID;

}


function changeID(){

  myID = createID();

  document.getElementById(
    "editID"
  ).value = myID;


  showToast(
    "🆔 New ID: " + myID
  );

}


function saveIdentity(){

  myName =
    document
      .getElementById("editName")
      .value
      .trim()
      || "Player";


  mySchool =
    document
      .getElementById("editSchool")
      .value
      .trim()
      || "My School";


  localStorage.setItem(
    "gs_name",
    myName
  );

  localStorage.setItem(
    "gs_school",
    mySchool
  );

  localStorage.setItem(
    "gs_id",
    myID
  );


  updateHome();

  showToast(
    "✓ Profile Saved"
  );


  setTimeout(
    goHome,
    700
  );

}


/* =========================
   PROFILE POPUP
========================= */

function openProfilePopup(){

  document.getElementById(
    "popName"
  ).textContent = myName;

  document.getElementById(
    "popID"
  ).textContent = myID;

  document.getElementById(
    "popSchool"
  ).textContent = mySchool;

  document.getElementById(
    "popLevel"
  ).textContent = myLevel;


  document.getElementById(
    "profilePopup"
  ).style.display = "flex";

}


function closeProfilePopup(){

  document.getElementById(
    "profilePopup"
  ).style.display = "none";

}


/* =========================
   HOUSE SETTINGS
========================= */

let selectedHouse = 1;


const houseSettings = {

  1:{
    color:"green",
    difficulty:"Normal"
  },

  2:{
    color:"gold",
    difficulty:"Hard"
  },

  3:{
    color:"blue",
    difficulty:"Easy"
  }

};


function openSettings(house){

  selectedHouse = house;

  document.getElementById(
    "settingsTitle"
  ).textContent =
    "⚙ House " +
    house +
    " Settings";


  document.getElementById(
    "settingColor"
  ).value =
    houseSettings[
      house
    ].color;


  document.getElementById(
    "settingDifficulty"
  ).value =
    houseSettings[
      house
    ].difficulty;


  document.getElementById(
    "settingsPopup"
  ).style.display =
    "flex";

}


function closeSettings(){

  document.getElementById(
    "settingsPopup"
  ).style.display =
    "none";

}


function saveSettings(){

  houseSettings[
    selectedHouse
  ].color =
    document.getElementById(
      "settingColor"
    ).value;


  houseSettings[
    selectedHouse
  ].difficulty =
    document.getElementById(
      "settingDifficulty"
    ).value;


  closeSettings();

  showToast(
    "✓ House Settings Saved"
  );

}


/* =========================
   GAME
========================= */

let currentHouse = 1;

let running = false;

let score = 0;

let health = 100;

let playerX = 45;

let enemyTimer;

let damageTimer;


function enterGame(house){

  currentHouse = house;

  hideAll();

  document
    .getElementById("game")
    .classList.add("active");


  const names = {

    1:"🟢 Green Arena",

    2:"🟠 Golden Arena",

    3:"🔵 Blue Arena"

  };


  document.getElementById(
    "gameName"
  ).textContent =
    names[house];


  const colors = {

    green:
      "linear-gradient(#12351b,#081109)",

    gold:
      "linear-gradient(#4b3108,#120b03)",

    blue:
      "linear-gradient(#0b3150,#06111b)"

  };


  document.getElementById(
    "gameArea"
  ).style.background =
    colors[
      houseSettings[
        house
      ].color
    ];


  setupHeroes();

  startGame();

}


/* =========================
   HERO SETUP
========================= */

function setupHeroes(){

  document.getElementById(
    "myHeroName"
  ).textContent =
    myName;


  const friendHero =
    document.getElementById(
      "friendHeroGame"
    );


  if(selectedFriend){

    friendHero.style.display =
      "block";


    document.getElementById(
      "friendHeroName"
    ).textContent =
      selectedFriend.name;


    document.getElementById(
      "friendGameFace"
    ).textContent =
      selectedFriend.hero;


    document.getElementById(
      "friendTag"
    ).style.display =
      "block";


    document.getElementById(
      "friendTag"
    ).textContent =
      "🤝 " +
      selectedFriend.name +
      " • " +
      selectedFriend.id;

  }else{

    friendHero.style.display =
      "none";


    document.getElementById(
      "friendTag"
    ).style.display =
      "none";

  }

}


/* =========================
   START
========================= */

function startGame(){

  running = true;

  score = 0;

  health = 100;

  playerX = 45;


  document.getElementById(
    "score"
  ).textContent = "0";


  document.getElementById(
    "health"
  ).textContent = "100";


  document.getElementById(
    "myHero"
  ).style.left =
    "45%";


  document
    .getElementById("gameArea")
    .querySelectorAll(
      ".enemy,.bullet"
    )
    .forEach(
      e=>e.remove()
    );


  startEnemies();

  startDamage();

}


function stopGame(){

  running = false;

  clearInterval(
    enemyTimer
  );

  clearInterval(
    damageTimer
  );

}


/* =========================
   MOVEMENT
========================= */

function moveLeft(){

  if(!running)return;

  playerX -= 5;

  if(playerX < 5)
    playerX = 5;


  document.getElementById(
    "myHero"
  ).style.left =
    playerX + "%";

}


function moveRight(){

  if(!running)return;

  playerX += 5;

  if(playerX > 90)
    playerX = 90;


  document.getElementById(
    "myHero"
  ).style.left =
    playerX + "%";

}


/* =========================
   FIRE
========================= */

function fire(){

  if(!running)return;


  const bullet =
    document.createElement(
      "div"
    );

  bullet.className =
    "bullet";


  const hero =
    document.getElementById(
      "myHero"
    );


  let x =
    hero.offsetLeft + 34;


  let y =
    hero.offsetTop;


  bullet.style.left =
    x + "px";


  bullet.style.top =
    y + "px";


  document
    .getElementById("gameArea")
    .appendChild(
      bullet
    );


  let timer =
    setInterval(()=>{

      y -= 12;

      bullet.style.top =
        y + "px";


      document
        .querySelectorAll(
          ".enemy"
        )
        .forEach(
          enemy=>{

            if(
              collision(
                bullet,
                enemy
              )
            ){

              enemy.remove();

              bullet.remove();

              clearInterval(
                timer
              );

              score += 10;


              document.getElementById(
                "score"
              ).textContent =
                score;

            }

          }
        );


      if(y < -30){

        bullet.remove();

        clearInterval(
          timer
        );

      }

    },30);

}


/* =========================
   COLLISION
========================= */

function collision(a,b){

  const A =
    a.getBoundingClientRect();

  const B =
    b.getBoundingClientRect();


  return(
    A.left < B.right &&
    A.right > B.left &&
    A.top < B.bottom &&
    A.bottom > B.top
  );

}


/* =========================
   ENEMIES
========================= */

function startEnemies(){

  clearInterval(
    enemyTimer
  );


  const speed = {

    1:900,

    2:600,

    3:1500

  }[currentHouse];


  enemyTimer =
    setInterval(
      createEnemy,
      speed
    );


  createEnemy();

}


function createEnemy(){

  if(!running)return;


  const enemy =
    document.createElement(
      "div"
    );


  enemy.className =
    "enemy";


  enemy.innerHTML = `
    <div class="enemyHead"></div>
    <div class="enemyBody"></div>
  `;


  enemy.style.left =
    Math.random()*90 + "%";


  enemy.style.top =
    Math.random()*55 + "%";


  document
    .getElementById("gameArea")
    .appendChild(
      enemy
    );


  setTimeout(()=>{

    if(enemy.parentNode)
      enemy.remove();

  },4000);

}


/* =========================
   DAMAGE
========================= */

function startDamage(){

  clearInterval(
    damageTimer
  );


  const speed = {

    1:2000,

    2:1000,

    3:3000

  }[currentHouse];


  damageTimer =
    setInterval(()=>{

      if(!running)return;


      health -= 5;


      document.getElementById(
        "health"
      ).textContent =
        health;


      if(health <= 0){

        stopGame();


        showToast(
          "💥 GAME OVER"
        );


        setTimeout(
          openHouses,
          1000
        );

      }

    },speed);

}


/* =========================
   TOAST
========================= */

function showToast(text){

  const toast =
    document.getElementById(
      "toast"
    );


  toast.textContent =
    text;


  toast.style.display =
    "block";


  setTimeout(()=>{

    toast.style.display =
      "none";

  },2000);

}

</script>

</body>
</html>
