<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Events</title>
    <style>
        div{
    height: 100px;
    width: 100px;
    background-color: aquamarine;
    color: white;
    border: 1.5px solid black;
}


    </style>
</head>
<body>
    <button onclick="console.log('button was clicked'); alert('hello')">Click here!</button>
    <button ondblclick="console.log('button was clicked 2x')">Click here 2 times!</button>
    <button id="bt1">Click here!</button>
    <div onmouseover="console.log('you are inside div')">this is a div</div>
    <div>this is a box</div>   
    <script>
    
    //EVENTS-- the change in the state of an object is known as an event

    let bt1 = document.querySelector("#bt1");
    bt1.onclick=() => {
    console.log("bt1 was clicked");
    let i = 46;
    i++;
    console.log(i);
    };

    //Event Handling
    bt1.onclick = () => {
    console.log("button was clicked");
    };

    //Event Object -- It is a special object that has details about the  event

    let div = document.querySelector("div");
    div.onmouseover = (e) => {
    console.log("onmouseover Clicked");
    console.log(e.type);
    console.log(e.target);
    console.log(e.clientX , e.clientY);
    };

    //Event Listeners
    //node.addEventListener(event,callback)

    btn1.addEventListener("click",(e) => {
        console.log("clicked");
        console.log(e);
        console.log(e.type);
        console.log(e.target);
    });

    bt1.addEventListener("click", (e) =>{
    console.log("bt1 was clicked - I");
    });

    bt1.addEventListener("click", (e) =>{
    console.log("bt1 was clicked - II");
    });

    const III = () => {
    console.log("bt1 was clicked - III");
    };
    bt1.addEventListener("click", III);
    
    bt1.addEventListener("click", (e) =>{
    console.log("bt1 was clicked - IV");
    });

    //Remove -- node.removeEventListener(event,callback)
    bt1.removeEventListener("click", III);
    </script>
</body>
</html>
