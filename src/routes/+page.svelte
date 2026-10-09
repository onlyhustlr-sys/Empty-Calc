
<script>

let em = $state("")
  
const cf=(e)=>{
    let val = e.target.textContent;
  if (val=="X") {
    val="*"
  }
  if (val=="=") {
    em=eval(em)
  }
  else{
    em+=val
  }
}
    </script>

<div>
<h1 class="ch">My Funny Calculator</h1>

<br><br>
<div class="cbd">
<div class="scr">
{em}
</div>
<button class="bt" onclick={cf}>1</button>
<button class="bt" onclick={cf}>2</button>
<button class="bt" onclick={cf}>3</button>

<button class="bt" onclick={cf}>4</button>
<button class="bt" onclick={cf}>5</button>
<button class="bt" onclick={cf}>6</button>

<button class="bt" onclick={cf}>7</button>
<button class="bt" onclick={cf}>8</button>
<button class="bt" onclick={cf}>9</button>

<button class="bt" onclick={cf}>0</button>

<button class="bt" onclick={cf}>+</button>
<button class="bt" onclick={cf}>-</button>
<button class="bt" onclick={cf}>/</button>
<button class="bt" onclick={cf}>X</button>
<button class="bt" onclick={cf}>=</button>
</div>
</div>

<style>
.cbd{
    display: flex;
    flex-direction:row;
    flex-wrap: wrap;
    justify-content: center;
}
.scr{
    min-width: 78vw;
    min-height: 10vh;
    margin: 5%;
  text-align: center;
    background-color: aqua;
    border-radius:2vw;
}
.bt{
    background-color:lightblue;
    width:20vw;
    height:8vh;
    text-align: center;
    margin:5%;
    align-self: center;
    font-family:courier ;
    font-size: 7vh;
    user-select: none;
}
.bt:active{
    background: lightseagreen;
}

:global(body){
    background-color: pink;margin: 0%;
    padding: 0%;
    display:flex;
    justify-content: center;
}
    button{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    h1{
        font-family: fantasy;
        font-variant: petite-caps;
        font-size: 8vw;
        color: hotpink;
        outline: double  red 2vh ;
        text-align: center;
        padding: 3%;
        width: 90vw;
        border-radius: 10vw;
        align-self:center;
    }
    .cbd{
        background-color: black;
    }
</style>_