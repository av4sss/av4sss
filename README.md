<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Quer namorar comigo?</title>
    <style>
      .box {
        display: flex;
        align-items: center;
        flex-direction: column;

        font-family: "Haas Grot Text R Web", "Helvetica Neue", Helvetica, Arial,
          sans-serif;
      }

      .buttons {
        display: block;
        width: 200px;
        margin-left: 100px;
      }

      .button {
        cursor: pointer;
        display: inline-block;
        font-size: 14px;
        font-weight: 500;
        border-radius: 8px;
        line-height: 20px;
        list-style: none;
        margin: 0;
        user-select: none;
        -webkit-user-select: none;
        touch-action: manipulation;
        vertical-align: baseline;
        text-align: center;
        padding: 10px 16px;
        border-style: none;
      }

      .button-1 {
        background-color: #ea4c89;
        color: #ffffff;
        transition: color 100ms;

        margin-right: 10px;
      }

      .button-1:hover {
        background-color: #f082ac;
      }

      .button-2 {
        background-color: rgb(216, 216, 216);
        color: #333333;
        transition: all 200ms;

        z-index: 1000;
      }
    </style>
  </head>
  <body>
    <div class="box">
      <h1>Quer namorar comigo?</h1>
      <div class="buttons">
        <button class="button button-1" id="sim">Sim</button>
        <button class="button button-2" id="nao">Não</button>
      </div>
    </div>
  </body>
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      const naoButton = document.getElementById("nao");
      const simButton = document.getElementById("sim");

      simButton.addEventListener("click", function () {
        alert(" eu te amo minha princesa S2!");
      });

      const handleNao = function () {
        naoButton.style.position = "fixed";

        const randTop =
          Math.random() * (window.innerHeight - naoButton.offsetHeight);
        const randLeft =
          Math.random() * (window.innerWidth - naoButton.offsetWidth);

        naoButton.style.top = randTop + "px";
        naoButton.style.left = randLeft + "px";
      };

      naoButton.addEventListener("click", handleNao);
      naoButton.addEventListener("mouseover", handleNao);
    });
  </script>
  </html> 
