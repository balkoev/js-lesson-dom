# js-lesson-dom
# Код из youtube видео - https://www.youtube.com/watch?v=4nq-0QUY1ZA

let cases = document.getElementsByClassName("maincounter-number")[0].innerText
let numCases = Number(cases.replace(/,/g, ''))

let recovered = document.getElementsByClassName("maincounter-number")[2].innerText
let numRecovered = Number(recovered.replace(/,/g, ''))

let savePlanet = () => {

    if (numCases >= 1000) {
        numCases -= 1111
        numRecovered += 1111
    } else {
        numCases -= 1
        numRecovered += 1
    }
    document.getElementsByClassName("maincounter-number")[0].innerText = numCases
    document.getElementsByClassName("maincounter-number")[2].innerText = numRecovered

    if (document.getElementsByClassName("maincounter-number")[0].innerText <= 0) {
        myStopFunction()
    }
}

let myStopFunction = () => {
    clearInterval(myVar)
}

let myVar = setInterval(savePlanet, 1)
