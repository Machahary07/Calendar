# Calendar – February 2026  
Fundamentals of Web Design (FWD) Assignment with localhost installation guide and netlify hosted site

Submitted by **Jeu Machahary**  
BTech CSE – 4th Semester  
Section - B

---

# Raw Design

![Raw Design](public/rawDesign.png)

---

# CODE

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <link rel="icon" type="image/svg+xml" href="/Calendar-favicon.svg" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Calendar</title>
  <link rel="stylesheet" href="/global.css">
</head>

<body>

<div class="wrapper">

  <div class="left">
    <div class="decor-line"></div>

    <div class="holidays">
      <strong>1</strong> Guru Ravidas Jayanti<br>
      <strong>12</strong> Maharishi Dayanand Saraswati Jayanti<br>
      <strong>15</strong> Maha Shivaratri<br>
      <strong>19</strong> Shivaji Jayanti
    </div>

    <img src="/months/February-image.svg" class="month-image" alt="February Art">

    <div class="month-title">
      <span class="feb">FEB</span>
      <span class="rua">RUA</span>
      <span class="ry">RY</span>
    </div>
  </div>

  <div class="right">

    <div class="year">2026</div>
    <div class="year-line"></div>

    <table>
      <thead>
        <tr>
          <th>SUN</th>
          <th>MON</th>
          <th>TUE</th>
          <th>WED</th>
          <th>THU</th>
          <th>FRI</th>
          <th>SAT</th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td><span class="highlight">1</span></td>
          <td>2</td>
          <td>3</td>
          <td>4</td>
          <td>5</td>
          <td>6</td>
          <td>7</td>
        </tr>
        <tr>
          <td class="sunday">8</td>
          <td>9</td>
          <td>10</td>
          <td>11</td>
          <td><span class="highlight">12</span></td>
          <td>13</td>
          <td>14</td>
        </tr>
        <tr>
          <td class="sunday">15</td>
          <td>16</td>
          <td>17</td>
          <td>18</td>
          <td><span class="highlight">19</span></td>
          <td>20</td>
          <td>21</td>
        </tr>
        <tr>
          <td class="sunday">22</td>
          <td>23</td>
          <td>24</td>
          <td>25</td>
          <td>26</td>
          <td>27</td>
          <td>28</td>
        </tr>
      </tbody>
    </table>

  </div>
</div>

<footer class="footer">
  <div class="footer-content">
    <div class="footer-left">
      <div class="footer-logo">
        <img src="/calendar-logo-white.svg" alt="Calendar Logo">
        <h2>Calendar</h2>
      </div>

      <p>
        Calendar is an opensource Fundamentals of Web Design (FWD) Assignment
        submitted by Jeu Machahary, BTech CSE 4th Sem to Mr. Spandan Sir.
      </p>
    </div>

    <div class="footer-right">
      <a href="https://github.com/machahary07/calendar" target="_blank">
        <img src="/GitHub_Invertocat_White.svg" alt="GitHub">
      </a>

      <p>
        Sourcecode Available in here:<br>
        <a href="https://github.com/machahary07/calendar" target="_blank">
          www.github.com/machahary07/calendar
        </a>
      </p>
    </div>
  </div>

  <img src="/Calendar-footer.svg" class="footer-bg" alt="Calendar Footer Background">
</footer>

</body>
</html>
```
---

# CSS

```css
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family: Arial, Helvetica, sans-serif;
}

::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar-track {
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: #e53935;
}

body{
  background:#efefef;
  min-height:100vh; 
  padding-bottom:400px;
  scroll-behavior:smooth;
}

.wrapper{
  width:100%;
  min-height:100vh;
  display:flex;
  padding:6vh 5vw;
  position:relative;
  z-index:2;
  background:#efefef;
}

.left{
  width:45%;
  position:relative;
}

.decor-line{
  width:4vw;
  height:2px;
  background:#e53935;
  margin-bottom:1.5vw;
}

.holidays{
  color:#e53935;
  font-size:1vw;
  line-height:1.8;
}

.month-image{
  position:absolute;
  bottom:-20px;
  left:-165px;
  width:45vw;
  max-width:500px;
  opacity:1;
  transform: rotate(35deg);
  transform-origin: center;
}

.month-title{
  position:absolute;
  top:45%;
  left:45%;
  transform:translateY(-20%);
  font-size:8vw;
  font-weight:300;
  color:#e53935;
  line-height:0.9;
  letter-spacing:0.4vw;
}

.month-title span{
  display:block;
}

.feb{
  margin-left:2vw;
}

.rua{
  margin-left:4vw;
}

.ry{
  margin-left:0;
}

.right{
  width:55%;
  padding-left:5vw;
  display:flex;
  flex-direction:column;
}

.year{
  text-align:right;
  font-size:5vw;
  font-weight:300;
  color:#e53935;
}

.year-line{
  width:20vw;
  height:2px;
  background:#e53935;
  margin-left:auto;
  margin-top:1vw;
  margin-bottom:4vh;
}

table{
  width:100%;
  border-collapse:collapse;
  text-align:center;
}

th{
  font-size:1.2vw;
  padding:1.2vw 0;
  font-weight:bold;
}

th:first-child{
  color:#e53935;
}

td{
  font-size:1.3vw;
  padding:1.5vw 0;
}

.sunday{
  color:#e53935;
}

.highlight{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  width:3vw;
  height:3vw;
  border-radius:50%;
  background:#e53935;
  color:white;
}

.footer{
  position: fixed;
  bottom: 0;
  height:400px;
  width:100%;
  background:#e53935;
  color:white;
  padding:8vh 5vw 18vh 5vw;
  overflow:hidden;
  z-index: 0;
}

.footer-content{
  display:flex;
  justify-content:space-between;
  align-items:flex-start;
  position:relative;
  z-index:2;
}

.footer-left{
  max-width:50%;
}

.footer-logo{
  display:flex;
  align-items:center;
  gap:15px;
  margin-bottom:20px;
}

.footer-logo h2{
  font-size:3vw;
  font-weight:700;
}

.footer-left p{
  font-size:1.1vw;
  line-height:1.6;
}

.footer-right{
  text-align:right;
}

.footer-right img{
  width:60px;
  margin-bottom:15px;
}

.footer-right p{
  font-size:1.1vw;
}

.footer-right a{
  color:white;
  text-decoration:underline;
}

.footer-bg{
  position:absolute;
  bottom:-60%;
  left:0;
  width:100%;
  z-index:1;
}

.footer-logo img{
  width:60px;
  height:auto;
}
```

---

# OUTPUT

https://calendarbyjeu.netlify.app/

---

# Installation (Run Locally)

### 1. Clone the Repository

```bash
git clone https://github.com/machahary07/calendar.git
```

### 2. Navigate into the Project Folder

```bash
cd calendar
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Run Development Server

```bash
npm run dev
```

Now open the local server link shown in your terminal (usually):

```
http://localhost:5173
```
