<template>
  <router-view />
</template>

<style>

* {
    box-sizing: border-box;
    font-family: 'Philosopher', sans-serif;
}

body {
    background-color: #102726;
    margin: 0px;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    color: white;
}

header {
    background-color: #163837;
    padding: 0px 10px;
    display: grid;
    grid-template-columns: auto;
    grid-template-rows: auto auto;
}

.logo {
    width: 18%;
    min-width: 90px;
    max-width: 130px;
    vertical-align: middle;
}

.slogan {
    display: inline;
    font-family: 'Tangerine', cursive;
    font-size: 2rem;
    margin-top: auto;
    vertical-align: middle;
}

nav {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

nav a {
    color: white;
    width: 100%;
    text-align: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.5);
    padding: 5px;
    text-decoration: none;
}

nav a:last-child {
    border: none;
}

article {
    padding: 5px;
    background-color: #1B484F;
    display: grid;
    grid-template-columns: 1fr;
    height: auto;
    align-items: flex-start;
    margin-bottom: 10px;
    border-radius: 20px;
}

article > h1 {
    color: white;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    margin-top: 0px;
}

section {
    padding: 10px;
}

.itemBox {
    margin: 10px;
    border-radius: 10px;
    background-color: #102726;
    overflow: hidden;
}

.itemPic {
    width: 100%;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.itemBox > p {
    text-align: center;
    padding: 10px;
}

.itemBox > ul {
    margin: 10px;
}

.itemBox a {
    display: block;
    width: 100%;
    text-align: center;
    text-decoration: none;
    font-size:large;
    color: white;
    background-color: #229C6E;
    padding: 15px;
    margin: 0px;
}

.name {
    font-weight: bold;
}

.itemBox a:hover {
    text-decoration: underline;
}

.articleHeader {
    font-family: 'Philosopher', sans-serif;
    margin-top: 15px;
}

.articleHeader, .wide {
    text-align: center;
    font-size: 1.4rem;
}

.wide {
    font-size: 1.2rem;
    margin: 15px;
}

.wide a {
    display: block;
    width: 30%;
    min-width: 300px;
    margin: auto;
    height: 40px;
    line-height: 40px;
    background-color: #229C6E;
    color:white;
    border-radius: 10px;
    text-decoration: none;
}

.wide a:hover {
    text-decoration: underline;
}

#flavors > div > p {
    margin: 5px;
}

.rounded {
    margin: 10px;
    border-radius: 10px;
    background-color: #229C6E;
    text-align: center;
    line-height: 2rem;
    display: grid;
    grid-template-columns: auto 25%;
    overflow: hidden;
    color: white;
    border: 1px solid white;
}

.rounded div {
    padding: 10px;
}

.rounded > div:last-child {
    background-color: #163837;
}

.order {
    color: white
}

@media (min-width: 500px) {
    article {
        grid-template-columns: 1fr 1fr;
    }

    .articleHeader, .wide {
        grid-column: 1/3;
    }

    #contactInput {
        display: grid;
        grid-template-columns: 12rem 14rem;
        row-gap: 5px;
    }
    
    #contactInput > label {
        text-align: right;
        margin: auto 10px auto auto;
    }

    #contactInput > input {
        width: 14rem;
        margin: auto;
    }
}

@media (min-width: 750px) {
    article {
        grid-template-columns: 1fr 1fr 1fr;
    }

    .articleHeader, .wide {
        grid-column: 1/4;
    }
}

@media (min-width: 1000px) {
    article {
        grid-template-columns: 1fr 1fr 1fr 1fr;
    }

    header {
        grid-template-columns: 45% auto;
    }

    nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-end;
    }
    
    nav a {
        width: auto;
        border-bottom: none;
        border-right: 1px solid rgba(255, 255, 255, 0.5);
        padding: 20px;
    }

    .articleHeader, .wide {
        grid-column: 1/5;
    }
}

footer {
    margin-top: auto;
    padding: 10px;
    background-color: #1B484F;
    color:white;
    min-height: 40px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
}

footer div {
    display: flex;
    align-items: center;
}

footer div span {
    margin-right: 5px;
}

.order form {
    margin-left: 30px;
}

label {
    margin-left: 10px;
}

.radioGroup {
    margin-left: 10px;
}

select, #name, #tel, #email {
    font-size: medium;
    margin-left: 5px;
}

#decorationsInput {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
}

#decorationsInput > div {
    display: flex;
    align-items: center;
    margin: 0px 5px 10px 10px;
}

#submitBtn {
    display: block;
    min-width: 3rem;
    margin: 30px auto;
    background-color: #229C6E; /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    font-size: 16px;
    border-radius: 10px;
}

#submitBtn:hover {
    box-shadow: inset -1px -1px 0px 2px black;
}

#notes {
    font-size: medium;
    margin-left: 10px;
    background-color: rgb(244, 255, 196);
    border-radius: 5px;
    padding: 10px;
}

#contactInput > * {
    display: block;
    width: 80%;
    margin: 0px auto 5px 10px;
}

.flavors {
    display: inline-block;
    margin-bottom: 10px;
}

table {
    border: 1px solid white;
    border-radius: 10px;
    margin: auto;
}

th:first-child {
    border-top-left-radius: 10px;
}

th:last-child {
    border-top-right-radius: 10px;
}

tr:last-child > td:first-child {
    border-bottom-left-radius: 10px;
}

tr:last-child > td:last-child {
    border-bottom-right-radius: 10px;
}

th, td {
    background-color: white;
    color: black;
    padding: 5px;
}

#inventory {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    align-items: center;
}

#orders {
    display: block;
    background-color: #229C6E;
    margin: 10px;
    border-radius: 10px;
    overflow-x: auto;
}

.inventoryGroup {
    padding: 5px;
    margin: 10px;
    background-color: #229C6E;
    border-radius: 10px;
}

section h1 {
    font-family: 'Philosopher', sans-serif;
    text-align: center;
    margin-top: 10px;
    color: white;
}

input {
    background-color: white;
}

select {
    background-color: white;
}



</style>

