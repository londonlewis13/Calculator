let global1= parseFloat("0");
let global2 = parseFloat("0");
var done = false;
let varnum = 1;
let process;

function numberKey(element) {
  let display =document.getElementById('display');
  let displayText = display.innerText;

  if(done === true){
    displayText = "0";
    process = " ";
    global1 = "0";
    global2 = "0";
    varnum = 1;
    done = false;
  }
  
  console.log(varnum);
  if(displayText === "0"){
    displayText = element.innerText;
    if(varnum === 1){
      global1 += element.innerText;
    } else{ global2 += element.innerText; }

    
  } else if(element.innerText === "ON/C"){
    displayText = "0";
    process = " ";
    global1 = "0";
    global2 = "0";
    varnum = 1;

    
  }else if(element.innerText === "(-)"){
    let displayCopy = displayText;
    delete displayText ;
    displayText += "-";
    displayText += displayCopy;  
    if(varnum === 1){
      global1 += element.innerText;
    } else{ global2 += element.innerText; }

    
  }
  else if(element.innerText === "="){
    displayText = display.innerText(0);
    if(varnum === 1){
      global1 += element.innerText;
    } else{ global2 += element.innerText; }
  }  
  else{
    displayText += element.innerText;
    if(varnum === 1){
      global1 += element.innerText;
    } else{ global2 += element.innerText; }
    
  }
  
  display.innerText = displayText;
  console.log(global1);
  console.log(global2);
  //calculate
  
}

function processKey(element){
  let display =document.getElementById('display');
  let displayText = display.innerText;
  
  displayText += element.innerText;
  varnum = 2;
  process = element.innerText;

  display.innerText = displayText;
  console.log(global1);
  console.log(global2);
  console.log(process);
}

function calculate(){
  console.log("It works");
  let display =document.getElementById('display');
  let final;
  if(done === true){
    final = "0";
    process = " ";
    global1 = "0";
    global2 = "0";
    varnum = 1;
    done = false;
  }
  if(process === "+"){
    final = parseFloat(global1) + parseFloat(global2);

  } else if(process === "–"){
    final = parseFloat(global1) - parseFloat(global2);

  }else if(process === "×"){
    final = global1 * global2;
   
  }else if(process ==="√"){
    final = Math.sqrt(global1);

    
  }else {
    final = global1 / global2;
    
  }
  display.innerText = final;
  console.log(final);
  done = true;
}
