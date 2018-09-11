
//getID:
var lbl = document.getElementById("label1");
var txt = document.getElementById("txtans");
var divSuc = document.getElementById("divSuccess");
var divErr = document.getElementById("divError");
var divEl = document.getElementById("but");
var txtValue = txt.value;
//ques
var randomnuberForQue = Math.ceil(Math.random() * 4);
randomnuberForQue =1;
var random1 = Math.ceil(Math.random() * 10);

var random2 = Math.ceil(Math.random() * 10);
var random3 = Math.ceil(Math.random() * 10);
var random4 = Math.ceil(Math.random() * 10);
var random5 = Math.ceil(Math.random() * 10);
var random6 = Math.ceil(Math.random() * 10);
var random7 = Math.ceil(Math.random() * 10);
    


    if (randomnuberForQue == 1) {
        var check = random1 * random2 / random3 + random4;
        lbl.innerHTML = `${random1} * ${random2} / ${random3} + ${random4}`;
        myFunc();
    }

    else if (randomnuberForQue == 2) {
        var check = random1 / random2 * (random3 + random4);
        lbl.innerHTML = `${random1} / ${random2} * (${random3} + ${random4})`;
        myFunc();
    }

    else if (randomnuberForQue == 3) {
        var check = (random1 * random2) / random5 + (random3 + random4);
        lbl.innerHTML = `(${random1} * ${random2}) / ${random5} + (${random3} + ${random4})`
        myFunc();
    }

    else if (randomnuberForQue == 4) {
        var check = random7 + random2 / (random1 * random3) + (random4 * random6);
        lbl.innerHTML = `${random7} + ${random2} / (${random1} * ${random3}) + (${random4} * ${random6})`;
       myFunc();
    }



function refresh(){
    document.location.reload();
}



 function myFunc() {

        

        if (txt.value.length > 0) {

        check = Math.round(check);
        txtValue = txt.value;
        
        
        if (parseInt(txtValue) !== parseInt(check)) {

            setTimeout(() => {
                divErr.style.display = "block";

            }, 100);
            var createEl = document.createElement("button");
            createEl.setAttribute("onclick", "refresh()");
            var createText = document.createTextNode("Again");
            createEl.appendChild(createText);
            console.log(createEl);
            divEl.appendChild(createEl);
        }
        else {

            setTimeout(() => {
                divSuc.style.display = "block";
                divErr.style.display = "none";
            }, 100);


        }


        }
    }